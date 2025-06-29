# Pausar a capacidade quando não estiver utilizando reduz o custo?

**Pausar uma capacidade do tipo "Power BI Embedded" reduz o custo,** pois a cobrança é por hora de uso. No caso de uma capacidade do Microsoft Fabric, apesar da cobrança também ser por hora, essa **economia nem sempre acontece.**

## Quando a pausa reduz custo

* **Fabric Capacity (SKU F)**: Cobrado por hora de execução. Pausar a capacidade suspende a cobrança enquanto ela estiver parada, **desde que não haja uso futuro pré-alocado pendente**.
* **Power BI Embedded (SKU A1 a A6)**: Cobradas por hora de execução, pausar a capacidade (via Azure Portal, PowerShell ou REST API) suspende a cobrança.



## Smoothing, Bursting e Throttling

O Microsoft Fabric usa [**smoothing e bursting**](https://learn.microsoft.com/en-us/fabric/data-warehouse/compute-capacity-smoothing-throttling), o que muda a lógica tradicional de "pausar = economizar".

### **Smoothing (Suavização):**

* A suavização permite que cargas de trabalho usem recursos além do limite provisionado (capacidade burstable) durante picos de demanda, distribuindo o consumo de recursos ao longo do tempo.
* A suavização serve para evitar que processamentos pesados consumam toda a capacidade disponível e falhe a execução ou impacte na visualização dos relatórios, ou outras tarefas que estejam em execução.
* Para isso, o Fabric utiliza o conceito de "pré-alocação proporcional de uso futuro". Isso permite usar a capacidade baseada em uso médio, não no pico.
* Quando você executa tarefas de background, como atualização de relatórios ou execução de notebooks, ou pipelines, o sistema **amortiza e distribui o custo ao longo das próximas 24 horas**.
* Para atividades interativas (navegação em relatórios), há suavização mínima de 5 minutos (até 64 min).
* Se você **pausa a capacidade antes do smoothing completar**, o sistema entende que você interrompeu a "janela de pagamento" e cobrará à parte, essas horas que já estavam alocadas, o que pode **até dobrar o custo estimado** se estiver considerando apenas a quantidade de horas ligadas, sem considerar o smoothing.
* Exemplo prático: Se no relatório Fabric Capacity Metrics, estiver mostrando que o processamento de background está em 50%, isso quer dizer que 50% da capacidade já está comprometido para as próximas 24 horas. Se você PAUSAR o recurso do Fabric, esse tempo futuro que foi suavizado será COBRADO à parte e esse custo será mostrado no relatório de custos do portal do Azure.



### **Bursting** (Capacidade Elástica)**:**

* Permite que workloads usem temporariamente mais recursos do que o SKU base, melhorando o desempenho em picos.
* Cada SKU tem um **fator de burst** (e.g. F2 até 32x, F8 pode ter até 12x).



### Throttling (Limitação)**:**

* Ocorre quando o uso médio de CUs ultrapassa os limites suavizados do SKU.
* Operações em andamento não são interrompidas; a limitação se aplica apenas às próximas operações após o consumo ser suavizado.
* **Proteção de sobrecarga**: você pode ultrapassar até 10 minutos de capacidade futura sem sofrer limitações de desempenho.
* Etapas do throttling:
  1. **Delay Interativo**: após 10 min de sobrecarga.
  2. **Rejeição Interativa**: após 60 min de sobrecarga.
  3. **Rejeição Background**: após 24 h de sobrecarga acumulada.



## Quando faz sentido pausar o **Microsoft Fabric**:

* Fora de **horários fixos de execução de pipelines** (ex: 00:00–06:00).
* A utilização da capacidade é majoritariamente composta por ações interativas (visualização e navegação nos relatórios).
* Baixo consumo de capacidade por operações de background.
* **Importante:** Sempre analise e acompanhe o consumo da capacidade pela tela de Gerenciamento de custos do Azure para verificar se realmente está ocorrendo uma economia. A partir do 2º dia após alterações no agendamento das pausas da capacidade já é possível analisar o custo diário.



## Quando faz sentido pausar o **Power BI Embedded**:

* Sempre que não estiver com relatórios embutidos em uso — não há smoothing, só cobrança por tempo ligado da capacidade, então o cálculo de economia é tão simples quanto contar a quantidade de horas que ficou ligado x custo por hora da capacidade.



## Boas práticas de uso da capacidade

1. **Evite pausar imediatamente após tarefas pesadas** no Fabric.
2. Use o relatório de métricas para analisar uso de background ativo.
3. Planeje **janelas fixas de disponibilidade da capacidade** com agendamentos alinhados.
4. Considere **escalar para uma SKU menor em vez de pausar**, se uso for contínuo, mas leve.
5. Em muitos cenários, faz mais sentido **ativar a reserva da instância** e deixar ligado 24x7 do que ficar pausando a capacidade para reduzir custos.
6. Sempre monitore e acompanhe o custo diário da capacidade para conseguir estimar quanto será o custo mensal no final do mês pela página de gerenciamento de custos no portal do Azure e evitar sustos. Não espere a fatura chegar para saber quanto a capacidade irá custar.



## Como reduzir o consumo de capacidade

Se seu ambiente tem sobrecarregamentos constantes, isso pode indicar a necessidade de:

* Avaliar se é necessário a**umentar o SKU** da capacidade.
* **Dividir workloads** ou espalhá-los em múltiplas capacidades.
* **Otimizar** as atividades interativas:
  * Otimizar medidas DAX com alto consumo de capacidade.
  * Evitar colunas calculadas e tabelas calculadas, se possível.
  * Reduzir número de visuais na mesma página (não ter mais de 10 é o recomendado).
  * Otimizar a modelagem dos modelos semânticos, como evitar relacionamentos N:N e filtragem bi-direcional.
  * Identificar e remover colunas e tabelas não utilizadas.
  * Pré-agregar os dados antes de importá-los para o Power BI.
  * Analisar o consumo das medidas que estão aplicando filtro de segurança por linha (RLS).
* Otimizar a atualização dos modelos semânticos:
  * Otimização do código M (Power Query) e garantir que o Query Folding está ocorrendo.
  * Utilização de carregamento incremental dos dados.
  * Analisar os índices e a performance geral das consultas e fontes de dados.
  * Pré-agregar os dados antes de importá-los para o Power BI.
  * Identificar e remover colunas e tabelas não utilizadas.
  * Otimizar tipos de dados das colunas, como substituir "Número decimal" por "Número decimal fixo", quando possível, especialmente em tabelas Fato com alta cardinalidade.
  * Avaliar propriedades IsAvailableInMdx e o Encoding Hint da coluna.
  * Separar colunas datetime em uma coluna de data e outra de tempo ou somente hora, dependendo do nível de granularidade desejado.
  * Avaliar o uso de DirectQuery ou DirectLake para volumes de dados muito grandes.



Se você precisa de ajuda profissional de uma equipe de especialistas para ajudar a sua empresa a reduzir o consumo de capacidade, [clique aqui neste link](https://powertuning.com.br/reuniao-bi) para agendar uma reunião com nosso time comercial.

Temos diversos casos de empresas que tiveram grande redução no consumo de capacidades, saindo de F64 para F8, por exemplo.

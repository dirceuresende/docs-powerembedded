# Capacidades dedicadas

### Fabric? Power BI Embedded? O que é isso?

As capacidades são recursos do Power BI que licenciam a solução do Power Embedded junto à Microsoft e permitem utilizar as API’s, de forma legal e ilimitada, para inserir os relatórios publicados no sistema e não precisar de licença para visualizar os relatórios.

Sem uma capacidade contratada, utilizando uma conta Pro ou PPU, você tem uma quantidade limitada de tokens para inserção de relatórios. Após um tempo, esse limite é atingido e o Power BI não permite mais inserir relatórios e o Power Embedded iria parar de funcionar. **Por este motivo, é obrigatório ter uma capacidade** **contratada para utilizar o Power Embedded.**

{% hint style="warning" %}
Caso alguém tente acessar o relatório fora desses horários, o relatório não irá abrir e nem atualizar os dados, pois irá apresentação uma mensagem de erro informando que a capacidade está desligada.



O Power Embedded, quando configurado, poderá ligar automaticamente a capacidade para permitir que visualizem os relatórios e irá desligar automaticamente após um período de inatividade (definido por você).
{% endhint %}

&#x20;

Tipos de capacidades (todas são suportadas pelo Power Embedded):

* Fabric: Mais nova, flexível, mais recursos e pode começar mais barato.
* Power BI Embedded: Mais estável, confiável e pode ser mais barato no modelo pago pelo uso, dependendo da região e tamanho.
* Premium por Capacidade: Capacidade que foi descontinuada e o custo inicial é 32 mil reais por mês.

&#x20;

Observações:

* As capacidades são contratadas direto com a Microsoft (ou parceiro) pelo Azure.
* Ter uma capacidade é um requisito para o Power Embedded funcionar.
* Microsoft libera um período de avaliação gratuito de 60 dias para o Fabric.



### Como é a cobrança

A cobrança da capacidade do Embedded é calculada a nível de segundo pela Microsoft, e convertida para hora para gerar a cobrança final, e o nosso sistema permite definir os períodos de horários, por dia da semana, que o sistema irá ficar ligado e fora desse horário, o próprio sistema já desliga a capacidade automaticamente.



## Como estimar a capacidade ideal

Para definir qual a capacidade mais indicada do Power BI Embedded ou Microsoft Fabric para o seu cenário, você pode nos enviar a quantidade e o tamanho de cada conjunto de dados do Power BI que será importado para a plataforma para termos uma estimativa de qual capacidade mais adequada para o seu cenário, mas iria te gerar um trabalho grande para fazer esse levantamento e seria apenas uma estimativa, pois existem vários outros fatores que influenciam no uso da capacidade além de só o tamanho.

O melhor caminho para realizar essa estimativa, seria utilizando o período de 60 dias de avaliação gratuita do Microsoft Fabric, onde poderemos rodar toda a PoC de forma gratuita, fazendo com que os relatórios atuais sejam atualizados e processados por essa capacidade trial gratuita (F64).

A partir do momento que o workspace é alterado para utilizar a capacidade do Fabric, o Power BI começa a coletar dados e estatísticas do uso real dessa capacidade.

Utilizando o relatório “[Fabric Capacity Usage Metrics](https://appsource.microsoft.com/en-us/product/power-bi/pbi\_pcmm.microsoftpremiumfabricpreviewreport)”, disponibilizado pela própria Microsoft, é possível identificar com muito mais precisão qual capacidade que o seu ambiente necessita.

Se você já for cliente do Power Embedded, terá acesso GRATUITO ao curso de Análises de Capacidades com o Microsoft Fabric.

{% embed url="https://cursos.powertuning.com.br/course/microsoft-fabric-analise-de-capacidade" %}

{% hint style="info" %}
Se você tiver interesse em ter acesso gratuito ao curso, entre em contato com o time de suporte, informe seu email e solicite seu acesso.

**Observação:** Disponível apenas para clientes após o período de avaliação gratuito.
{% endhint %}

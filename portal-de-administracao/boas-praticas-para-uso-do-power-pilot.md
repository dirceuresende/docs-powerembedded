# Boas práticas para Uso do Power Pilot

## Modelagem:

O modelo semântico é o coração da interação entre os seus dados no Power BI e a IA. Ele traduz a estrutura técnica dos dados em conceitos de negócio compreensíveis, permitindo que a IA entenda perguntas como:

“Qual foi o valor total de vendas por categoria no último trimestre?”

Para que essa interpretação seja correta, o modelo deve refletir relações claras entre os dados presentes no conjunto.

O modelo **Star Schema** é a arquitetura recomendada para modelos analíticos em geral e é especialmente importante em soluções de Power BI principalmente quando integradas a ambiente com IA. É um modelo mais enxuto e coeso, o que permite melhor interpretação das relações entre tabelas.

<figure><img src="../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure>

**• Fato:** \
Concentra eventos ou transações do negócio. \
&#x20;    FatoVendas, FatoPedidos,FatoAtendimentos

•**Dimensão:** \
Descreve atributos contextuais relacionados às tabelas  fatos.\
&#x20;    DimCliente,DimProduto,DimTempo,DimRegiao

#### **Características Principais:**

1. Relacionamentos do tipo 1:N;
2. Sem joins complexos ou múltiplos caminhos ambíguos.&#x20;
3. Estrutura simples e intuitiva para interpretação semântica.&#x20;

#### Benefícios para o Power Pilot:

1. Facilita o entendimento das relacções entre fatos e dimensoes
2. Permite à IA identificar métricas de negócios e seus contextos ( quem, quando, onde, o quê).
3. Evita ambiguidade semântica em modelos complexos ( como snowflake schemas)
4. Melhora a eficiência e a precisão na geração das consultas DAX.

#### Nomeação:

O assistente trabalha com PLN ( Processamento de Linguagem Natural), o que faz com que ela analise o modelo do Power BI linguisticamente, ou seja, os nomes e descrições tem extrema importancia na forma como a IA compreende os dados.&#x20;

* **Evite abreviações:**  Use nomes completos e claros. \
  &#xNAN;_&#x45;xemplo:_ QuantidadeVendida  e evite usar QtdVend
* **Use nomes descritivos e semânticos:** Deixe explicito o significado. \
  &#xNAN;_&#x45;xemplo:_ ValorVenda, DataPedido,CategoriaProduto e evite usar ValVen,DataPed.
* **Evite caracteres especiais e acentos:** Use apenas letras e números.\
  &#xNAN;_&#x45;xemplo:_ PrecoUnitario evite Preço\_Unitário &#x20;



Cada tabela e coluna no Power BI possui um campo de descrição, que pode (e deve) ser preenchido cin informações sobre:

1. &#x20;O significado do dado;
2. O contexto de negócio;
3. A forma de cálculo ou origem da informação.

Essas descrições são consumidadas diretamente pela IA, ampliando sua capacidade de racionar de raciocinar sobre o contexto e gerar respostas mais precisas e contextualizadas.

> AVISO: É importante que as descrições sejam claras, porém sucinta e objetivas. A quantidade de conteúdo utilizado na descrição impacta no uso de tokens, ou seja, tenha cautela ao escrever suas descrições no modelo.

_Exemplo:_

**Tabela:** FatoVendas\
**Descrição:** Contém os registros de vendas realizadas. Cada linha representa uma transação individual. As medidas associadas refletem o valor e a quantidade vendida.

**Coluna:**&#x56;alorVenda\
**Descrição:** Valor monetário total da venda, considerando descontos aplicados.

<figure><img src="../.gitbook/assets/image (449).png" alt=""><figcaption></figcaption></figure>

O ponto se aplica à medidas, defina medidas DAX claras, nomeadas semanticamente e documentadas.

1. Use nomes significativos: TotalVendas, LucroBruto,MargemPercentual;
2. Evite medidas duplicadas ou com lógica redundante;
3. Documente as descrições.


# Configurar faturamento

Uma necessidade bem comum entre os clientes do Power Embedded, é alterar o dia de vencimento das faturas, os emails de cobrança e alguns dados cadastrais para o faturamento, como informar a ordem/pedido de compra.

Para simplificar esse processo e deixar que o usuário seja autossuficiente nessa gestão dos dados de faturamento, foi disponibilizada uma tela onde o administrador do sistema consegue editar todos esses dados.

<figure><img src="../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Para saber mais sobre isso, acesse a tela de [**Configurações de Faturamento**](https://admin.powerembedded.com.br/Organization/BillingSettings/).
{% endhint %}



Na tela de Configurações de Faturamento, você poderá cadastrar e alterar:

* O CNPJ ou CPF de faturamento do Power Embedded
* País
* Inscrição Municipal e Inscrição Estadual (campos opcionais)
* E-mails de Cobrança (quem irá receber a mensalidade)
* Dia do Vencimento e Recorrência da Cobrança
* Informações adicionais de faturamento, como pedido de compra (se necessário)

<figure><img src="../../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure>



Após digitar/alterar o CNPJ, o sistema vai preencher todos os dados da sua empresa, como a razão social, nome fantasia, endereço, conforme a imagem abaixo:

<figure><img src="../../.gitbook/assets/image (285).png" alt=""><figcaption></figcaption></figure>

Se o valor inserido no campo de CNPJ/CPF tenha sido o número de CPF, a opção de **Pessoa Física** será ativada automaticamente.

Se sua empresa estiver enquadrada no **Regime MEI, ou seja** optante pelo **Simples Nacional**, basta ativar essas opções.



### Configurações de Cobrança

<figure><img src="../../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure>

#### **Tipos de Recorrência da Cobrança**

1. **Dias após o primeiro dia do mês de pagamento:** Quantidade de dias contados a partir do dia 01 do mês. Por exemplo, se você configurar 45 dias, o vencimento da cobrança será 45 dias a partir do dia 01 do mês de faturamento. Valores válidos: Entre 1 e 90 dias.
2. **Dia específico do mês de pagamento:** Essa recorrência indica que a cobrança será gerada em um dia específico de cada mês. Por exemplo, se você configurar 15 dias, o faturamento será gerado sempre no dia 15 do mês de faturamento, independente do dia que o faturamento foi gerado. Valores válidos: Entre 1 e 30 dias.
3. **Dia especifico no mês seguinte ao faturamento:** Parecido com a opção anterior, essa recorrência indica que a cobrança será gerada em um dia específico do próximo mês. Por exemplo, se você configurar 15 dias, o faturamento será gerado sempre no dia 15 do mês seguinte ao faturamento realizado. Valores válidos: Entre 1 e 30 dias.
4. **Dias a partir da data de faturamento:** Número de dias que serão contados a partir da data em que a fatura é gerada. Por exemplo, se você configurar 15 dias, a data de vencimento será 15 dias a partir do dia que o faturamento foi realizado, que geralmente ocorre nos primeiros 5 dias úteis do mês. Valores válidos: Entre 1 e 90 dias.



Ao clicar em “**SALVAR”,** o sistema irá sincronizar os dados com o sistema de faturamento do Power Embedded.


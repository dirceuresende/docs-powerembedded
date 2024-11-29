# Dúvidas Power Pilot

## Introdução

Esta documentação foi criada para esclarecer as principais dúvidas relacionadas à funcionalidade do **Power Pilot**. Aqui, você encontrará respostas detalhadas sobre o que é o Power Pilot, como ele funciona, seus custos, integrações e outras questões importantes.



{% hint style="info" %}
Esta documentação tem o objetivo de responder às possíveis dúvidas que você pode ter em relação à funcionalidade do Power Pilot. Para configurar o Power Pilot, siga a documentação oficial: **Como configurar o Power Pilot**.
{% endhint %}

## O que é Power Pilot ?

O **Power Pilot** é uma IA generativa desenvolvida para ajudar você a criar assistentes personalizados que respondem às suas perguntas de negócios de maneira eficiente.

#### **Pré-requisitos e Funcionamento**

Para utilizar o Power Pilot, é necessário:

1. **Contratar um modelo de IA**: Pode ser da OpenAI ou do Azure OpenAI. O uso do modelo é cobrado por token.
2. **Cadastrar o modelo no portal de administração do Power**: Após contratar o modelo, ele precisa ser configurado no portal de administração.

## Principais dúvidas em relação ao Power Pilot

<details>

<summary><strong>Como funciona o custo do Power Pilot?</strong></summary>

O custo é calculado por tokens:

* **Token de entrada (input)**: As perguntas feitas ao assistente.
* **Token de saída (output)**: As respostas geradas pelo assistente.

Por exemplo, com o modelo **GPT-4o-mini**:

* **Custo de input**: $0,15 de dólares por 1 milhão de tokens.&#x20;
* **Custo de output**: $0,60 dólares  por 1 milhão de tokens.

Você só será cobrado quando atingir 1 milhão de tokens, tornando a funcionalidade acessível e econômica. Além disso, se não houver interação com o assistente, não haverá custo

Preço dos modelos de IA: [https://openai.com/api/pricing/](https://openai.com/api/pricing/)

</details>

<details>

<summary><strong>O que é um token ?</strong></summary>

Os grandes modelos de linguagem processam texto usando **tokens**, que são sequências de caracteres (como palavras ou partes de palavras). Esses modelos aprendem as relações entre tokens e geram respostas baseadas nas sequências.\
\
No site da Open AI, você consegue ter uma demonstração do que é tokens, e uma comparação com caracteres\
\
Tokenizer: [https://platform.openai.com/tokenizer](https://platform.openai.com/tokenizer)



</details>

<details>

<summary><strong>Existe previsão de custo mensal?</strong></summary>

Por ser uma funcionalidade paga por uso, o custo pode variar. No entanto, em testes realizados, 400 perguntas feitas ao assistente resultaram em um custo inferior a 5 dólares.

Além disso, no portal de administração do Power Embedded, há uma auditoria específica para o uso do Power Pilot. Essa funcionalidade é muito útil quando é necessário acompanhar a quantidade de tokens utilizados, estimar os custos e obter uma visão geral sobre o consumo. Com isso, você consegue ter uma estimativa precisa dos custos envolvidos.

</details>

<details>

<summary><strong>Como funciona a integração com o WhatsApp?</strong></summary>

**A integração com o WhatsApp exige:**

* Um modelo de IA contratado.
* Um assistente configurado no portal.

**Custos:**

* **Número padrão**: R$150/mês. Esse é o número do Power Pilot, onde o cliente não pode personalizar a foto ou algumas informações no WhatsApp.
* **Número personalizado**: R$200/mês. Nesse caso, o cliente pode utilizar um número próprio, personalizando a foto e algumas informações do WhatsApp. (Esse número ele não pode ser utilizado em um celular, tem quer ser um número somente para IA)

**Observação:** Você pode utilizar um único número de WhatsApp para gerenciar vários assistentes. Quando um usuário interagir com o Power Pilot no WhatsApp, serão exibidos apenas os assistentes para os quais ele possui permissão.

</details>

<details>

<summary><strong>É possível dar permissões para usuários ou grupos específicos?</strong></summary>

Sim, ao criar um assistente, você pode definir:

* Quem terá acesso (usuários ou grupos específicos).
* Se a funcionalidade estará disponível no WhatsApp ou não para determinados usuários ou grupos

</details>

<details>

<summary><strong>O Power Pilot é diferente do Copilot ?</strong></summary>

Sim, ambas são ferramentas de inteligência artificial porém distintas:

* O **Power Pilot** foi desenvolvido pela equipe do **Power Embedded** com foco em fornecer respostas de negócios a baixo custo. Podendo utilizar essa funcionalidade mesmo na menor capacidade do Fabric, como uma F2.
* O **Copilot**, da Microsoft, está disponível no Power BI para usuários do plano a partir do SKU F64, que tem um custo inicial elevado.

</details>

<details>

<summary><strong>O Power Pilot funciona se eu usar a funcionalidade de "Mostrar os relatórios na aplicação"</strong></summary>

Sim, é possível utilizar a funcionalidade do Power Pilot. No entanto, como o Power Pilot é exibido na barra de navegação do relatório, é necessário configurar o parâmetro **HideNavbar** da API de Identity como **true** (hideNavbar = TRUE) para habilitar essa funcionalidade corretamente.

</details>

<details>

<summary><strong>Eu não tenho uma assinatura paga no Azure ? Posso usar a gratuita ?</strong></summary>

Para utilizar a funcionalidade do **Power Pilot**, é recomendado ter uma assinatura paga no Azure. A assinatura gratuita oferecida pelo Azure tem uma limitação de tokens, geralmente inferior a 10K tokens por minuto, o que é insuficiente para o uso ideal dessa funcionalidade.

A **Power Tuning**, é parceira Microsoft, e pode ajudá-lo a criar sua assinatura no Azure. Nosso time pode configurar essa assinatura para você, permitindo que, a partir dela, você contrate o recurso de IA necessário para utilizar o Power Pilot.

Tornar-se parceiro Microsoft é gratuito. Basta preencher o formulário no link abaixo, e nosso time de Cloud entrará em contato:

\
[**Torne-se parceiro Microsoft**](https://powertuning.com.br/parceria-azure)[\
](https://powertuning.com.br/parceria-azure)

</details>

<details>

<summary><strong>É preciso treinar o modelo ?</strong></summary>

Não é necessário treinar o modelo para utilizar o Power Pilot. Todos os prompts já são configurado internamente via código. Basta seguir as instruções da nossa documentação para configurar o Power Pilot e começar a utilizá-lo imediatamente.\
\
[Documentação Power Piltot](https://docs.powerembedded.com.br/portal-de-administracao/power-pilot-ia)

</details>

<details>

<summary><strong>Eu já tenho um GPT Pro contratado na open AI, posso utilizar no Power Pilot ?</strong></summary>

Não, o GPT Pro é o GPT como serviço. No caso do Power Pilot, é necessário utilizar a API de um modelo de IA. Quando você precisa de uma IA isolada ou personalizada, pode contratar as APIs, e o cliente tem a liberdade de escolher o modelo que deseja usar, como o GPT-4, GPT-4O Mini, entre outros.

</details>

# Assistentes de IA

{% embed url="https://www.youtube.com/watch?v=J7TKL4maKbI" %}

### Como configurar o PowerPilot (IA) no Power Embedded

Para que você tenha um assistente no portal, é preciso fazer a configuração dos seguintes passos:

1. Validar os [pré-requisitos](pre-requisitos.md) no Portal de Administração do Power BI.
2. Contratar o modelo no [Azure OpenAI](contratacao-de-uma-ia/azure-openai.md) ou [OpenAI (ChatGPT)](contratacao-de-uma-ia/openai.md)
3. [Criar um modelo](modelos-de-ia.md) no Power Embedded
4. [Criar um assistente](assistentes-de-ia.md) no Power Embedded (você está aqui)



### O que é um assistente?

Um assistente é uma aplicação de inteligência artificial projetada para ajudar os usuários a responder a perguntas, fornecer informações de maneira eficiente e personalizada.&#x20;

O assistente utiliza modelos avançados de linguagem natural, como o GPT (Generative Pre-trained Transformer), para entender e gerar texto de forma que imite a interação humana.



### Criando um assistente de IA do Power Pilot

O próximo passo é criar um assistente para que os usuários que você permiti eles consigam visualizar e fazer suas respectivas perguntas.&#x20;

Esse menu é de extrema importância, pois é nele que você faz toda a configuração e defini quais usuários ou grupos vão acessar e qual conjunto de dados que esse assistente vai ter acesso.

Para criar um assistente é preciso ir ao menu **Power Pilot – IA > Assistente > Criar assistente.**

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

Nesta tela, você poderá configurar as seguintes configurações:

* **Geral:** Nesse menu é preciso definir um nome para o seu assistente e escolher qual modelo ele vai estar vinculado, esse modelo se refere ao modelo de IA criado anteriormente.\
  \
  Está destacado o campo **Cadeia de conexão da conta de armazenamento do Azure** ou **Azure storage account connection string**. Para utilizar a funcionalidade de gerar um arquivo .CSV, é necessário ter uma **Storage Account** no Azure para gerenciar o tráfego de arquivos.\
  \
  Se você já possui essa conta, basta preencher o campo com o valor da **“connection string”**, que pode ser encontrado na aba **“Chave de acesso”** dentro da sua Storage Account. Não é necessário ter uma **Storage Account** para criar um assistente, somente se você quiser ter a opção de baixar um arquivo.\

* **Usuários:** Neste menu, você definirá quais usuários terão acesso ao assistente criado. Se um usuário não estiver associado a nenhum assistente, o assistente não ficará disponível para ele. Lembre-se de que, se o usuário fizer parte de um grupo ao qual você conceder acesso, o usuário também poderá visualizar o assistente.\

* **Grupos:** Neste menu, você definirá quais grupos terão acesso ao assistente criado. Se um grupo não estiver associado a nenhum assistente, o assistente não ficará disponível para os usuários daquele grupo.\

* **Conjunto de dados:** Aqui, você escolherá o conjunto de dados com o qual o modelo associado responderá às perguntas dos usuários.

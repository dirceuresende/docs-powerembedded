# OpenAI

### Como configurar o PowerPilot (IA) no Power Embedded

Para que você tenha um assistente no portal, é preciso fazer a configuração dos seguintes passos:

1. Validar os [pré-requisitos](../pre-requisitos.md) no Portal de Administração do Power BI.
2. Contratar o modelo no [Azure OpenAI](azure-openai.md) ou [OpenAI (ChatGPT)](openai.md) (você está aqui)
3. [Criar um modelo](../modelos-de-ia.md) no Power Embedded
4. [Criar um assistente](../assistentes-de-ia.md) no Power Embedded



Requisitos para criação de um assistente no portal da OpenAI.

* Ter uma conta cadastrada na OpenAI.
* Ter um método de pagamento configurado para ser efetuada a cobrança. (É preciso ter um método de pagamento cadastrado para que o assistente funcione)

Para criar o recurso de IA acesso [clique nesse link](https://platform.openai.com/assistants).



**1° Passo** – O primeiro passo para criar um assistente pela OpenAI é preciso criar uma "Secret Key". Para isso vá em **API Keys > Create new secret key.**

<figure><img src="../../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>



Após clicar em **API Keys** ou **Chave API**, você verá um botão para validar seu número de telefone, caso sua conta seja recém-criada. Após a validação, você poderá criar sua primeira chave de API.

O campo  **Owned By** ou  **propiedade de** , pode manter como padrão, defina um nome para sua chave e clique em **Create secrect key**

<div align="left">

<figure><img src="../../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

</div>



Certifique-se de copiar e armazenar sua chave de API em um local seguro. Veja o exemplo abaixo:

<div align="left">

<figure><img src="../../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

</div>



Copie essa chave e salve em um bloco de notas. Essa chave é o que você irá colar no campo “Chave” na criação do modelo de IA no portal de administração. Muito importante salvar essa chave, pois ao sair dessa tela a mesma não será possível recuperar.

**2° Passo –** Definir qual o modelo do seu assistente de IA.

<figure><img src="../../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>



Ao clicar em “Create” você é redirecionado para a aba de criação desse modelo.

Preencha os campos de nome e defina qual modelo de IA, vai ser utilizado. Para essa documentação estamos utilizando o “gpt-4o-mini” que atualmente tem menor custo por tokens. Ao preencher os campos basta criar o assistente.

<figure><img src="../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

Pronto, agora precisamos ir ao portal do Power Embedded para Criar um modelo e criar um assistante.

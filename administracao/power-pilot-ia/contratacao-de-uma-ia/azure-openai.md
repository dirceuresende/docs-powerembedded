# Azure OpenAI

### Como configurar o PowerPilot (IA) no Power Embedded

Para que você tenha um assistente no portal, é preciso fazer a configuração dos seguintes passos:

1. Validar os [pré-requisitos](../pre-requisitos.md) no Portal de Administração do Power BI.
2. Contratar o modelo no [Azure OpenAI](azure-openai.md) ou [OpenAI (ChatGPT)](openai.md) (você está aqui)
3. [Criar um modelo](../modelos-de-ia.md) no Power Embedded
4. [Criar um assistente](../assistentes-de-ia.md) no Power Embedded



Para criar o recurso de IA no Azure [clique nesse link](https://portal.azure.com/#view/Microsoft\_Azure\_ProjectOxford/CognitiveServicesHub/\~/OpenAI).

<figure><img src="../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>



Agora você precisa preencher as informações necessárias para contratação do recurso.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

</div>



Após vir para essa próxima tela, pode deixar selecionado a primeira opção.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

</div>



Nessa aba, caso você tenha tags para identificar recursos com base em configurações da empresa, basta associar. Caso não tenha, deixe em branco.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

</div>



Após verificar os dados e as configurações, basta criar o recurso clicando em “Create”.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

</div>



Ao criar o recurso precisamos ir até a aba de **“Keys and Endpoint”** para copiar dois valores importantes que iremos utilizar na criação do Modelo de IA no portal de administração do Power Embedded.

<figure><img src="../../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>



Com o recurso criado agora precisamos definir qual vai ser o modelo que iremos utilizar [clique nesse link.](https://oai.azure.com/portal/)

Nessa nova tela vá em **Implantações > Criar uma implantação.**

<figure><img src="../../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>



Escolher o modelo de IA é uma etapa essencial na configuração do seu assistente virtual. Nesta documentação, optamos pelo modelo GPT-4o-mini devido ao seu custo mais acessível por token. [Clique e saiba mais](https://azure.microsoft.com/pt-br/pricing/details/cognitive-services/openai-service/)

<div align="left">

<figure><img src="../../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>

</div>

Você pode definir o limite de taxa de tokens de acordo com suas necessidades de uso do assistente. No entanto, para garantir uma experiência mais fluida e eficiente, é recomendável manter o limite mínimo de 100K tokens por minuto.

Pronto, no portal do Azure finalizamos todo o processo, agora iremos no portal de administração do Power Embedded fazer a criação do modelo e do assistente.

# Modelos de IA

{% embed url="https://www.youtube.com/watch?v=J7TKL4maKbI" %}

### Como configurar o PowerPilot (IA) no Power Embedded

Para que você tenha um assistente no portal, é preciso fazer a configuração dos seguintes passos:

1. Validar os [pré-requisitos](pre-requisitos.md) no Portal de Administração do Power BI.
2. Contratar o modelo no [Azure OpenAI](contratacao-de-uma-ia/azure-openai.md) ou [OpenAI (ChatGPT)](contratacao-de-uma-ia/openai.md)
3. [Criar um modelo](modelos-de-ia.md) no Power Embedded (você está aqui)
4. [Criar um assistente](assistentes-de-ia.md) no Power Embedded



### Como criar um modelo de IA no Power Embedded

Acesse a página de Power Pilot IA > Modelos ou [clique aqui](https://admin.powerembedded.com.br/AiModels/Create).

Clique no botão **Criar Modelo de IA**.

<div>

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption><p>Azure OpenAI</p></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption><p>OpenAI</p></figcaption></figure>

</div>



Nesta tela, você poderá configurar as seguintes configurações conforme o provedor da API de IA que você irá utilizar.

* **Nome:** É o nome que terá seu modelo (Pode ser qualquer nome que você definir)

<details>

<summary>Azure OpenAI</summary>

**Modelo:** Nesse campo é preciso preencher o nome do modelo contratado. (Exemplo: Gpt-4o-mini, Gpt-4 e etc.). Para ficar mais fácil a busca do nome do modelo. [**Clique nesse link**](https://oai.azure.com/portal/0ce7f057e4df4ba9bbc98993a2088133/deployment?tenantid=eaa0c55d-e848-4192-ad75-91deaadc01f4)**.**

<img src="../../.gitbook/assets/image (65).png" alt="" data-size="original">



**Endpoint:** Esse campo é preenchido com o valor do Endpoint.

<img src="../../.gitbook/assets/image (58).png" alt="" data-size="original">



**Chave:** Preencher esse campo com o valor da chave criada. Abaixo orienta o caminho dependendo de onde o assistente foi criado.

![](<../../.gitbook/assets/image (59).png>)



**Custo em dólar para 1 milhão de tokens de entrada:** Preencha este campo com o valor dos tokens por interação de perguntas, que varia conforme o modelo contratado. Evite usar valores aleatórios, pois isso pode afetar a auditoria do Power Pilot. Consulte a seção de preços na [Azure](https://azure.microsoft.com/pt-br/pricing/details/cognitive-services/openai-service/) para saber o valor exato.

**Custo em dólar para 1 milhão de tokens de saída: Preencha** este campo com o valor dos tokens por interação de respostas, que varia conforme o modelo contratado. Evite usar valores aleatórios, pois isso pode afetar a auditoria do Power Pilot. Consulte a seção de preços na [Azure](https://azure.microsoft.com/pt-br/pricing/details/cognitive-services/openai-service/) para obter o valor exato.&#x20;

</details>

<details>

<summary>OpenAI</summary>

**Modelo:** Selecione o modelo que você quer utilizar no drop-down.



**Chave:** Preencher esse campo com o valor da chave criada.

![](<../../.gitbook/assets/image (66).png>)



**Tokens de prompt:** Preencha este campo com o valor dos tokens por interação de perguntas, que varia conforme o modelo contratado. Evite usar valores aleatórios, pois isso pode afetar a auditoria do Power Pilot. Consulte a seção de preços no site da [OpenAI](https://openai.com/api/pricing/) para saber o valor exato.

**Tokens de conclusão: Preencha** este campo com o valor dos tokens por interação de respostas, que varia conforme o modelo contratado. Evite usar valores aleatórios, pois isso pode afetar a auditoria do Power Pilot. Consulte a seção de preços no site da [OpenAI](https://openai.com/api/pricing/) para obter o valor exato.

</details>

Modelo criado agora precisamos criar um assistente

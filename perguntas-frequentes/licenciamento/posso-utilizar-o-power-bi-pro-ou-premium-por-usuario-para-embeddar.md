# Posso utilizar o Power BI Pro ou Premium por Usuário para Embeddar?

### Conheça as formas corretas de incorporar relatórios

Antes de utilizar a tecnologia de [Análise integrada do Power BI](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-analytics-power-bi) para incorporar relatórios em portais e aplicações Web, seja para redução de custos, recursos avançados e personalização, você deve entender que existem 2 modelos de licenciamento:

* [Inserir para seus clientes](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-analytics-power-bi#embed-for-your-customers): Permite que você crie um aplicativo que utiliza um Service Principal para autenticar e interagir com os dados no Power BI. Seus usuários não precisam entrar usando credenciais do Power BI para ver o conteúdo inserido e o licenciamento ocorre contratando uma capacidade para licenciar os workspaces dos relatórios.
* [Inserir para a organização](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-analytics-power-bi#embed-for-your-organization): Permite que você crie um aplicativo que requer o uso de uma conta Pro do Power BI para cada usuário. Os usuários inscritos só podem consumir o conteúdo inserido aos quais eles têm acesso no serviço do Power BI.

| Inserir para seus clientes                                                                                          | Inserir para a organização                                                                          |
| ------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Também conhecida como app owns data                                                                                 | Também conhecida como **user owns data**                                                            |
| Para autenticar usuários do aplicativo, usa o seu próprio método de autenticação                                    | Os usuários do aplicativo se autenticam no Microsoft Entra ID                                       |
| Os usuários do aplicativo não precisam de uma licença                                                               | Cada usuário do aplicativo precisa de uma licença do Power BI                                       |
| Autenticação não interativa. Seu aplicativo usa uma _entidade de serviço_ ou um _usuário mestre_ para se autenticar | Autenticação interativa. Seu aplicativo usa as credenciais do usuário do aplicativo para autenticar |

{% hint style="danger" %}
**Caso você esteja utilizando uma plataforma que utilize uma conta Pro para gerar os tokens de inserção de relatórios, sem utilizar uma capacidade para isso, você provavelmente está violando os termos de uso do Power BI e sua empresa pode sofrer multas e sanções pela Microsoft.**
{% endhint %}



### Posso incorporar relatórios utilizando apenas uma conta PRO ou PPU?

É possível gerar tokens para incorporar relatórios em uma capacidade Pro ou Premium por Usuário, mas de acordo com a [documentação oficial da Microsoft:](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/move-to-production)

“Os tokens incorporados com licença Pro ou Premium por usuário (PPU) destinam-se a testes de desenvolvimento, portanto, uma conta mestra ou Service Principal do Power BI só pode gerar um número limitado de tokens.

Adquira uma capacidade para incorporação em um ambiente de produção. Não há limite para quantos tokens incorporados você pode gerar ao comprar uma capacidade.

Nos testes de desenvolvimento, você pode usar tokens de avaliação incorporados gratuitos com uma licença Pro. **Para incorporar em um ambiente de produção, você deve adquirir uma capacidade.**

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/05/Power-Embedded-Mover-aplicacao-para-producao.png" alt=""><figcaption></figcaption></figure>

A página de [perguntas e respostas do Power BI Embedded](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#quantos-tokens-inseridos-posso-criar-) reafirma que contas Pro não podem ser utilizadas para soluções de Embedded em produção:

“Os tokens inseridos com a licença Pro ou PPU (Premium por usuário) destinam-se para teste de desenvolvimento, portanto, uma conta mestre ou [entidade de serviço](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embed-service-principal) do Power BI pode gerar apenas um número limitado de tokens. [Compre uma capacidade](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#technical) para inserir em um ambiente de produção. Não há limites para a quantidade de tokens inseridos que você pode gerar ao comprar uma capacidade. Em testes de desenvolvimento, você pode usar tokens de avaliação de inserção gratuitos com uma licença Pro. Para fazer uma inserção em um ambiente de produção, você deve comprar uma capacidade."

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded-3.png" alt=""><figcaption></figcaption></figure>

&#x20;

A página [Cenários de uso do Power BI: inserir para clientes – Power BI | Microsoft Learn](https://learn.microsoft.com/pt-br/power-bi/guidance/powerbi-implementation-planning-usage-scenario-embed-for-your-customers#licensing) também reforça que o uso de uma capacidade é obrigatório para utilizar tecnologias de Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded.png" alt=""><figcaption></figcaption></figure>



Além disso, o conteúdo que será mostrado na aplicação NÃO PODE estar em um workspace pessoal

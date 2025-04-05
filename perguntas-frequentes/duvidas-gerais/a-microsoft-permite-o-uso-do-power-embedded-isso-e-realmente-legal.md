# A Microsoft permite o uso do Power Embedded? Isso é realmente legal?

Com certeza, a Microsoft permite o uso do Power Embedded e é uma solução 100% legal. A Power Tuning é uma empresa Microsoft Solutions Partner desde 2018, e uma das líderes em vendas de Azure no Brasil e, portanto, tem um forte relacionamento com a Microsoft e a distribuidora TD Synnex, e em hipótese alguma iria desenvolver um produto que utilizasse alguma licença ilegal ou mecanismo que quebre o contrato de uso com a Microsoft.

### Conheça as formas corretas de incorporar relatórios

Antes de utilizar a tecnologia de [Análise integrada do Power BI](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-analytics-power-bi) para incorporar relatórios em portais e aplicações Web, seja para redução de custos, recursos avançados e personalização, você deve entender que existem 2 modelos de licenciamento:

* [Inserir para seus clientes](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-analytics-power-bi#embed-for-your-customers): Permite que você crie um aplicativo que utiliza um Service Principal para autenticar e interagir com os dados no Power BI. Seus usuários não precisam entrar usando credenciais do Power BI para ver o conteúdo inserido e o licenciamento ocorre contratando uma capacidade para licenciar os workspaces dos relatórios.
* [Inserir para a organização](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-analytics-power-bi#embed-for-your-organization): Permite que você crie um aplicativo que requer o uso de uma conta Pro do Power BI para cada usuário. Os usuários inscritos só podem consumir o conteúdo inserido aos quais eles têm acesso no serviço do Power BI.

| Inserir para seus clientes                                                                                                    | Inserir para a organização                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Também conhecida como **app owns data**                                                                                       | Também conhecida como **user owns data**                                                                                 |
| Modelo de licenciamento por capacidade, onde o workspace é associado à uma capacidade contratada pelo portal do Azure         | Modelo de licenciamento por usuário, onde o usuário que acessa o aplicativo tem uma licença do Power BI associada à ele. |
| Os usuários do aplicativo se autenticam com seu próprio método de autenticação, não exigindo que o usuário esteja no Entra ID | Os usuários do aplicativo se autenticam no Microsoft Entra ID da empresa                                                 |
| Os usuários do aplicativo não precisam de uma licença PRO ou PPU para visualizar relatórios                                   | Cada usuário do aplicativo precisa de uma licença PRO ou PPU do Power BI                                                 |
| Autenticação não interativa. Seu aplicativo usa uma _entidade de serviço_ ou um _usuário mestre_ para se autenticar           | Autenticação interativa. Seu aplicativo usa as credenciais do usuário do aplicativo para autenticar                      |

{% hint style="danger" %}
**Caso você esteja utilizando uma plataforma que utilize uma conta Pro para gerar os tokens de inserção de relatórios, sem utilizar uma capacidade para isso, você provavelmente está violando os termos de uso do Power BI e sua empresa pode sofrer multas e sanções pela Microsoft.**
{% endhint %}

### Azure Marketplace

O Power Embedded também está disponível para ser acessado e contratado pelo [Azure Marketplace](https://azuremarketplace.microsoft.com/pt-br/marketplace/apps/powertuningperformanceemdados1702567987391.powerembedded?tab=overview), o que indica um forte relacionamento com a Microsoft para suportar o produto

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/05/Power-Embedded-no-Marketplace-da-Microsoft.png" alt=""><figcaption></figcaption></figure>

### Perguntas e respostas da licença do Power BI Embedded

Falando sobre o licenciamento por capacidade, no [link abaixo](https://azure.microsoft.com/pt-br/pricing/details/power-bi-embedded/), a Microsoft deixa bem claro que os usuários que estão vendo o conteúdo publicado no Power BI Embedded não precisam de licenças do Power BI atribuídas a eles, portanto, não é necessária uma licença PRO para visualização dos relatórios através do Power Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/O-Power-Embedded-e-legal-Print-1-768x455.png" alt=""><figcaption></figcaption></figure>

### Microsoft Fabric também permite incorporar relatórios

Neste [link aqui](https://powerbi.microsoft.com/pt-br/blog/power-bi-embedded-with-microsoft-fabric/), a Microsoft mostra que o Microsoft Fabric também pode ser utilizado normalmente para inserir relatórios em aplicações terceiras, sem problema algum

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/O-Power-Embedded-e-legal-Print-3.png" alt=""><figcaption></figcaption></figure>

### Usuários podem criar/alterar relatórios pelo portal sem precisar de licença

Neste[ link abaixo](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#quem-precisa-de-uma-licen-a-power-bi-pro-ou-ppu--premium-por-usu-rio--para-o-power-bi-embedded-e-por-qu--), a Microsoft deixa explícito que alteração e criação de relatórios por meio de um portal que utilize o licenciamento do Power BI Embedded, não requer uma licença PRO ou PPU para isso, e por tanto, a alteração e criação de relatórios pelo Power Embedded é totalmente legal e suportada.

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/O-Power-Embedded-e-legal-Print-2-1024x439.png" alt=""><figcaption></figcaption></figure>

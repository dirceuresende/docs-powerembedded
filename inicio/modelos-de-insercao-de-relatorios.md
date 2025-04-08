# Modelos de inserção de relatórios

## Conheça as formas corretas de incorporar relatórios <a href="#conheca-as-formas-corretas-de-incorporar-relatorios" id="conheca-as-formas-corretas-de-incorporar-relatorios"></a>

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
**Caso você esteja utilizando uma plataforma que utilize uma conta Pro para gerar os tokens de inserção de relatórios, sem utilizar uma capacidade para isso, você provavelmente está violando os termos de uso do Power BI e sua empresa pode sofrer multas e sanções pela Microsoft. Saiba mais** [**clicando aqui neste link**](../perguntas-frequentes/licenciamento/posso-utilizar-o-power-bi-pro-ou-premium-por-usuario-para-embeddar.md)**.**
{% endhint %}



### 1) User Owns Data (Usuário é dono dos dados)

Este é o modelo mais simples e direto:

* Cada usuário final **se autentica no Power BI com sua própria conta corporativa** (via Entra ID).
* O aplicativo age como uma ponte, mas a experiência é personalizada por usuário.
* Cada usuário **precisa de uma licença Power BI Pro** (ou acesso a uma workspace em capacidade Premium).
* A aplicação apenas facilita o embed, mas **o acesso aos relatórios é controlado via Power BI**.



**Cenários típicos:**

* Aplicativos internos para colaboradores de uma empresa.
* Soluções corporativas que seguem políticas internas de segurança e identidade.



**Correto:**

* Usuários internos autenticados no Entra ID.
* Licenciamento Pro ou P SKU.
* RLS controlado no próprio Power BI.



**Errado:**

* Tentar usar User owns data com usuários externos.
* Compartilhar credenciais ou tokens manualmente.
* Ignorar licenciamento por usuário.



### **2) App Owns Data (Aplicativo é dono dos dados)**

Esse é o modelo ideal para **ISVs e soluções SaaS** como o Power Embedded:

* A aplicação **usa um Service Principal (ou Master Account)** para autenticar no Power BI, em nome de todos os usuários.
* Os usuários finais **não precisam de conta Power BI nem licença Pro**.
* Os relatórios são incorporados diretamente na interface da aplicação.
* O controle de permissões, RLS e visibilidade é feito **dentro da aplicação**, via token de incorporação.



## **Modelo do Power Embedded -** App Owns Data (multi-tenant)

Cada **cliente tem**:

* Seu **próprio tenant Microsoft Entra ID**
* Suas **capacidades Premium (Power BI Embedded ou Fabric)**
* Seus próprios **workspaces com relatórios, associados com 1 capacidade Premium**
* Um **service principal criado no tenant dele**, concedendo permissão somente aos workspaces usados no portal.



O Power Embedded (no tenant da ISV):

* Autentica usando o **client\_id + secret** do service principal do cliente
* Gera o **token de embed** com escopo mínimo
* **Aplica segurança e RLS** com base no banco de dados interno da ISV
* **Não possui controle ou hospedagem dos relatórios**, apenas os consome via API



Pontos importantes:

* Os **usuários são do próprio tenant deles** ou usuários externos, cadastrados por um administrador do portal via SSO ou métodos alternativos (Entra ID, Google, Email/senha, etc.).
* O **acesso aos relatórios é feito via autenticação não interativa**, conforme definido pela Microsoft para ISVs no modelo "inserir para seus clientes".
* A Power Tuning, como ISV, cria um **Service Principal diretamente dentro do tenant do cliente** (com consentimento deles), e o configura com as permissões adequadas para gerar o token de embed.
* O Power Embedded **atua como um middleware**, mas o acesso e o embed ocorrem usando o **Service Principal daquele tenant**, com capacidade vinculada àquele tenant.
* Mesmo que o portal seja multicliente, **cada tenant tem sua própria instância de embed isolada**, com seu próprio Service Principal e sua própria capacidade.
* Os usuários finais **não precisam de licenças Power BI Pro**, uma vez que os relatórios estão atribuídos a uma capacidade dedicada.
* Como o conteúdo e o Service Principal estão no **mesmo tenant do cliente**, não há violação do controle de dados nem do isolamento entre tenants.

#### ✅ Isso está 100% em conformidade com o modelo **"App owns data"**



## Erros comuns ao utilizar o modelo App Owns Data

{% hint style="warning" %}
Antes de utilizar a tecnologia de [Análise integrada do Power BI](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-analytics-power-bi) para incorporar relatórios em portais e aplicações Web, é bom entender quais as regras para que a solução esteja em conformidade com o licenciamento correto da Microsoft, para evitar violar os termos de uso do Power BI.
{% endhint %}

### **1) ISV com um único tenant, hospedando relatórios de clientes**

* Um único workspace por cliente **dentro do tenant da ISV**.
* Uma capacidade compartilhada entre todos.
* Service Principal controlado pela ISV.
* Acesso segmentado por RLS ou filtros.
* Nenhum controle real do cliente sobre seus relatórios.



**Risco:**

* Violação das regras de licenciamento.
* Possível infração contratual com a Microsoft.
* Pode levar à suspensão da conta pela Microsoft.
* Dados de múltiplos clientes sob controle de um único tenant = risco de segurança e privacidade.



### **2) Uso de Master Account para todos os relatórios:**

* A aplicação usa uma conta "genérica" com licença Pro para gerar embed tokens.
* Não utiliza Service Principal.
* Não há uso de capacidade Premium.
* Usuários finais acessam sem licença.



**Risco:**

* **Totalmente fora do modelo suportado atualmente.**
* Prática obsoleta e não recomendada pela Microsoft.
* Altamente arriscado para escalabilidade, segurança e compliance.
* Inviável para escala ou auditoria.
* Não é suportado oficialmente.
* Pode levar à suspensão da conta.

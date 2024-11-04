# Trial do Fabric

Para facilitar o processo de instalação do Power Embedded, criamos este tutorial para auxiliar nossos clientes a realizar a instalação do Power Embedded.

### Pré-requisitos para realizar a instalação

Como o Power Embedded é um sistema no formato SaaS, você não precisará contratar ou gerenciar nenhum servidor, aplicação ou banco de dados, irá apenas utilizar o software como um serviço.

Para configurar o Power Embedded na sua empresa, precisamos que os seguintes pré-requisitos sejam atendidos antes de agendarmos a instalação:

* Conta de um usuário do Azure com permissão para criar a capacidade Fabric ou Embedded.
* Conta de um usuário do Azure com permissão para criar grupos e registros de aplicativos no Azure AD.
* Conta de um usuário do Azure que possua a role “Fabric administrator” para acessar o [portal de administração do Power BI.](https://app.powerbi.com/admin-portal/tenantSettings)

Durante a reunião de instalação do sistema, que é feita junto com o cliente, precisamos que seja fornecido um usuário com as permissões listadas acima, ou que tenha alguma pessoa do time do cliente, com essas permissões, que possa compartilhar a tela e executar as ações que serão instruídas.



### Como criar o aplicativo do Power Embedded no Azure AD

Para registrar o de aplicativo que será utilizado pelo Power Embedded, você precisará acessar [esse link aqui](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/\~/RegisteredApps).

Na tela abaixo, clique no botão “New registration

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-3.png" alt=""><figcaption></figcaption></figure>

</div>

Agora você deverá escolher um nome para o aplicativo que irá criar no seu Azure AD. O nome fica a seu critério.

Após isso, clique no botão “Register”, no final da página

<div data-full-width="false">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-5.png" alt=""><figcaption></figcaption></figure>

</div>

Após a criação desse Aplicativo, você será direcionado para a tela de visão geral desse usuário.

Copie o valor do campo “Application (client) ID” e salve em um bloco de notas. Essa chave é o que você irá colar no campo “**Id do Cliente do Power BI**” na configuração da organização do Power Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-6.png" alt=""><figcaption></figcaption></figure>

Agora clique na opção “Certificates & secrets” e em seguida, clique no botão “New client secret

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-7.png" alt=""><figcaption></figcaption></figure>

Na nova tela aberta, digite uma descrição para esse segredo (conforme a sua preferência) e selecione a validade deste segredo.

Sugiro escolher 24 meses para só precisar se preocupar com essa expiração depois de 2 anos (Sim, após o prazo escolhido, esse segredo irá expirar e o sistema irá PARAR de funcionar. Você precisará gerar um novo segredo e atualizar no Power Embedded).

Agora clique no botão “Add”, no final da página

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-8.png" alt=""><figcaption></figcaption></figure>

Agora copie o campo “Value” gerado. Existe um botão de copiar ao lado dessa chave.

Anote e guarde bem essa chave, pois essa será a ÚNICA vez que você poderá vê-la. Caso você perca essa chave, não será possível recuperá-la: Você precisará gerar um novo segredo e atualizar no sistema.

Esse valor que destaquei e você copiou, você deverá colar no campo “**Chave de Acesso do Cliente do Power BI**” da tela de configuração do Power Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-9.png" alt=""><figcaption></figcaption></figure>



### Sincronizar usuários e grupos do Azure AD (Entra ID)

Para integrar o Power Embedded com o Azure AD (Entra ID) e importar os usuários e grupos.

Na mesma tela de registro de aplicativos, clique em “API permissions” e em “Add a Permission”.

![](https://powerembedded.com.br/wp-content/uploads/2024/07/Permissoes-de-APIS.png)

Na próxima tela selecione a opção do “Microsoft Graph”.

![](https://powerembedded.com.br/wp-content/uploads/2024/07/Permissoes-aplicativo.png)

Em seguida seleciona a opção de “Application permissions”.

![](https://powerembedded.com.br/wp-content/uploads/2024/07/Microsoft-Graph.png)

Na aba a seguir, busque por “Directory” e selecione a primeira opção “Directory.Read.All” e clique em “Add permissions”.

![](https://powerembedded.com.br/wp-content/uploads/2024/07/Directory-1.png)

Para finalizar basta conceder o consentimento do administrador clicando em “Grant admin consent for”.

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/07/Conssentimento-admin.png" alt=""><figcaption></figcaption></figure>

Pronto, quando finalizar as próximas etapas já conseguirá importar os usuários e grupos do Azure AD (Entra ID) para o Power Embedded.



### Adicionando o usuário do Power Embedded a um novo grupo do AD

Para liberar permissões no Portal de Administração do Power BI para o Service Principal que você acabou de criar, ele obrigatoriamente precisa fazer parte de um grupo de segurança do Azure AD (Entra ID).

Para fazer isso, acesse [este link aqui](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/GroupsManagementMenuBlade/\~/AllGroups) e clique no botão “New group”

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-11.png" alt=""><figcaption></figcaption></figure>

Selecione a opção “Security” no campo “Group type” e digite um nome à sua preferência para esse grupo que estamos criando.

Clique no link “Owners” e adicione as pessoas que ficarão responsáveis pelo Power Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-12.png" alt=""><figcaption></figcaption></figure>

Clique no link “No members selected” da categoria “Members”

Na tela que foi aberta, digite o nome do Service Principal que você criou para filtrar. Selecione o Service Principal na lista e clique no botão “Select”, no final da página

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-13.png" alt=""><figcaption></figcaption></figure>

Agora que você selecionou o membro para adicionar à este novo grupo, clique no botão “Create”, no final da página

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-14.png" alt=""><figcaption></figcaption></figure>



### Como liberar as permissões necessárias no Portal de Administração do Power BI

Utilizando um usuário com permissão de administrador do Power BI, acesse [este link aqui](https://app.powerbi.com/admin-portal/tenantSettings).

Desça a página até encontrar a seção **“Configurações do Desenvolvedor”** (ou busque por **“api”** na barra de busca à direita

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric.png" alt=""><figcaption></figcaption></figure>

Marque a opção **“As entidades de serviço podem usar APIs do Fabric”**.

Por questões de segurança, marque a opção **“Especificar grupos de segurança”** na seção “Aplicar em:” e selecione o grupo de segurança que criamos no começo deste tópico (no meu caso, “PowerEmbedded-Group”

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric2.png" alt=""><figcaption></figcaption></figure>

Clique no botão “Aplicar”.

Desça mais um pouco a página e repita o mesmo processo para o item **“As entidades de serviço podem acessar APIs de administrador somente leitura”** e **“Aprimorar as respostas das APIs de administração com metadados detalhados”**, na seção **“Configurações da API de Administração”**

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric5.png" alt=""><figcaption></figcaption></figure>

Atualize a página e agora a opção _**“Aprimorar as respostas das APIs de administração com as expressões DAX e mashup”**_ vai ficar disponível para ser marcada. Repita o mesmo processo para essa permissão.

Ainda na categoria **“Configurações do desenvolvedor”**, ou pesquisando por “inserir” na barra de busca, marque a opção **“Inserir conteúdo em aplicativos”** e adicione o grupo de segurança que você criou no filtro “Grupos de segurança específicos”, na opção “Aplicar em”.

Caso essa configuração já esteja ativada e permitida para toda a organização, que é o padrão do Power BI, pode deixar assim, caso o cliente concorde. Alterar isso pode causar problemas em outros processos, caso estejam utilizando algo que necessite dessa permissão

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric4.png" alt=""><figcaption></figcaption></figure>

Agora, na categoria **" Configurações de compartilhamento e de exportação"**, ou pesquisando por **"exportar"** na barra de busca, marque a opção **"Exportar os relatórios como arquivos de imagens"**, e clique em "aplicar".

Caso essa configuração já esteja ativada, pode deixar assim. Essa configuração permite a exportação dos dados como  imagem (PNG) no portal de Visualizações.&#x20;



E por último, na seção **“Configurações de integração”**, faça o mesmo processo para a configuração **“Permitir pontos de extremidade XMLA e analisar no Excel com modelos semânticos locais”**, que serve para permitir a listagem das roles de RLS de forma automática.

Caso essa configuração já esteja ativada e permitida para toda a organização, que é o padrão do Power BI, pode deixar assim, caso o cliente concorde. Alterar isso pode causar problemas em outros processos, caso estejam utilizando algo que necessite dessa permissão

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/05/Power-Embedded-Instalacao-Permitir-pontos-de-extremidade-XMLA-e-analisar-no-Excel-com-modelos-semanticos-locais-2.png" alt=""><figcaption></figcaption></figure>

Pronto! Agora o Portal possui acesso ao seu ambiente do Power BI.



### Primeiro acesso ao Portal Administrativo

Acesse a área administrativa do Portal, acessando [esse link aqui](https://admin.powerembedded.com.br/), logado com um usuário com permissão de **“Administrador Global do Azure”**.

Você irá autenticar na sua conta Microsoft e assim que terminar de logar, verá uma tela de solicitação de permissão no seu Azure AD.

**Marque a opção “Consent on behalf of your organization” e clique no botão “Accept”**

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-4.png" alt=""><figcaption></figcaption></figure>

Esqueceu de marcar a opção “Consent on behalf of your organization” ou fez a instalação com uma conta que não era administrador?

<details>

<summary>Clique aqui para visualizar como liberar essa permissão manualmente</summary>

Caso você tenha acessado o portal de administração utilizando um usuário sem as permissões necessárias, a tela acima talvez não apareça para você, e apareça, na verdade, a tela abaixo, quando você ou outro usuário tentar logar na área administrativa

<img src="https://powerembedded.com.br/wp-content/uploads/2023/10/Enterprise-Application-Consentir-App-como-Administrador.png" alt="" data-size="original">

Se isso acontecer, você precisará autorizar a aplicação do Power Embedded (powerportal.cloud) em nome da organização, utilizando um usuário com permissões globais no Azure AD.

Para fazer isso, clique no link “[Enterprise Applications](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/StartboardApplicationsMenuBlade/\~/AppAppsPreview/menuId\~/null)” do Azure AD (Entra ID

<img src="https://powerembedded.com.br/wp-content/uploads/2023/10/Aplicativos-empresariais.png" alt="" data-size="original">

Localize e clique no aplicativo “powerportal.cloud”

[![](https://powerembedded.com.br/wp-content/uploads/2023/10/Aplicativos-empresariais-powerportal.cloud\_.png)](https://powerembedded.com.br/wp-content/uploads/2023/10/Aplicativos-empresariais-powerportal.cloud\_.png)

Clique no menu “Permissão” no painel da esquerda e depois clique no botão “Conceder consentimento do administador para …” e autorize a aplicação.

[![](https://powerembedded.com.br/wp-content/uploads/2023/10/Aplicativos-empresariais-Permissoes-powerportal.cloud\_.png)](https://powerembedded.com.br/wp-content/uploads/2023/10/Aplicativos-empresariais-Permissoes-powerportal.cloud\_.png)

</details>

Após confirmar as permissões, você será direcionado para o sistema e deverá criar a nova organização

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-2.png" alt=""><figcaption></figcaption></figure>

Nesta tela, você poderá configurar as seguintes configurações:

* **Nome:** É o nome da sua empresa. O sistema irá recuperar o nome cadastrado no Tenant do Azure, mas você poderá alterá-lo nesta tela ou futuramente, pela página de configurações do sistema.
* **Id do Cliente do Power BI:** É o ID do Service Principal que será criado para integrar o Power Embedded com o seu Azure Active Directory (vamos explicar mais sobre isso logo abaixo).
* **Chave de Acesso do Cliente do Power BI:** É o segredo gerado para o Service Principal (vamos explicar mais sobre isso logo abaixo).
* **Domínio Customizado:** É o domínio da sua empresa (sem www ou https). Esse campo será utilizado para criar uma URL de acesso personalizada de acesso aos relatórios (ex: relatorios.suaempresa.com.br)

Com o Client ID e o Secret Value que você obteve no início da instalação e anotou em um bloco de notas, agora vamos utilizá-los na tela de configuração da organização do Power Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/08/Manual-de-Instalacao-do-Power-Embedded-10-1.png" alt=""><figcaption></figcaption></figure>

Clique no botão “Criar Organização” e você já poderá começar a usar o Portal.



### Como integrar o Portal ao Workspace do Power BI?

Para que seja possível importar os relatórios do Power BI para o Power Embedded, você precisará fazer duas coisas no workspace:

1. Ativar o período de avaliação do Fabric (caso ainda não tenha feito).
2. Alterar a capacidade do Workspace para capacidade Fabric.
3. Adicionar o Service Principal criado (usuário do Power Embedded) como administrador dos workspaces que você quer importar relatórios (pode ser mais de 1).

Para ativar o período de avaliação do Fabric, clique na sua foto no menu do Power B

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric11.png" alt=""><figcaption></figcaption></figure>

Vale lembrar que apenas 6 pessoas na organização podem ter iniciado a avaliação do Fabric, e uma vez que a pessoa já ativou o trial, não é possível realocar essa capacidade para outra pessoa.

Para alterar a capacidade do Workspace para capacidade Premium (Fabric), acesse o workspace, clique nos 3 pontinhos e selecione a opção “Configurações do Workspace

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric6.png" alt=""><figcaption></figcaption></figure>

Na tela que foi aberta, clique no menu “Premium”, depois escolha a licença “Embedded” e no campo “Modo de licença”, selecione o recurso “Avaliação”.

Clique no botão “Aplicar”, logo mais abaixo

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric7.png" alt=""><figcaption></figcaption></figure>

A partir desse momento, esse workspace agora está na capacidade Premium do Fabric. Caso você pause esse recurso, o Workspace ficará inacessível, mesmo utilizando uma conta Pro e acessando direto pelo portal.

O último passo agora é adicionar o usuário do Service Principal ao Workspace.

Para adicionar o Service Principal criado como administrador de um workspace, acesse o workspace, clique nos 3 pontinhos e selecione a opção “Gerenciar acesso

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric8.png" alt=""><figcaption></figcaption></figure>

Clique no botão “+ Adicionar pessoas ou grupos”

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric9.png" alt=""><figcaption></figcaption></figure>

Pesquise pelo nome do aplicativo que foi criado anteriormente (PowerEmbedded-App) e lembre de alterar o nível de acesso para “Administrador”. Após isso, clique no botão “Add”

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/03/Habilitar-Power-Embedded-no-Fabric10.png" alt=""><figcaption></figcaption></figure>



Pronto! Agora o Power Embedded já possui acesso nesse workspace. Repita isso para todos os Workspaces que você quer importar relatórios.

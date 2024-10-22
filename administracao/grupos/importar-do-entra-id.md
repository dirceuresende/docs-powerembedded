# Importar do Entra ID

Essa opção irá permitir que você possa importar os grupos diretamente do Entra ID do Azure (antigo Azure AD) para o Power Embedded.

O sistema exibirá uma lista dos grupos existentes no Entra ID da sua empresa.

Você irá selecionar os grupos que deseja importar e esses grupos serão automaticamente adicionados ao Power Embedded.

Há também uma opção no rodapé desta página de incluir os usuários do grupo. Ao marcar essa opção, todos os usuários dos grupos que estão sendo importados serão importados e associados aos respectivos grupos, conforme associação que já existe no Entra ID.

<figure><img src="../../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>



### Requisitos para a integração com Entra ID

Para integrar o Power Embedded com o Azure AD (Entra ID) e importar os usuários e grupos, acesse a tela de [Registros de aplicativos](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/\~/RegisteredApps).

Pesquise pelo aplicativo do Power Embedded (PowerEmbedded-App), clique em “API permissions” e em “Add a Permission”.

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

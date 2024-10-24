# Importar do Entra ID

Essa opção irá permitir que você possa importar os usuários diretamente do Entra ID do Azure (antigo Azure AD) para o Power Embedded.

O sistema exibirá uma lista dos usuários existentes no Entra ID da sua empresa.

Você irá selecionar os usuários que deseja importar, e esses e-mails serão automaticamente adicionados ao Power Embedded, onde todos os usuários serão criados como o perfil de **visualizadores** por padrão.

Há também uma opção no rodapé desta página de incluir os grupos do ID. Ao marcar essa opção, todos os grupos em que o usuário está inserido na organização da empresa serão importados e associados ao usuário.

{% hint style="warning" %}
Observação: Caso o usuário esteja em muitos grupos, essa ação pode acabar gerando uma dificuldade de organização para o seu ambiente dentro do Power Embedded, uma vez que terão muitos grupos cadastrados.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Se você quiser sincronizar os grupos e seus usuários de forma automática ao invés de uma importação pontual, leia o artigo [Sincronizar Grupos com Entra ID](../grupos/sincronizar-com-entra-id.md).



Se você não quiser sincronizar os grupos, mas apenas realizar uma importação pontual de grupos e seus usuários, leia o artigo [Importar Grupos do Entra ID](../grupos/importar-do-entra-id.md).
{% endhint %}



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

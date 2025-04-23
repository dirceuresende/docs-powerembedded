# Sincronizar com Entra ID

A sincronização automática de grupos do Entra ID aprimora a governança de usuários ao sincronizar automaticamente os grupos locais do Power Embedded com os grupos que estão do Entra ID.

Esta funcionalidade permite que o time de segurança, service desk ou infraestrutura gerencie as associações de usuários e grupos diretamente pelo Entra ID, sem a necessidade de ter permissão no Power Embedded, e essas alterações irão refletir no sistema automaticamente.

No Power Embedded, já era possível criar grupos e também importá-los a partir de arquivos CSV ou do Entra ID ou de forma programática através da API, acelerando bastante o processo de importação dos usuários e grupos.

No entanto, essas opções exigem alguma ação manual do usuário ou que você crie uma integração utilizando programação (no caso da API).

A sincronização é uma funcionalidade que permite realizar essa sincronia com os dados do Entra ID de forma simples e automática, facilitando a gestão da segurança, RLS e permissões.

<figure><img src="../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Se você não quiser sincronizar os grupos, mas apenas realizar uma importação pontual de grupos e seus usuários, leia o artigo [Importar Grupos do Entra ID](importar-do-entra-id.md).



Se você quiser importar alguns usuários pontualmente, ao invés de importar ou sincronizar um grupo, leia o artigo [Importar Usuário do Entra ID](../usuarios/importar-do-entra-id.md).
{% endhint %}



### Como configurar a sincronização automática com o Entra ID

Para que a sincronização de grupos com o Entra ID funcione corretamente, você precisará definir qual o comportamento do sistema no momento do sincronismo.

Para configurar o comportamento da sincronização, acesse o menu “**Configurações”** > Aba “**Integrações”** > **Sincronização de grupos com Entra ID**.

<figure><img src="../../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure>

A seguir, explicaremos detalhadamente o que cada permissão significa e como ela afeta o processo de sincronização:

**Criar usuário no sistema ao ser adicionado aos grupos sincronizados:** Esta permissão é responsável por cadastrar automaticamente no Power Embedded e associar aos respectivos grupos no sistema, os usuários que são adicionados a grupos sincronizados no Entra ID. Se essa permissão estiver desativada, os novos usuários criados no Entra ID não serão adicionados ao sistema automaticamente.

\
**O que fazer quando um usuário for removido de um grupo sincronizado no Entra ID?**\
Existem quatro opções para definir o que o sistema irá fazer quando um usuário for removido de um grupo que está sincronizado com o Entra ID, e entender cada uma delas é crucial para um aproveitamento eficaz da funcionalidade:

1. **Desabilitado:** Esta é a opção padrão do sistema, e caso ela esteja marcada, remover o usuário do grupo sincronizado no Entra ID não terá nenhum efeito no Power Embedded.
2. **Excluir o usuário do sistema:** Quando um usuário é removido de um grupo do Entra ID, ele será automaticamente removido desse mesmo grupo no Power Embedded. Se o usuário ainda fizer parte de algum outro grupo sincronizado, o sistema irá apenas retirá-lo dos grupos do Power Embedded que o usuário não faz mais parte no Entra ID. Se o usuário não fizer mais parte de nenhum grupo sincronizado, ele será removido permanentemente do sistema, incluindo suas configurações e permissões.
3. **Bloquear o usuário do sistema:** Quando um usuário é removido de um grupo do Entra ID, ele será automaticamente removido desse mesmo grupo no Power Embedded. Se o usuário ainda fizer parte de algum outro grupo sincronizado, o sistema irá apenas retirá-lo dos grupos do Power Embedded que o usuário não faz mais parte no Entra ID. Se o usuário não fizer mais parte de nenhum grupo sincronizado, ele será bloqueado no sistema, impedindo o seu acesso, mas mantendo ainda as permissões e configurações. Essa é uma opção mais conservadora do que a exclusão, garantindo uma fácil recuperação (basta desbloquear o usuário) em caso de algum erro na remoção do usuário no grupo do Entra ID.
4. **Retirar o usuário do grupo no sistema:** Quando um usuário é removido de um grupo do Entra ID, ele continua cadastrado no portal, mas é removido apenas do grupo específico do qual ele foi retirado no Entra ID. Diferente das outras opções, o usuário permanece ativo no portal, porém sem associação com o grupo do qual foi removido.

&#x20;

A sincronização no portal é feita automaticamente uma vez ao dia. No entanto, se for necessário forçar essa sincronização, é possível fazê-lo de duas formas:

1. Clicando no botão “Sincronizar Agora” para sincronizar todos os grupos
2. Escolher um grupo específico, clicar no botão “Ações” e depois no botão “Sincronizar”, para sincronizar apenas o grupo selecionado.



### Como sincronizar grupos com o Entra ID

Para que a sincronização ocorra de fato, é necessário selecionar quais grupos você deseja sincronizar.

**Passo 1:** Acesse a tela de “Grupos”\
**Passo 2:** Clique no botão “Sincronizar”\
**Passo 3:** Na tela de “Grupos sincronizados com o Entra ID”, clique no botão “Adicionar Grupos”\
**Passo 4:** Serão listados todos os grupos do Entra ID. Selecione um ou mais grupos que deseja sincronizar e salve.

<figure><img src="../../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure>



### Regras de Funcionamento do Sincronismo Automático

1. A sincronização só será executada caso você tenha ativado a criação automática de usuários OU tenha configurado alguma ação para executar quando o usuário for removido do Entra ID, que não seja a opção “Desabilitado”.
2. Se o grupo selecionado para sincronizar não existir no Power Embedded, ele será criado automaticamente no sistema.
3. Caso já exista um grupo no sistema com esse mesmo nome que foi selecionado para a sincronização com o Entra ID, esse grupo será incluído na sincronização. Se algum usuário fizer parte desse grupo no Power Embedded e que não fizer parte desse grupo no Entra ID, ele será removido do grupo no Power Embedded, podendo ser até bloqueado ou removido do sistema, dependendo das configurações do sincronismo.
4. A sincronização automática é executada diariamente, às 22h.



### Permissões para a importação de dados do Entra ID

Para ser possível importar dados de usuários e grupos do Entra ID, é necessário atribuir algumas permissões para o Service Principal, criado no Portal do Azure, utilizado pelo Power Embedded para se comunicar com o seu ambiente.

Na tela de [Registro de aplicativos](https://portal.azure.com/#view/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/~/RegisteredApps), pesquise pelo nome do aplicativo criado (O nome padrão é PowerEmbedded-App).

Na tela do aplicativo, clique em _**API permissions**_, no menu lateral e depois em _**Add a Permission**_.

<figure><img src="../../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure>

Na próxima tela selecione a opção do _**Microsoft Graph**_.

<figure><img src="../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>

Em seguida selecione a opção de _**Application permissions**_.

<figure><img src="../../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure>

Na aba a seguir, busque por _**Directory**_ e selecione a primeira opção _**Directory.Read.All**_ e clique em _**Add permissions**_.

<figure><img src="../../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>

Caso queira utilizar uma permissão menos privilegiada, pode liberar apenas as permissões "User.Read.All" e "Group.Read.All".

<figure><img src="../../.gitbook/assets/image (434).png" alt=""><figcaption></figcaption></figure>

Para finalizar basta conceder o consentimento do administrador clicando em _**Grant admin consent for**_.

<figure><img src="../../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure>

Pronto, agora você já conseguirá importar os usuários e grupos do Azure AD (Entra ID) para o Power Embedded.

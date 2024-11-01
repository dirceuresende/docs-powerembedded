# Migração

Para simplificar a configuração do Power Embedded, preparamos um script que automatiza o processo de importação de usuários, RLS e relatórios do Power BI para o Power Embedded de forma simples e fácil.

## Requisitos

Para conseguir executar o processo de migração é importante está com as seguintes permissões habilitadas:



<details>

<summary>Permissão de admin do usuário de serviço</summary>

Para adicionar o Service Principal criado como administrador de um workspace, acesse o workspace, clique nos 3 pontinhos e selecione a opção “Gerenciar acesso

<img src="../.gitbook/assets/app 1.png" alt="" data-size="original">

Clique no botão “+ Adicionar pessoas ou grupos”

<img src="../.gitbook/assets/app 2.png" alt="" data-size="original">

Pesquise pelo nome do aplicativo que foi criado anteriormente (PowerEmbedded-App) e lembre de alterar o nível de acesso para “Administrador”. Após isso, clique no botão “Add”

<img src="../.gitbook/assets/app 3.png" alt="" data-size="original">



Pronto! Agora o Power Embedded já possui acesso nesse workspace. Repita isso para todos os Workspaces que você quer importar relatórios.

</details>

<details>

<summary>Permissões Leitura API</summary>

Permissões para a importação de dados do Entra ID

Para ser possível importar dados de usuários e grupos do Entra ID, é necessário atribuir algumas permissões para o Service Principal, criado no Portal do Azure, utilizado pelo Power Embedded para se comunicar com o seu ambiente.

Na tela de [Registro de aplicativos](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/\~/RegisteredApps), pesquise pelo nome do aplicativo criado (O nome padrão é PowerEmbedded-App).

Na tela do aplicativo, clique em _API permissions_, no menu lateral e depois em _Add a Permission_.

<img src="../.gitbook/assets/sin 1 small.png" alt="" data-size="original">

Na próxima tela selecione a opção do _Microsoft Graph_.

<img src="../.gitbook/assets/sinc 2 small.png" alt="" data-size="original">



Em seguida selecione a opção de _Application permissions_.

<img src="../.gitbook/assets/sinc small 3.png" alt="" data-size="original">

Na aba a seguir, busque por _Directory_ e selecione a primeira opção _Directory.Read.All_ e clique em _Add permissions_.

<img src="../.gitbook/assets/sinc small 4.png" alt="" data-size="original">

Para finalizar basta conceder o consentimento do administrador clicando em _Grant admin consent for_.

<img src="../.gitbook/assets/Screenshot 2024-10-29 164709.png" alt="" data-size="original">

Pronto, agora você já conseguirá importar os usuários e grupos do Azure AD (Entra ID) para o Power Embedded.

</details>

## Instruções

Com as devidas permissões habilitadas agora é só seguir o passo a passo de processo.

Vá ao portal de administração do Power Embedded no menu de migração, siga estas etapas. Nesse menu siga as instruções abaixo.

**Etapa 1:** Gere os tokens de acesso utilizando o botão abaixo e copie. O token gerado será válido por apenas 1 hora.

<figure><img src="../.gitbook/assets/image (382).png" alt=""><figcaption></figcaption></figure>

**Etapa 2:** Abra o script PowerShell disponível neste [\[link aqui\]](https://admin.powerembedded.com.br/powershell/migrationtool.txt), copie e cole no Power Shell

**Etapa 3**: Substitua as variáveis do script pelos respectivos valores

<figure><img src="../.gitbook/assets/image (383).png" alt=""><figcaption></figcaption></figure>

**ID de Cliente do Power BI**: Acesse o Portal de Administração do Power BI Embedded > Configurações > campo “ID de Cliente do Power BI”.

<figure><img src="../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure>

**Chave de API**: Acesse o Portal de Administração do Power BI Embedded > Configurações > campo “Chave de API” (clique no ícone em vermelho para gerar a chave).

<figure><img src="../.gitbook/assets/image (385).png" alt=""><figcaption></figcaption></figure>

**Pbi Token:** Chave Gerada no menu de migração

<figure><img src="../.gitbook/assets/pbi.png" alt=""><figcaption></figcaption></figure>

**Ad Token :** Chave gerada no menu de migração.

<figure><img src="../.gitbook/assets/ad.png" alt=""><figcaption></figcaption></figure>

Com os compos preenchidos agora é só rodar o código no Power Shell.

<figure><img src="../.gitbook/assets/print 8.png" alt=""><figcaption></figcaption></figure>

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

# A senha do usuário de serviço do Power BI expirou

<div align="left">

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

</div>

Durante a [instalação do Power Embedded](../../documentacao-tecnica/instalacao/trial-do-fabric.md), uma das etapas era a criação de um usuário de serviço na [página do Entra ID](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/\~/RegisteredApps), no portal do Azure, que faz a comunicação entre o sistema e o Power BI, e foi configurado um tempo de vencimento para a senha deste usuário.

Quando essa senha expira, é quando o erro acima aparece no Power Embedded, pois não está sendo mais possível estabelecer essa comunicação.

Caso isso tenha acontecido, siga esses 6 passos abaixo para criação de uma nova senha do usuário de serviço.



### **1. Acessar o Registro de aplicativos no Entra ID**

Para criar uma nova senha de aplicativo que será utilizado pelo Power Embedded, você precisará acessar [esse link aqui](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/\~/RegisteredApps).



### **2. Localizar o usuário utilizado no Power Embedded**

Na página de registro de aplicativos na aba “Todos os aplicativos” (All applications), busque pelo usuário criado no momento da instalação do Power Embedded (O nome padrão do usuário é “PowerEmbedded-App”).

Ao encontrar, clique no nome do aplicativo.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Caso você NÃO esteja utilizando o nome padrão do usuário (PowerEmbedded-App) e não se lembra qual é o nome do usuário que está utilizando, acesse a página de Configurações do Power Embedded, copie o ID que está no campo "Id de Cliente do Power BI" e pesquise por esse ID ao invés de pesquisar pelo nome do aplicativo.
{% endhint %}



### **3. Acessar a página de certificados e segredos**

Agora clique em “Certificados e segredos” (Certificates & secrets) e em seguida “Novo segredo do cliente” (New client secret) para gerar uma nova senha.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>



### **4. Gerar um novo segredo (senha)**

Na nova tela aberta, digite uma descrição para esse segredo (conforme a sua preferência) e selecione a validade deste segredo (o recomendado são 24 meses).

Agora clique no botão “Adicionar” (Add), no final da página.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>



### 5. Copiar e salvar a senha gerada

Agora copie o a senha gerada que está na coluna **“Valor”**. Existe um botão de copiar ao lado dessa chave.

{% hint style="warning" %}
Anote e guarde bem essa chave, pois essa será a ÚNICA vez que você poderá vê-la. Caso você perca essa chave, não será possível recuperá-la: Você precisará gerar um novo segredo e atualizar no sistema novamente.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>



### **6. Atualizar a senha no Power Embedded**

Com esse valor copiado, vá até o portal de administração do Power Embedded em Configurações, e cole no campo “Chave de Acesso do Cliente do Power Bi” e depois, clique no botão “Salvar”.

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Ao fazer esse processo, o portal irá funcionar normalmente.

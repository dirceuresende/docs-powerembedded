# Alterar senha do aplicativo

### Erro de senha expirada ou ao validar token de acesso

Se você encontrou o erro abaixo ao tentar acessar o portal de administração ou um erro relacionado à senha do usuário de serviço do Power BI no portal de relatórios, não se preocupe. Isso ocorreu porque a senha do usuário de serviço do Power BI expirou ou foi alterada no portal do Azure.

Para resolver o problema, basta gerar uma nova senha no portal do Azure e atualizar a senha na tela de configurações do Power Embedded.

Siga o passo a passo abaixo para concluir o processo:

<figure><img src="../../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>



Outra mensagem de erro bem comum é quando a senha expira. Quando um usuário tentar abrir um relatório no portal de visualização, irá ver a mensagem de erro abaixo:

<div align="left">

<figure><img src="../../../.gitbook/assets/image (193).png" alt=""><figcaption><p>A senha do usuário de serviço do Power BI, que utiliza o aplicativo 'abc123' expirou.</p></figcaption></figure>

</div>



Para concluir esse processo, você precisará realizar estes passos abaixo:

1. Acesse o portal do Azure [clique nesse link](https://portal.azure.com/#view/Microsoft\_AAD\_IAM/ActiveDirectoryMenuBlade/\~/RegisteredApps)
2. Pesquise pelo aplicativo do Power Embedded (PowerEmbedded-App)
3. Clique no item "Certificados & segredos" no menu lateral e depois clique em "Novo segredo do cliente"
4. Defina uma descrição e a data de expiração dessa chave
5. Copie essa nova chave e guarde-o com segurança em um cofre de senhas, pois não será possível recuperá-la novamente
6. No Power Embedded, acessa a página de "Configurações", cole o valor copiado no campo “Chave de Acesso do Cliente” e clique em Salvar.



### Como criar a senha do aplicativo no portal do Azure

**Passo 1:** Com o portal do Azure aberto, na tela inicial, vá para ‘App registrations’ e procure pelo usuário criado durante a instalação.

Por padrão, o nome sugerido é **PowerEmbedded-App**. Clique sobre ele ao encontrá-lo.

<figure><img src="../../../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>

**Passo 2:** Nessa tela, clique em **“Certificates & secrets”** e em seguida clique em **“New client secret”** para criar um novo segredo do cliente.

<figure><img src="../../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>



**Passo 3:** Na nova tela aberta, digite uma descrição para esse segredo (conforme a sua preferência) e selecione a validade deste segredo.

_A recomendação é escolher 24 meses para só precisar se preocupar com essa expiração depois de 2 anos (Sim, após o prazo escolhido, esse segredo irá expirar e o sistema irá PARAR de funcionar. Você precisará gerar um novo segredo e atualizar no Power Embedded)._

Agora clique no botão **Adicionar (Add)**, no final da página.

<figure><img src="../../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

**Passo 4:** Agora copie o campo “Value” gerado. Existe um botão de copiar ao lado dessa chave.

Anote e guarde bem essa chave, pois essa será a ÚNICA vez que você poderá vê-la. Caso você perca essa chave, não será possível recuperá-la: Você precisará gerar um novo segredo e atualizar no sistema.

Esse valor que destaquei e você copiou, você deverá colar no campo “**Chave de Acesso do Cliente do Power BI**” da tela de configuração do Power Embedded.

<figure><img src="../../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>



### Configurando a senha do aplicativo no Power Embedded

**Passo 5:** Vá ao portal de administração e adicione o valor copiado no campo **“Chave de Acesso do Cliente do Power BI”.**

<figure><img src="../../../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

Feito isso o portal irá voltar a funcionar normalmente.

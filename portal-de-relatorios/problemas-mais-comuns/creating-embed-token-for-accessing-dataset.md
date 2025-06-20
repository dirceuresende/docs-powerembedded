---
description: >-
  Esse erro normalmente ocorre quando o seu relatório está conectado ao Azure
  Analysis Services. Abaixo, apresentamos uma documentação com um passo a passo
  para ajudá-lo a resolver esse problema.
---

# Creating embed token for accessing dataset

<figure><img src="../../.gitbook/assets/Erro.png" alt=""><figcaption></figcaption></figure>

#### Passo 1: Conectar ao Servidor via SSMS

**1.1. Obter o Server Name**

1. Acesse o **Azure Portal**.
2. Vá até o recurso **Azure Analysis Services**.
3. No menu **Overview**, copie o **Server Name**.

<figure><img src="../../.gitbook/assets/AAS - Azure.png" alt=""><figcaption></figcaption></figure>

**1.2. Conectar no SSMS**

1. Abra o **SQL Server Management Studio (SSMS)**.
2. Clique em **Conectar** e selecione a opção **Analysis Services**.

<figure><img src="../../.gitbook/assets/SSMS - Conect.png" alt=""><figcaption></figcaption></figure>

3. No campo **Server Name**, cole o valor copiado anteriormente, Insira suas credenciais no campo **Username** e clique em **Conectar**.

<figure><img src="../../.gitbook/assets/Server name.png" alt=""><figcaption></figcaption></figure>

**1.3. Adicionar o Service Principal**

1. Após a conexão, clique com o botão direito sobre o servidor e selecione **Propriedades**.

<figure><img src="../../.gitbook/assets/Properties.png" alt=""><figcaption></figcaption></figure>

2. Na nova janela, vá até a guia **Segurança e** Clique em **Add** para adicionar um **Service Principal**.

<figure><img src="../../.gitbook/assets/security.png" alt=""><figcaption></figcaption></figure>

3. Em **Manual Entry**, insira o service principal no seguinte formato:  app:AppicationClientID@DirectoryTenantID

<figure><img src="../../.gitbook/assets/Manual entry.png" alt=""><figcaption></figcaption></figure>

<details>

<summary>Passo 2: Obter o Application Client ID e Directory Tenant ID</summary>



* No **Azure Portal**, acesse **Microsoft Entra ID**.

<img src="../../.gitbook/assets/image (420).png" alt="" data-size="original">\


* No menu lateral, clique em **App Registrations** (Registro de Aplicativos) e busque pelo **service principal** criado durante a instalação do portal (por padrão, o nome é **PowerEmbedded-app**).

<img src="../../.gitbook/assets/APP Registration.png" alt="" data-size="original">



* Copie os seguintes valores:
  * **Application Client ID**
  * **Directory Tenant ID**

![](<../../.gitbook/assets/image (422).png>)



*   Monte a string no formato correto:

    ```
    App<ApplicationClientID>@<DirectoryTenantID>
    ```

    Exemplo:

    ```
    app:436fed95-c8bc-4e1a-92d7-99a52c353675@ec50c6a3-b95c-4f22-8424-318f1cd459c6
    ```
* Volte ao **SSMS**, cole esse valor no campo **Manual Entry** e clique em **Add**.

![](<../../.gitbook/assets/image (423).png>)\


* Confirme as alterações clicando em **OK**.

![](<../../.gitbook/assets/image (424).png>)

</details>

Feito esse processo nós acabamos de adicionar o PowerEmbedded-app com administrador do Azure Analysis Service, o próximo passo é acessar o portal de administração do Power Embedded e clicar em salvar, siga o passo 3.



<details>

<summary>Passo 3: Acessar o portal do Power Embedded<br></summary>

* Acesse o **Portal de Administração do Power Embedded e** vá até **Configurações** e clique no botão de salvar.&#x20;

![](<../../.gitbook/assets/image (428).png>)\


Feito isso os relatórios irão funcionar normalmente

</details>

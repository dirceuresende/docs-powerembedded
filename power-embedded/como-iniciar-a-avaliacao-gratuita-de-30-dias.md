# Como iniciar a avaliação gratuita de 30 dias

Se você já leu a documentação do Power Embedded ou agendou uma apresentação e ficou interessado em testar a plataforma gratuitamente por 30 dias, sem nenhum custo, você pode agendar o início dos testes do sistema.

Para agendar a instalação do Power Embedded e iniciar o período de avaliação de 30 dias, por favor, utilize o link abaixo:\
[https://powerembedded.com.br/instalacao](https://powerembedded.com.br/instalacao)

Para que a instalação seja realizada com sucesso, é necessário a presença de uma pessoa que seja administradora do portal do Azure ([https://portal.azure.com/](https://portal.azure.com/)) e alguém que consiga acessar as configurações de locatário do Power BI ([https://app.powerbi.com/admin-portal/tenantSettings](https://app.powerbi.com/admin-portal/tenantSettings)).

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/10/Pre-requisitos-de-de-instalacao.png" alt=""><figcaption></figcaption></figure>



Sobre as permissões necessárias para a instalação, seguem atividades que iremos realizar no Azure AD (alguém com permissão “Azure Global Administrator” deve executar):

* Criar um aplicativo no AD (Acessar a tela de registros de aplicativo)
* Criar um novo grupo no AD
* Adicionar esse usuário neste grupo
* Criar o recurso do Power BI Embedded ou Fabric pelo Azure (**opcional se for utilizar o Trial do Fabric**)
* Adicionar o Service Principal recém-criado na role “Contributor” no recurso criado (**opcional se for utilizar o Trial do Fabric**)
* Adicionar o Service Principal recém-criado como “Power BI Capacity Administrator” do recurso criado  (**opcional se for utilizar o Trial do Fabric**)
* Logar na área administrativa do Power Embedded ([admin.powerembedded.com.br](https://admin.powerembedded.com.br/)), autorizar o App na sua organização (vai abrir um pop-up no primeiro acesso solicitando o consentimento) e criar os primeiros usuários com perfil de Administrador.
* Logar no portal de visualização do Power Embedded ([relatorios.powerembedded.com.br](https://relatorios.powerembedded.com.br/)) e autorizar o App na sua organização (vai abrir um pop-up no primeiro acesso solicitando o consentimento).



Seguem atividades que iremos realizar no portal de Administração do Power BI (alguém com permissão “Fabric Administrador” deve executar):

* Habilitar as configurações abaixo e permitir o grupo do AD criado a utilizar essas configurações:
  1. Inserir conteúdo em aplicativos
  2. As entidades de serviço podem usar APIs do Fabric
  3. As entidades de serviço podem acessar APIs de administrador somente leitura
  4. Aprimorar as respostas das APIs de administração com metadados detalhados
  5. Permitir pontos de extremidade XMLA e analisar no Excel com modelos semânticos locais
* Associar os workspaces ao recurso da capacidade contratada ou da trial (ou criar novos workspaces para migrar em paralelo)
* Adicionar o grupo do AD criado como administrador dos workspaces



{% hint style="info" %}
Para conhecer o processo de instalação, acesse a página [Instalação do Power Embedded](../documentacao-tecnica/instalacao/).
{% endhint %}

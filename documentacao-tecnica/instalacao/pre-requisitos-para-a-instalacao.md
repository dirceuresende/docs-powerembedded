# Pré-Requisitos para a Instalação

Para agendar a instalação do Power Embedded e iniciar o período de avaliação de 30 dias, por favor, utilize o link abaixo:

[**https://powerembedded.com.br/instalacao**](https://powerembedded.com.br/instalacao)



## O que é o processo de instalação

Para que a instalação seja realizada com sucesso, é necessário a presença de uma pessoa que seja administradora do portal do Azure ([https://portal.azure.com/](https://portal.azure.com/)) e alguém que consiga acessar as configurações de locatário do Power BI ([https://app.powerbi.com/admin-portal/tenantSettings](https://app.powerbi.com/admin-portal/tenantSettings)).

Vamos realizar todos os passos abaixo juntos, durante essa reunião de instalação, mas apenas para conhecimento, seguem as permissões necessárias para a instalação, seguem atividades que iremos realizar no Azure AD (alguém com permissão “Azure Global Administrator” deve executar):

1. Criar um aplicativo no AD (Acessar a tela de registros de aplicativos)
2. Criar um novo grupo no AD
3. Adicionar esse usuário neste grupo
4. Criar o recurso do Power BI Embedded ou Fabric pelo Azure (opcional se for utilizar o Trial do Fabric)
5. Adicionar o Service Principal recém-criado na role “Contributor” no recurso criado (opcional se for utilizar o Trial do Fabric ou não quiser que o portal gerencie a capacidade)
6. Adicionar o Service Principal recém-criado como “Power BI Capacity Administrator” do recurso criado  (opcional se for utilizar o Trial do Fabric ou não quiser que o portal gerencie a capacidade)
7. Logar na área administrativa do Power Embedded ([admin.powerembedded.com.br](https://admin.powerembedded.com.br/)), autorizar o aplicativo na sua organização (vai abrir um pop-up no primeiro acesso solicitando o consentimento) e criar os primeiros usuários com perfil de Administrador.
8. Logar no portal de visualização do Power Embedded ([relatorios.powerembedded.com.br](https://relatorios.powerembedded.com.br/)) e autorizar o aplicativo na sua organização (vai abrir um pop-up no primeiro acesso solicitando o consentimento).

&#x20;

Seguem atividades que iremos realizar no portal de Administração do Power BI (alguém com permissão “Fabric Administrador” deve executar):

1. Habilitar as configurações abaixo e permitir o grupo do AD criado a utilizar essas configurações:
   * Inserir conteúdo em aplicativos
   * As entidades de serviço podem usar APIs do Fabric
   * As entidades de serviço podem acessar APIs de administrador somente leitura
   * Aprimorar as respostas das APIs de administração com metadados detalhados
   * Permitir pontos de extremidade XMLA e analisar no Excel com modelos semânticos locais
2. Associar os workspaces ao recurso da capacidade contratada ou da trial (ou criar novos workspaces para migrar em paralelo)
3. Adicionar o grupo do AD criado como administrador dos workspaces



## Permissões necessárias do Power Embedded

### Permissões no Entra ID

**Microsoft Graph**:

<table><thead><tr><th width="139">Permissão</th><th width="358">Descrição</th><th width="102">Tipo</th><th>Consentimento</th></tr></thead><tbody><tr><td>User.Read</td><td>Permissão padrão para ler os dados do usuário logado na aplicação</td><td>Delegado</td><td>Não</td></tr><tr><td>User.Read.All <strong>(Opcional)</strong></td><td>Necessário apenas se for importar/sincronizar usuários com Entra ID</td><td>Aplicação</td><td>Sim</td></tr><tr><td>Group.Read.All <strong>(Opcional)</strong></td><td>Necessário apenas se for importar/sincronizar usuários com Entra ID</td><td>Aplicação</td><td>Sim</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



### Permissões no Portal de Administração do Power BI

<figure><img src="../../.gitbook/assets/image (418).png" alt=""><figcaption></figcaption></figure>

Permissões necessárias:

* As entidades de serviço podem usar APIs do Fabric
* As entidades de serviço podem acessar APIs de administrador somente leitura
* Permitir pontos de extremidade XMLA e analisar no Excel com modelos semânticos locais (já vem ativado por padrão)
* Inserir conteúdo em aplicativos (já vem ativado por padrão)



Permissões opcionais:

* Aprimorar as respostas das APIs de administração com metadados detalhados (Necessário caso queira permitir o uso da IA Generativa do portal)
* Aprimorar as respostas das APIs de administração com as expressões DAX e mashup (Necessário caso queira permitir o uso da IA Generativa do portal)
* Exportar para Excel (Necessário caso queira permitir exportar dados do relatório para Excel pelo portal)
* Exportar para .csv (Necessário caso queira permitir exportar dados do relatório para CSV pelo portal)
* Exportar relatório como apresentações em Power Point ou documentos PDF (necessário caso queira permitir exportar relatórios ou criar assinaturas por email no formato PDF ou Power Point)
* Exportar os relatórios como arquivos de imagem (necessário caso queira permitir exportar relatórios no formato de Imagem/PNG)



### Permissões na capacidade Fabric ou Power BI Embedded

O Power Embedded possui uma funcionalidade que permite ligar, desligar e alterar o SKU da capacidade manualmente, baseado em agendamento ou por demanda.

Caso você queira permitir que os administradores do portal possam utilizar esse recurso, você precisará realizar as atividades abaixo pelo portal do Azure:

1. Adicionar o Service Principal na role “Contributor” da capacidade (opcional se for utilizar o Trial do Fabric)
2. Adicionar o Service Principal como “Power BI Capacity Administrator” da capacidade (opcional se for utilizar o Trial do Fabric)



## Links úteis

[Documentação técnica da instalação](trial-do-fabric.md)

[Site principal do Power Embedded](https://powerembedded.com.br)

[Série de vídeos sobre o Power Embedded](https://powerembedded.com.br/videos)

[Calculadora do Power Embedded para estimar o custo da solução para o seu ambiente](https://powerembedded.com.br/calculadora)


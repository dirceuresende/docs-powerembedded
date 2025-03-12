# Pré-Requisitos para a Instalação

Para agendar a instalação do Power Embedded e iniciar o período de avaliação de 30 dias, por favor, utilize o link abaixo:

[**https://powerembedded.com.br/instalacao**](https://powerembedded.com.br/instalacao)



Para que a instalação seja realizada com sucesso, é necessário a presença de uma pessoa que seja administradora do portal do Azure ([https://portal.azure.com/](https://portal.azure.com/)) e alguém que consiga acessar as configurações de locatário do Power BI ([https://app.powerbi.com/admin-portal/tenantSettings](https://app.powerbi.com/admin-portal/tenantSettings)).

<figure><img src="../../.gitbook/assets/image (418).png" alt=""><figcaption></figcaption></figure>

Vamos realizar todos os passos abaixo juntos, durante essa reunião de instalação, mas apenas para conhecimento, seguem as permissões necessárias para a instalação, seguem atividades que iremos realizar no Azure AD (alguém com permissão “Azure Global Administrator” deve executar):

* Criar um aplicativo no AD (Acessar a tela de registros de aplicativos)
* Criar um novo grupo no AD
* Adicionar esse usuário neste grupo
* Criar o recurso do Power BI Embedded ou Fabric pelo Azure (opcional se for utilizar o Trial do Fabric)
* Adicionar o Service Principal recém-criado na role “Contributor” no recurso criado (opcional se for utilizar o Trial do Fabric)
* Adicionar o Service Principal recém-criado como “Power BI Capacity Administrator” do recurso criado  (opcional se for utilizar o Trial do Fabric)
* Logar na área administrativa do Power Embedded ([admin.powerembedded.com.br](https://admin.powerembedded.com.br/)), autorizar o aplicativo na sua organização (vai abrir um pop-up no primeiro acesso solicitando o consentimento) e criar os primeiros usuários com perfil de Administrador.
* Logar no portal de visualização do Power Embedded ([relatorios.powerembedded.com.br](https://relatorios.powerembedded.com.br/)) e autorizar o aplicativo na sua organização (vai abrir um pop-up no primeiro acesso solicitando o consentimento).

&#x20;

Seguem atividades que iremos realizar no portal de Administração do Power BI (alguém com permissão “Fabric Administrador” deve executar):

* Habilitar as configurações abaixo e permitir o grupo do AD criado a utilizar essas configurações:
  * Inserir conteúdo em aplicativos
  * As entidades de serviço podem usar APIs do Fabric
  * As entidades de serviço podem acessar APIs de administrador somente leitura
  * Aprimorar as respostas das APIs de administração com metadados detalhados
  * Permitir pontos de extremidade XMLA e analisar no Excel com modelos semânticos locais
* Associar os workspaces ao recurso da capacidade contratada ou da trial (ou criar novos workspaces para migrar em paralelo)
* Adicionar o grupo do AD criado como administrador dos workspaces



### Links úteis

[Documentação técnica da instalação](trial-do-fabric.md)

[Site principal do Power Embedded](https://powerembedded.com.br)

[Série de vídeos sobre o Power Embedded](https://powerembedded.com.br/videos)

[Calculadora do Power Embedded para estimar o custo da solução para o seu ambiente](https://powerembedded.com.br/calculadora)

&#x20;

### Processo de Migração dos Relatórios

Para o processo de implantação em fases, pode-se utilizar duas abordagens:

1. Migrar um ou alguns workspaces e migrar somente estes, para testar a solução e ir migrando os outros aos poucos.
2. Duplicar os relatórios, republicando para outro workspace, que estará rodando na capacidade do Fabric e importar somente esse(s) workspace(s).&#x20;

O processo de migração de um workspace é bem rápido, demorando alguns segundos e poucos cliques do mouse, sendo este rápido e sem gerar indisponibilidades e pode ser feito em massa (alterar vários/todos workspaces de uma vez)

Caso queira desfazer essa migração, é só voltar os workspaces para a capacidade Pro novamente.

&#x20;

### Sobre a capacidade do Power Embedded ou Fabric

A cobrança da capacidade do Embedded é calculada a nível de segundo pela Microsoft, e convertida para hora para gerar a cobrança final, e o nosso sistema permite definir os períodos de horários, por dia da semana, que o sistema irá ficar ligado e fora desse horário, o próprio sistema já desliga a capacidade automaticamente.

Caso alguém tente acessar o relatório fora desses horários, o sistema poderá ligar automaticamente para permitir que visualizem os relatórios e irá desligar automaticamente após um período de inatividade (definido por você).

Para definir qual a capacidade mais indicada do Power BI Embedded ou Microsoft Fabric para o seu cenário, o melhor caminho seria utilizando o período de 60 dias de avaliação gratuita do Microsoft Fabric, onde poderemos rodar toda a PoC de forma gratuita, fazendo com que os relatórios atuais sejam atualizados e processados por essa capacidade trial gratuita (F64), coletando o uso real dessa capacidade através da análise da carga do seu ambiente atual utilizando o relatório "Fabric Capacity Usage Metrics", disponibilizado pela própria Microsoft, a fim de identificar com muito mais precisão qual capacidade que o seu ambiente necessita.

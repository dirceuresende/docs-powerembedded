# Fontes de dados

Neste menu, é possível visualizar, exportar e filtrar as fontes de dados conectadas aos conjuntos de dados.

<figure><img src="../../.gitbook/assets/image (302).png" alt=""><figcaption></figcaption></figure>

### Permissões para listar gateways e fontes de dados

Para ser possível listar os gateways existentes no ambiente do Power BI, é necessário liberar uma permissão para o usuário do aplicativo (PowerEmbedded-App) no Power BI Serviço.

Acesse a tela de [Gerenciar conexões e gateways](https://app.powerbi.com/groups/me/gateways) e clique na opção _**Gerenciar gateways de dados locais.**_

<figure><img src="../../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure>

Agora você irá clicar nas 3 elipses (…) ao lado do gateway que deseja liberar a permissão e selecionar a opção Gerenciar Usuários.

<figure><img src="../../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure>

Na tela de gerenciamento de usuários, pesquise pelo nome do aplicativo que você está utilizando no Power Embedded (o nome padrão é _PowerEmbedded-App_), marque a permissão de Administrador e clique no botão Share.

<figure><img src="../../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure>

Agora repita esse processo para todos os gateways que você precisar gerenciar e acessar dados pelo Power Embedded, **especialmente se for utilizar conexão com o Analysis Services (SSAS).**

{% hint style="danger" %}
Se estiver utilizando conexão DirectQuery ou Live Connection com um **Analysis Services (SSAS),** essa configuração do gateway pode ser necessária para abrir os relatórios, caso apresentem erro de conexão.
{% endhint %}

{% hint style="warning" %}
**IMPORTANTE:** Não é necessário alterar as permissões nas fontes de dados, uma vez que o usuário do Power Embedded já possui permissão de administrador no Gateway.&#x20;

Isso reduz bastante o esforço de ter que configurar essas permissões em cada um das fontes de dados, uma vez que a quantidade de fontes de dados é bem maior que a quantidade de gateways.
{% endhint %}



### Fixar usuários no Analysis Services

Uma funcionalidade foi desenvolvida no Power Embedded para atender um cenário específico, caso você tenha um serviço de Analysis Services e deseja configurar um RLS (Row-Level Security) ao nível de empresa ao invés do nível de usuário.

Caso você queira trabalhar com RLS no Analysis Services no nível de usuário ao invés do nível de empresa, saiba mais acessando o artigo [Facilitando o mapeamento de usuários e RLS ao utilizar o Analysis Services](https://powerembedded.com.br/facilitando-o-mapeamento-de-usuarios-e-rls-ao-utilizar-o-analysis-services/).

Para configurar o RLS no Analysis Services, acessando pelo Power Embedded ou até mesmo pelo Power BI, é necessário fazer o mapeamento usuário por usuário em configurações de gateways do Power BI.

<div align="left">

<figure><img src="../../.gitbook/assets/image (303).png" alt=""><figcaption></figcaption></figure>

</div>

Se você tem 100 usuários, isso demandará um tempo considerável para configurar manualmente e aplicar o RLS, uma vez que não há uma API disponível para automatizar isso no Power BI.

Caso você queira utilizar um usuário fixo, independente de quem estiver acessando o relatório, basta utilizar um asterisco (\*) no nome original e o nome do usuário que será utilizado para fazer a conexão.

Entretanto, para um cenário onde não é necessário identificar individualmente cada usuário, mas sim filtrar os dados utilizando um usuário fixo por empresa, existe um recurso nas fontes de dados, quando o tipo de dado é Analysis Services, chamado “Fixar Usuário” e que resolve esse problema.

<figure><img src="../../.gitbook/assets/image (304).png" alt=""><figcaption></figcaption></figure>

Ao fixar o usuário para cada empresa nesta conexão, defino qual usuário será enviado para o Analysis Services, independente de qual o usuário que está visualizando o relatório.&#x20;

Por exemplo, se todos os usuários associados à empresa Microsoft estiverem utilizando este Analysis Services, todos os pedidos enviados pelo Power Embedded para o Power BI serão atribuídos ao usuário “douglas.rosseto@powertuning@.com.br” no exemplo abaixo.

<figure><img src="../../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>

Ao configurar o mapeamento de usuário na tela de gateways do Power BI, eu só preciso fazê-lo para o usuário Douglas Rosseto, ao invés de realizar o processo para os 100 usuários individualmente, o que seria demorado e complicado em termos de manutenção.

Esta é uma forma de simplificar este cenário específico, onde não é necessário aplicar um filtro individual por RLS para cada usuário, mas sim por empresa, o que atenderia às necessidades com o cadastro de um único usuário.

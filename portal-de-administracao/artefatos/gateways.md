# Gateways

Nesta tela é possível visualizar os gateways disponíveis no Power BI e algumas informações úteis como nome do servidor, informações de contato, versão do gateway e quantidade de fontes de dados que utilizam esse gateway, servindo como um inventário dos gateways da sua empresa, uma vez que o sistema permite exportar esses dados para CSV e Excel.

Ao clicar em “Ações” e depois em “Gerenciar no Power BI”, é possível ser redirecionado para o Power BI para gerenciar as configurações do gateway por lá.

<figure><img src="../../.gitbook/assets/image (298).png" alt=""><figcaption></figcaption></figure>



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


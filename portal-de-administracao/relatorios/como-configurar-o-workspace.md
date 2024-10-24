# Como configurar o workspace

{% embed url="https://www.youtube.com/watch?v=rf7Hpz8CSOs" %}

Para que seja possível importar os relatórios do Power BI para o Power Embedded, você precisará fazer duas coisas no workspace:

1. Alterar a capacidade do Workspace para capacidade Premium (Microsoft Fabric ou Power BI Embedded).
2. Adicionar o Service Principal criado (usuário do Power Embedded) como administrador dos workspaces que você quer importar relatórios (pode ser mais de 1).

Para alterar a capacidade do Workspace para capacidade Premium (Microsoft Fabric ou Power BI Embedded), acesse o workspace e clique no botão “Configurações de workspace”

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Caso sua tela seja muito pequena, clique nos 3 pontinhos e selecione a opção “Configurações de workspace”

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



Na tela que foi aberta, clique no menu “Informações da licença”, depois escolha uma das licenças Premium abaixo:

* Capacidade Premium (Descontinuada e substituída pelo Fabric)
* Inserido (Power BI Embedded)
* Capacidade de Malha (Fabric)
* Avaliação (Fabric Trial = F64)

<figure><img src="../../.gitbook/assets/image (369).png" alt=""><figcaption></figcaption></figure>

A escolha da licença irá depender qual foi o tipo de licença contratada e está disponível no seu ambiente.

{% hint style="warning" %}
A opção **Capacidade Premium** só estará disponível caso você tenha uma capacidade Premium disponível no seu ambiente, assim como **Inserido** e **Capacidade de malha** também só estarão disponíveis caso você tenha pelo menos um recurso desses tipos criados no Azure.

Além disso, o seu usuário precisa estar configurado como **Administrador de capacidade** neste recurso no Azure.

A opção **Avaliação** só ficará disponível caso o seu usuário tenha alguma avaliação do Fabric ativada.
{% endhint %}

No campo “Capacidade de licença”, selecione o recurso que você criou anteriormente na lista.

Clique no botão “Selecionar licença”, no final da página.

A partir desse momento, esse workspace agora está na capacidade Premium e associado ao recurso do Power BI Embedded ou Fabric.

{% hint style="warning" %}
Caso você pause esse recurso, o Workspace ficará inacessível, mesmo utilizando uma conta Pro e acessando direto pelo portal. Os conjuntos de dados também não atualizam e vão dar erro ao tentar atualizar, caso a capacidade esteja pausada.
{% endhint %}



O último passo agora é adicionar o usuário do Power Embedded ao Workspace.

Para adicionar o usuário do Power Embedded (PowerEmbedded-App) como administrador de um workspace, acesse o workspace, clique nos 3 pontinhos e selecione a opção “Gerenciar acesso”

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

Clique no botão “+ Adicionar pessoas ou grupos”.

<div align="left">

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

</div>

Pesquise pelo nome do aplicativo que foi criado anteriormente (PowerEmbedded-App) e lembre de alterar o nível de acesso para “Administrador”. Após isso, clique no botão “Adicionar”.

<div align="left">

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

</div>

Pronto! Agora o Power Embedded já possui acesso nesse workspace. Repita isso para todos os Workspaces que você quer importar relatórios.

{% hint style="info" %}
Para configurar a capacidade no portal do azure, acesse [Configuração de Capacidades](../artefatos/capacidades/).
{% endhint %}

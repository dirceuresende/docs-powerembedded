# Requisitos para importar relatório

{% embed url="https://www.youtube.com/watch?v=rf7Hpz8CSOs" %}

Para que seja possível importar os relatórios do Power BI para o Power Embedded, você precisará fazer duas coisas no workspace:

1. Alterar a capacidade do Workspace para capacidade Premium (Embedded).
2. Adicionar o Service Principal criado (usuário do Power Embedded) como administrador dos workspaces que você quer importar relatórios (pode ser mais de 1).

Para alterar a capacidade do Workspace para capacidade Premium (Embedded), acesse o workspace, clique nos 3 pontinhos e selecione a opção “Configurações de workspace”

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Na tela que foi aberta, clique no menu “Premium”, depois escolha a licença “Inserido” (Embedded), Capacidade de Malha (Fabric) ou Avaliação. Isso irá depender qual foi o tipo de licença contratada e no campo “Capacidade de licença”, selecione o recurso que você criou anteriormente na lista.

\
Clique no botão “Aplicar”, logo mais abaixo.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

A partir desse momento, esse workspace agora está na capacidade Premium e associado ao recurso do Power BI Embedded. Caso você pause esse recurso, o Workspace ficará inacessível, mesmo utilizando uma conta Pro e acessando direto pelo portal.

O último passo agora é adicionar o usuário do Service Principal ao Workspace.

Para adicionar o Service Principal criado como administrador de um workspace, acesse o workspace, clique nos 3 pontinhos e selecione a opção “Gerenciar acesso”

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Clique no botão “+ Adicionar pessoas ou grupos”.

<div align="left">

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

</div>

Pesquise pelo nome do aplicativo que foi criado anteriormente (PowerEmbedded-App) e lembre de alterar o nível de acesso para “Administrador”. Após isso, clique no botão “Adicionar”.

<div align="left">

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

</div>

Pronto! Agora o Power Embedded já possui acesso nesse workspace. Repita isso para todos os Workspaces que você quer importar relatórios.

{% hint style="info" %}
Para configurar a capacidade no portal do azure, acesse [Configuração de Capacidades](../artefatos/capacidades/).
{% endhint %}

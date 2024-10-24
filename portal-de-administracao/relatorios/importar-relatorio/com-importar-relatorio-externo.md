# Com importar relatório externo

O Power Embedded foi idealizado para suportar relatórios do Power BI, sejam paginados, dashbords e relatórios tradicionais.

Além desse tipos, o Power Embedded também tem suporte para importação de URL externa, o que abre infinitas possibilidades para centralizar a gestão e visualização de relatórios de diferentes ferramentas em uma plataforma única.

Você pode até mesmo utilizar esse recurso para compartilhar arquivos entre os funcionários da sua empresa de forma segura e auditável.

Para utilizar o recurso, vá até a página de [Relatórios](https://admin.powerembedded.com.br/Reports) e clique no botão **Importar** > **Relatório da Web**.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



Digite o nome do relatório ou arquivo que será mostrado no portal de relatório e informe a URL original de acesso.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Neste exemplo, estarei importando um relatório que criei no Google Data Studio para o Power Embedded</p></figcaption></figure>

{% hint style="info" %}
Muitos serviços e sites, como Canva, Slideshare e outros, bloqueiam por padrão, que você mostre um conteúdo dentro de outro site (como o Power Embedded), mas disponibilizam um botão ou opção para gerar um link compartilhável (embed), que possui liberação para ser incorporado em outros sites.\
\
Se você tentar importar uma URL e receber uma mensagem de erro ao tentar visualizar no Power Embedded, verifique se existe alguma opção para gerar esse link compartilhável no serviço que você está tentando incorporar.
{% endhint %}



Após importar essa URL externa, o relatório estará disponível na página de relatórios como qualquer outro relatório do Power BI que você já importou.

Todas as funcionalidades estarão disponíveis (com exceção do RLS), como permissões por usuário, grupos, escolher uma imagem para ser a miniatura e as auditorias.

{% hint style="warning" %}
Essa opção de "Abrir em uma nova aba externa" serve para atender 2 cenários:

* Ao clicar no relatório externo, é interessante que sempre seja aberta uma nova aba no navegador.
* O servidor que está hospedando a página ou arquivo não permite o uso de Embed do conteúdo e a conexão acaba sendo recusada ao tentar utilizar o recurso de Relatório da Web e não há uma opção de gerar link compartilhável.\
  \
  Ao ativar essa opção, o relatório será aberto em uma nova aba e esse problema não acontecerá.
{% endhint %}



Os relatórios de URL externa aparecem em uma categoria separada:

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>



Os relatórios, links ou arquivos podem ser visualizados normalmente:

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
A segurança dos relatórios e o RLS nesse formato é feita utilizando cookies de sessão do navegador, onde você precisará estar logado nesse serviço que você está tentando inserir para conseguir mostrar os dados no Power Embedded corretamente e ter os filtros de segurança aplicados.
{% endhint %}



Até mesmo arquivos podem ser acessados utilizando esse recurso, como, por exemplo, um documento PDF hospedado numa conta do OneDrive:

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>



A visualização segue o mesmo formato e padrão dos já existentes:

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
O Power Embedded não hospeda ou importa os arquivos que você quer mostrar na plataforma utilizando essa importação, portanto, você precisará hospedar esses arquivos em algum local externo, como OneDrive, FTP ou Sharepoint.
{% endhint %}



As auditorias de acesso de relatório são aplicadas normalmente para os relatórios externos, assim como já funcionam nos outros tipos de relatórios

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Espero que vocês aproveitem bem esse novo recurso e boas análises!

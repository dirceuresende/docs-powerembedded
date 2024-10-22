# Mostrar relatório no seu sistema

{% embed url="https://www.youtube.com/watch?v=jNMQy3avxLE" %}

### **Como obter a Chave de API para autenticação as requisições**

O primeiro passo, é obter a chave da API na tela de configurações para autenticar:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-22.png" alt=""><figcaption></figcaption></figure>

</div>



Com essa chave, você já consegue autenticar as requisições utilizando a API.

### **Método 1: Utilizar o endpoint Identity/URL**

Para retornar a URL que você irá utilizar para acessar o portal de relatórios de forma transparente, sem passar pela tela de login, utilize a chamada **POST** abaixo:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-1536x237.png" alt=""><figcaption></figcaption></figure>

</div>

O cabeçalho **X-API-Key** deve ser informado, passando como valor, o token da API gerado acima pela tela de configurações.

O corpo da requisição (body) possui os seguintes valores possíveis:

```json
{
    "userEmail": "[email protected]",
    "baseUrl": "https://bi.minhaempresa.com.br",
    "organizationId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "reportId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
    "hideMenu": true,
    "hideNavbar": true,
    "hideSidebar": true,
    "embed": true
}
```

#### Parâmetros gerais

* **userEmail**: Único campo obrigatório na requisição. Deve ser informado o email da pessoa que está logada no seu sistema. Esse usuário que será gravado nas auditorias e os relatórios que esse usuário tem acesso que serão mostrados na tela. Caso o relatório tenha RLS, este será aplicado automaticamente, utilizando as regras de filtragem desse usuário informado.
* baseUrl: Neste campo, você deve preencher com a informação do subdomínio configurado. É obrigatório informar esse dado para que toda a experiência seja personalizada, inclusive no caso de expiração do token.

Quando os parâmetros de organizationId e reportId **NÃO** são informados, o portal de visualização completo será renderizado no seu sistema, assim como quando você acessa no modo tradicional (sem API), mostrando apenas os relatórios que o usuário informado possui acesso. O usuário poderá navegar livremente nos relatórios que ele possui acesso.

#### Parâmetros para controle de exibição

hideMenu: Oculta a barra de menus quando o relatório é aberto.

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-6-768x28.png" alt=""><figcaption></figcaption></figure>

</div>

hideNavbar: Oculta a barra de navegação quando o relatório é aberto.

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-7-768x39.png" alt=""><figcaption></figcaption></figure>

</div>

hideSidebar: Oculta a barra lateral na tela de navegação.

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-8.png" alt=""><figcaption></figcaption></figure>

</div>

embed: É um parâmetro atalho que pode ser utilizado para definir todas as propriedades de exibição acima de uma única vez.



#### Parâmetros para exibição de um relatório apenas

Caso você queira exibir um relatório específico, você precisará informar, obrigatoriamente, os 2 parâmetros abaixo:

organizationId: É o ID único da sua organização no sistema. Esse ID é fixo e nunca é alterado. Esse ID você pode obter na URL da tela de “Configurações"

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-4-1-768x555.png" alt=""><figcaption></figcaption></figure>

</div>

reportId: É o ID do relatório, onde cada relatório tem o seu ID único (é o mesmo reportId do relatório no Power BI serviço). Para obter o ID do relatório, capture o ID que fica na URL da tela de edição do relatório:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-5-1024x829.png" alt=""><figcaption></figcaption></figure>

</div>



### **Retorno da API**

O retorno da API é uma URL que só pode ser acessada uma única vez e caso não tenha acesso, irá expirar em 5 minutos:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-3-1024x127.png" alt=""><figcaption></figcaption></figure>

</div>

Caso você tenha informado os outros parâmetros, como organizationId e reportId (para mostrar apenas 1 relatório) e os parâmetros de exibição, a requisição terá esse formato:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-10-768x252.png" alt=""><figcaption></figcaption></figure>

</div>

E a URL retornada será algo assim:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-11-768x149.png" alt=""><figcaption></figcaption></figure>

</div>



Com essa URL gerada, você só precisa criar um iframe utilizando ela como o exemplo abaixo:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-fazer-a-requisicao-para-a-API-Identity-URL-12-768x332.png" alt=""><figcaption></figcaption></figure>

</div>



E com isso, você já consegue mostrar os relatórios do Power BI na sua aplicação, através do Power Embedded, de forma transparente e segura.

Como o token da URL é de uso ÚNICO, essa URL só pode ser acessada uma única vez. Caso você queira mostrar o relatório novamente, terá que executar essa requisição novamente.

Como o token é para o usuário específico, ao acessar um relatório, o Power Embedded sabe quem é o usuário que está acessando e faz as devidas validações se esse usuário possui acesso ao relatório que está sendo mostrado e aplica as regras de RLS, caso o relatório possua.



### Método 2: Utilizando o endpoint Identity/Token

Para conseguir gerar o token de acesso e renderizar os relatórios na sua aplicação, você deverá primeiro obter o token usando a chamada abaixo:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-23-768x414.png" alt=""><figcaption></figcaption></figure>

</div>



E o servidor irá retornar o token de uso ÚNICO para chamar as API’s (cada requisição deverá solicitar um novo token):

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-23-768x414.png" alt=""><figcaption></figcaption></figure>

</div>



Agora podemos fazer a chamada da API que renderiza o relatório, informando como parâmetros:

* **A URL base do portal de visualização** (Ex: [https://relatorios.powerembedded.com.br](https://relatorios.powerembedded.com.br/) – Aqui você utiliza o seu domínio personalizado, como [https://bi.suaempresa.com.br/](https://bi.suaempresa.com.br/), por exemplo)
* **O token gerado no passo anterior** (Ex: 2506b719-5a7e-789b-812f-c64013cc617f)
* **O ID da organização** (ID fixo para cliente do Power Embedded – Está na URL da tela de configurações – Ex: 12201800-1a46-491a-bfe3-6ee5590e372e)
* **O ID do relatório** que será embeddado (Ex: a4ee7a1e-6c65-44e7-9a38-06dd8514483c)

Com isso, você irá abrir um iframe com a seguinte URL:\
[https://bi.suaempresa.com.br/integration/tokenauth?token={token\_gerado}\&embed=true\&returnUrl=/Organization/{Id\_da\_Organizacao}/Report/{Id\_Relatorio}](https://relatorios.powerembedded.com.br/integration/tokenauth?token={token\_gerado}\&embed=true\&returnUrl=/Organization/{Id\_da\_Organizacao}/Report/{Id\_Relatorio})

Exemplo com as variáveis preenchidas:\
[https://bi.suaempresa.com.br/integration/tokenauth?token=98b6e796-3b1f-4f2f-abfe-aa2a8a1eadb8\&embed=true\&returnUrl=/Organization/12201800-1a46-491a-bfe3-6ee5590e372e/Report/a4ee7a1e-6c65-44e7-9a38-06dd8514483c](https://relatorios.powerembedded.com.br/integration/tokenauth?token=2506b719-5a7e-789b-812f-c64013cc617f\&embed=true\&returnUrl=/Organization/12201800-1a46-491a-bfe3-6ee5590e372e/Report/a4ee7a1e-6c65-44e7-9a38-06dd8514483c)

{% hint style="warning" %}
Como o token é de uso ÚNICO, essa URL só pode ser acessada uma única vez.
{% endhint %}

Caso você queira embeddar o relatório novamente, terá que gerar um novo token de acesso para o e-mail informado.

Como o token é para o usuário específico, ao acessar um relatório, o Power Embedded sabe quem é o usuário que está acessando e faz as devidas validações se esse usuário possui acesso ao relatório que está sendo embeddado e aplica as regras de RLS, caso o relatório possua.



### **Documentação**

Documentação completa da API:\
[Swagger UI (powerembedded.com.br)](https://api.powerembedded.com.br/index.html)

Página de demonstração da API para Embeddar os relatórios:\
[Demo – PowerPortal.IntegrationDemo (powerembedded.com.br)](https://dev.demoapi.powerembedded.com.br/)

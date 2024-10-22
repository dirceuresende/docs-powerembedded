# Automações com APIs

### **Como obter a Chave de API para autenticação as requisições**

O primeiro passo, é obter a chave da API na tela de configurações para autenticar

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/06/Power-Embedded-Como-obter-a-chave-da-API-768x622.png" alt=""><figcaption></figcaption></figure>

</div>

Com essa chave, você já consegue autenticar as requisições à API.



### **Gerenciando usuários pela API**

Chamada para realizar uma listagem de usuários do sistema

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-2.png" alt=""><figcaption></figcaption></figure>

</div>

Resposta do servidor

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-3.png" alt=""><figcaption></figcaption></figure>

</div>

Aonde o array reports retorna o ID dos relatórios que o usuário tem acesso.

Você também pode filtrar a lista de usuário por nome e/ou e-mail

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-4-768x99.png" alt=""><figcaption></figcaption></figure>

</div>

Para criar um novo usuário no sistema, utilize a chamada abaixo:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-5.png" alt=""><figcaption></figcaption></figure>

</div>

Onde as roles são:\
1 = Administrador\
2 = Contribuidor\
3 = Visualizador

Para apagar um usuário do sistema, utilize a chamada abaixo:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-6-768x100.png" alt=""><figcaption></figcaption></figure>

</div>

### &#x20;**Controlando permissões em relatórios pela API**

Você também pode dar permissão para um usuário acessar um determinado relatório, informando o e-mail do usuário e uma lista com os ID’s dos relatórios:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-7.png" alt=""><figcaption></figcaption></figure>

</div>

Para remover a permissão de um usuário em um relatório, utilize a chamada abaixo:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-8.png" alt=""><figcaption></figcaption></figure>

</div>



### **Listando os Relatórios existentes no Power Embedded**

Você também pode listar os relatórios existentes para recuperar alguns metadados, como o ID do relatório:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-9.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-10-1536x613.png" alt=""><figcaption></figcaption></figure>

</div>



Também é possível filtrar o relatório pelo nome, workspace ou tipo:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-11-768x107.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-12-1536x605.png" alt=""><figcaption></figcaption></figure>

</div>



### **Row-Level Security (RLS) utilizando a API**

Você também pode listar o nome das roles que um relatório possui, para criar a associação Relatório X Usuário X Role (RLS), onde o parâmetro da chamada é o ID do relatório:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-13-768x94.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-14-300x289.png" alt=""><figcaption></figcaption></figure>

</div>



Para listar esse mapeamento entre Relatório x Usuário x Role, você pode utilizar a chamada abaixo, e poderá filtrar os dados pelo ID do usuário, Id do relatório ou nome da role:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-15-1536x103.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-16.png" alt=""><figcaption></figcaption></figure>

</div>



Para atribuir uma permissão de RLS, você irá passar uma lista de e-mails que vão ser adicionados na regra do RLS, o ID do relatório e o nome da role que os usuários serão adicionados:

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-17-768x294.png" alt=""><figcaption></figcaption></figure>

</div>



Para remover a permissão RLS, você vai mudar somente a URL da requisição, pois são os mesmos parâmetros para adicionar

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-18-768x287.png" alt=""><figcaption></figcaption></figure>

</div>



### **Consultando o log de acessos de relatórios do Power Embedded via API**

Você também pode utilizar a API para acessar o log de auditoria de relatórios e conseguir consultar todos os acessos a relatórios realizados pelos usuários do Power Embedded.

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-19.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-20.png" alt=""><figcaption></figcaption></figure>

</div>



Você pode aplicar filtros na requisição por vários campos

<div align="left">

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/12/Novo-recurso-APIs-para-integrar-e-Embeddar-o-Power-Embedded-na-sua-aplicacao-21-1536x108.png" alt=""><figcaption></figcaption></figure>

</div>



### **Como mostrar os relatórios do Power BI na sua aplicação**

{% hint style="info" %}
Para saber mais sobre exibição de relatórios em aplicações externas, acesse a página [Mostrar relatórios no seu sistema](mostrar-relatorio-no-seu-sistema.md).
{% endhint %}



### **Documentação**

Documentação completa da API:\
[Swagger UI (powerembedded.com.br)](https://api.powerembedded.com.br/index.html)

Página de demonstração da API para Embeddar os relatórios:\
[Demo – PowerPortal.IntegrationDemo (powerembedded.com.br)](https://dev.demoapi.powerembedded.com.br/)

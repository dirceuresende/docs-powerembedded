# Segurança (RLS)

{% embed url="https://www.youtube.com/watch?v=xuLr4iWR378" %}

A RLS (segurança em nível de linha) com o Power BI pode ser usada para restringir o acesso a dados para determinados usuários. Os filtros restringem o acesso a dados no nível da linha e você pode definir filtros nas funções.

A RLS permite:&#x20;

* Definir filtros de carregamento de dados com base no usuário que está visualizando o relatório&#x20;
* Criar diversas filtragens de dados em um mesmo relatório&#x20;
* Restrição por perfil de usuário&#x20;
* Restrição por função (cargo/setor)

Uma das vantagens do RLS é ter apenas um único relatório e distribuir para vários usuários ou clientes, sem ter que criar um relatório com dados filtrados para cada perfil de usuário, reduzindo a manutenção desses relatórios, uma vez que um único relatório filtraria os resultados apresentados de acordo com a pessoa que está visualizando.

No Power Embedded, oferecemos suporte tanto para RLS (Row-Level Security) quanto para OLS (Object-Level Security).

{% hint style="warning" %}
O RLS/OLS é configurado APENAS no Power Embedded, não mais no Power BI serviço.

Caso seja necessário que algumas pessoas continuem acessando o relatório no Power BI serviço, aí você deverá configurar no Power BI também.
{% endhint %}



Abaixo estão algumas informações para ajudar no entendimento.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure></div>

Quando o relatório possuir uma ou mais regras de RLS, é obrigatório associá-la ao usuário que está visualizando o relatório, seja utilizando RLS estático ou dinâmico, caso contrário ele não conseguirá visualizar os relatórios, e uma mensagem como esta será exibida:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (235).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Diferente do Power BI serviço, onde os usuários administradores não são afetados pelo RLS, no Power Embedded, TODOS os usuários são afetados pelo RLS.

Se um usuário administrador não estiver em nenhuma regra de segurança, irá receber essa mensagem de erro acima. Caso esse usuário precise visualizar todos os dados, crie uma regra de segurança sem nenhum filtro e associe o usuário à essa regra de segurança.
{% endhint %}



### Como gerenciar as regras de segurança no Power Embedded

Para associar um usuário a uma regra de RLS ou OLS, você tem 3 formas de fazer essa configuração:

1.  Na tela de [Relatórios](https://admin.powerembedded.com.br/Reports), pesquise o relatório que deseja gerenciar as regras de RLS, clique no botão **Ações** e depois clique no item **Segurança.** \
    \
    Se o relatório tiver RLS e esse botão não estiver aparecendo, entre na página de [**Conjuntos de dados**](https://admin.powerembedded.com.br/Datasets) e clique no botão **Recarregar.**\
    \


    <figure><img src="../../../../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure>


2.  Na página de [Relatórios](https://admin.powerembedded.com.br/Reports), pesquise o relatório que deseja gerenciar as regras de RLS, clique no botão **Ações** e depois clique no item **Editar.** \
    \
    Você deverá ver um botão amarelo chamado **Editar RLS.** Se o relatório tiver RLS e esse botão não estiver aparecendo, entre na página de [**Conjuntos de dados**](https://admin.powerembedded.com.br/Datasets) e clique no botão **Recarregar**\


    <figure><img src="../../../../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure>


3.  Na página de [**Conjuntos de dados**](https://admin.powerembedded.com.br/Datasets), pesquise o conjunto de dados que deseja gerenciar as regras de RLS, clique no botão **Ações** e depois clique no item **Segurança.** \


    <figure><img src="../../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>



### **Segurança estática**

Para empresas que precisam ou gostariam de criar várias regras de segurança e associar os usuários com as regras, sem a necessidade de ter uma tabela no modelo com os usuários e permissões, existe a segurança estática, que é mais simples de configurar, mas apresenta performance pior e é mais difícil de gerenciar as permissões.

Nesse formato, você irá visualizar a lista das roles que existem no modelo e poderá associar os usuários ou grupos que serão filtrados por essa regra, clicando no botão de ações.

<figure><img src="../../../../.gitbook/assets/image (227).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>



Aqui está um print das regras criadas no Power BI Desktop. Existem duas regras criadas: ‘Alimentos’ e ‘Bebidas’. Isso significa que se um usuário for atribuído à regra de alimentos, ele só poderá visualizar dados relacionados a alimentos.

<figure><img src="../../../../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure>

Ao publicar o relatório e acessar “Ações” > “Segurança”, o Power Embedded identifica automaticamente as regras criadas e irá carregar a lista com essas regras.

Você pode então atribuir essas regras aos usuários conforme necessário.

{% hint style="warning" %}
Se a lista de regras de segurança não estiver sendo mostrada na tela de segurança, mesmo após clicar no botão "Recarregar lista de roles", provavelmente é porque o workspace do relatório está em uma capacidade PRO ao invés de uma capacidade dedicada (Fabric, Power BI Embedded ou Power BI Premium)
{% endhint %}



Quando o usuário "marcos" acessar o relatório, ele só vai verá as informações relacionadas a alimentos.

<figure><img src="../../../../.gitbook/assets/image (228).png" alt=""><figcaption></figcaption></figure>



### **Segurança Dinâmica**

Com a Segurança Dinâmica, você pode definir uma ou mais roles e elas serão aplicadas automaticamente para todos os usuários que acessem o relatório. Essa é a recomendação de boas práticas para melhor gerenciamento de regras e performance.

Nesse formato, a role/função criada no Power BI Desktop, receberá o e-mail do usuário que está acessando o relatório (utilizando as funções USERNAME() ou USERPRINCIPALNAME()) e será responsável por realizar os filtros utilizando esse e-mail, com base nas regras criadas.

<figure><img src="../../../../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure>

Nessa forma de aplicar os filtros automaticamente conforme o usuário, é necessário manter no seu modelo uma tabela com os usuários e permissões segundo a regra do RLS ou OLS.

A tabela abaixo exemplifica um modelo contendo as informações de e-mails dos gerentes de um determinado relatório.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (230).png" alt=""><figcaption></figcaption></figure></div>

Relacionamento entre as tabelas, ou seja, sua tabela vai estar vinculada a uma fato que contém as informações.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (231).png" alt=""><figcaption></figcaption></figure></div>

Ao publicar esse relatório, a regra passa a ser visualizada no portal, é só selecionar a mesma e a regra será aplicada, diferente da estática aqui você não atribui um usuário a regra, somente clica na regra que deseja aplicar.

<figure><img src="../../../../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure>



Relatório normal sem a regra existentes:

<figure><img src="../../../../.gitbook/assets/image (233).png" alt=""><figcaption></figcaption></figure>



Relatório com regra de RLS existente no modelo utilizando a RLS dinâmica:

<figure><img src="../../../../.gitbook/assets/image (234).png" alt=""><figcaption></figcaption></figure>

A regra de RLS é aplicada utilizando a função UserPrincipalName() para identificar qual usuário está logado e realizar o filtro nas outras tabelas também, ou seja, o usuário só consegue visualizar as informações pertinentes a ele.



### Prioridade do RLS estático e dinâmico

Para configurar corretamente regras de RLS em alguns cenários, pode ser necessário utilizar RLS estático e dinâmico ao mesmo tempo.



Como o Power Embedded prioriza essas regras:

1. Verifica se o usuário que está visualizando o relatório está associado à alguma regra de RLS estático. Se estiver, envia essa regra e finaliza a validação.
2. Verifica se o usuário que está visualizando o relatório está em algum grupo, que está associado à alguma regra de RLS estático. Se estiver, envia essa regra e finaliza a validação.
3. Verifica se alguma regra de RLS dinâmico está marcada. Se estiver, envia essa regra e finaliza a validação.
4. Nenhuma das condições anteriores foi atingida, então não vai enviar nenhuma regra de RLS e, provavelmente, vai dar erro de RLS ao tentar abrir o relatório.



### RLS com DirectQuery no Power BI

Se você se deparar com o erro abaixo ao tentar acessar o relatório, é muito provável que a tabela que contém a regra de RLS esteja utilizando a conexão DirectQuery.

<figure><img src="../../../../.gitbook/assets/image (236).png" alt=""><figcaption></figcaption></figure>

O DirectQuery é amplamente utilizado para acessar dados em tempo real. No entanto, é importante destacar que as regras de Row-Level Security (RLS) não se aplicam diretamente às tabelas conectadas via Direct Query no Power BI.&#x20;

Isso acontece porque a configuração dessas regras, quando se utiliza DirectQuery, deve ser feita no nível do banco de dados, e não no Power BI.&#x20;

Por isso, é importante alterar a conexão da tabela para os modos Import ou Dual, caso seja necessário aplicar essas regras.



Para alterar a conexão da tabela, siga os passos abaixo:

1. Abra o Power BI Desktop.
2. Vá para a “**Exibição do Modelo**“.
3. Selecione a tabela que **possui regras de RLS e está conectada via DirectQuer**y.
4. Acesse o menu **“Avançado”**, conforme mostrado na imagem.
5. Altere o modo de armazenamento para **“Importar” ou “Dual”.**

<figure><img src="../../../../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>

Ao seguir o passo a passo anterior, um aviso como o mostrado na imagem aparecerá na tela. Basta clicar em “OK” e prosseguir. Após realizar esse processo, é só publicar o relatório novamente.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (238).png" alt=""><figcaption></figcaption></figure></div>

Agora irá conseguir ver suas informações.

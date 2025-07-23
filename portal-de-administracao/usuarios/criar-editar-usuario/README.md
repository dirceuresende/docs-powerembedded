# Criar/editar usuário

{% embed url="https://www.youtube.com/watch?v=0zV2ADJmWcc" %}

Nesse método, você pode criar usuários manualmente, um por um, e atribuir suas permissões, funções, departamentos, etc.

O processo de cadastro de usuário é bastante simples. No entanto, a documentação abaixo oferece um guia detalhado para orientá-lo durante esse processo.

É importante observar que o cadastro de usuário envolve várias abas relacionadas ao acesso e às permissões dentro da aplicação. As abas são: **Geral**, **Permissões**, **Grupos**, **Empresas**, e **Assistentes**.

### Geral

Nesta aba, você pode cadastrar o e-mail, nome, função, departamento e data de validade do usuário. Também define a página inicial após o login e o método de autenticação a ser utilizado.

<figure><img src="../../../.gitbook/assets/Screenshot_30.png" alt=""><figcaption></figcaption></figure>

* **Data de validade**: Defina uma data de validade para o usuário. Após essa data, o usuário não poderá acessar o sistema.
* **Página inicial após login**: Selecione uma página ou relatório específico para o usuário ser redirecionado imediatamente após o login. Certifique-se de que o usuário tenha acesso ao relatório ou aplicativo selecionado.
* **Método de autenticação**: Escolha o método de autenticação que o usuário deve usar.



### Permissões

Nesta aba, você define as permissões que o usuário terá ao visualizar um relatório.

Isso inclui a capacidade de baixar arquivos PBIX, atualizar conjuntos de dados, entre outros.

{% hint style="warning" %}
As permissões concedidas para o usuário são aplicadas em TODOS os relatórios que esse usuário tenha acesso. Se você precisa limitar essas permissões para relatórios específicos, libere essa permissão utilizando Grupos.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Screenshot_29.png" alt=""><figcaption></figcaption></figure>

### Grupos

Aqui você associa o usuário a um ou mais grupos de acesso.

Para adicionar o usuário ao grupo, basta marcar os grupos e depois clicar no botão "Salvar".

Para remover o usuário do grupo, basta desmarcar os grupos e depois clicar no botão "Salvar".

Quando o usuário faz parte de um grupo, as permissões de acesso ao relatório, configurações de RLS e permissões são herdadas do grupo, que se somam com as permissões que o usuário já possui.

<figure><img src="../../../.gitbook/assets/grupos (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Você também pode gerenciar a associação entre Usuários e Grupos na tela de gerenciamento de grupos, só que o contexto passa a ser o grupo específico e não o usuário.
{% endhint %}

### Relatórios

Aqui você associa o usuário a um ou mais relatórios. Nem os usuários administradores possuem acesso aos relatórios importados automaticamente. Todo acesso a relatório deve ser explícito.

Para liberar acesso ao relatório, basta marcar o relatório e depois clicar no botão "Salvar".

Para remover o usuário ao relatório, basta desmarcar o relatório e depois clicar no botão "Salvar".

<figure><img src="../../../.gitbook/assets/relatorios.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Você também pode gerenciar as permissões do relatório na tela de gerenciamento de relatórios, só que o contexto passa a ser o relatório específico e não o usuário.
{% endhint %}

### Empresas

Nesta aba, você define a empresa à qual o usuário estará associado.

Isso afeta a identidade visual do usuário dentro da aplicação. Para associar a identidade visual de uma empresa ao usuário, basta vinculá-lo a essa empresa. [Saiba mais](https://powerembedded.com.br/ajuda-cadastro-de-empresas/)

<figure><img src="../../../.gitbook/assets/empresas.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Você também pode gerenciar a associação entre usuário e empresa na tela de gerenciamento de empresas, só que o contexto passa a ser a empresa específica e não o usuário.
{% endhint %}

{% hint style="warning" %}
A associação do usuário com a empresa não tem influência nas permissões de acesso do usuário com o relatório, nem com o RLS ou permissões. Serve apenas para filtragens e para controlar a identidade visual do portal de acordo com a empresa do usuário.

Caso o usuário esteja em mais de uma empresa ou em nenhuma, a identidade visual será herdada das configurações gerais da organização.
{% endhint %}



### Assistentes

Se você estiver utilizando assistentes do Power Pilot (IA Generativa) no Power Embedded, essa aba permite definir quais assistentes estarão disponíveis para o usuário.

Nesta tela você especifica quais assistentes podem ser utilizados pelo usuário. [O que é um assistente](https://powerembedded.com.br/power-pilot-ia/)

<figure><img src="../../../.gitbook/assets/assistentes.png" alt=""><figcaption></figcaption></figure>

### IA

Se você utiliza um assistente do Power Pilot no Power Embedded,  nessa aba é possível estipular um valor em dólar para esse determinado usuário utilizar mensalmente.&#x20;

<figure><img src="../../../.gitbook/assets/IA.png" alt=""><figcaption></figcaption></figure>



## Email de boas-vindas ao cadastrar o usuário

Ao cadastrar um usuário, seja clicando no botão “Criar usuário” ou “importar um arquivo CSV”, é possível enviar um e-mail de boas-vindas para o novo usuário.

Para ativar essa funcionalidade, marque a caixa de seleção “Enviar e-mail de boas-vindas”.

<div align="left"><figure><img src="../../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure></div>

Quando essa opção estiver **habilitada**, o e-mail de boas-vindas será enviado automaticamente ao novo usuário.

Se o usuário for utilizar o método de login com nome de usuário e senha, ele poderá criar sua própria senha através do e-mail que receberá ao clicar em “Registrar”.

<figure><img src="../../../.gitbook/assets/image (179).png" alt=""><figcaption><p>Exemplo de email de boas-vindas</p></figcaption></figure>

{% hint style="info" %}
Caso o usuário criado tenha permissão diferente de "Visualizador", no email de boas-vindas será incluído o link para entrar no portal de administração.
{% endhint %}

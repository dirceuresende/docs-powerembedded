# Criar/editar grupo

{% embed url="https://www.youtube.com/watch?v=TEDkZXwdV5M" %}

Se você precisa gerenciar seus usuários de forma mais eficiente e centralizar a administração em um único local, você está no lugar certo. A seguir, apresentamos uma documentação detalhada sobre os tipos de cadastros de grupos disponíveis na aplicação e a possibilidade de sincronização com grupos existentes no Entra ID (Azure AD)

A plataforma oferece quatro métodos para criar grupos, descritos a seguir:

1. **Importar via Entra ID**: Integre diretamente com o Entra ID para criar grupos a partir dos dados existentes.
2. Sincronizar via Entra ID: Integre diretamente com o Entra ID de forma recorrente para criar grupos a partir dos dados existentes conforme as mudanças que ocorrem no Entra ID.
3. **Importar Arquivo CSV**: Importe grupos de um arquivo CSV, facilitando a inclusão em massa.
4. **Criar Grupo Manualmente**: Crie grupos diretamente na plataforma, com controle total sobre as configurações.
5. **Cadastrar Usuário via API**: Utilize chamadas à API para criar e gerenciar grupos, ideal para integrações automatizadas.

Esses métodos proporcionam flexibilidade para adaptar a gestão de grupos às suas necessidades específicas.



### Geral

Nesta aba, você pode cadastrar o nome e descrição do grupo (ambos obrigatórios), página inicial após o login e o método de autenticação a ser utilizado.

<figure><img src="../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

* **Data de validade**: Defina uma data de validade para o usuário. Após essa data, o usuário não poderá acessar o sistema.
* **Página inicial após login**: Selecione uma página ou relatório específico para o usuário ser redirecionado imediatamente após o login. Certifique-se de que o usuário tenha acesso ao relatório ou aplicativo selecionado.
* **Método de autenticação**: Escolha o método de autenticação que o usuário deve usar.



### Permissões

Nesta aba, você define as permissões que o grupo irá conceder para os usuários que fazem parte dele ao visualizar um relatório.

<figure><img src="../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
As permissões concedidas para o grupo só afetam os usuários nos relatórios que esse grupo possui acesso. Se quiser liberar uma permissão para o usuário em todos os relatórios que tem acesso, as permissões aplicadas diretamente no usuário são aplicadas em TODOS os relatórios que esse usuário tenha acesso.
{% endhint %}



### Relatórios

Aqui você associa o grupo a um ou mais relatórios, para que esse grupo libere acesso neste relatório para os usuários que fazem parte do grupo.

Para liberar acesso ao relatório, basta marcar o relatório e depois clicar no botão "Salvar".

Para remover o usuário ao relatório, basta desmarcar o relatório e depois clicar no botão "Salvar".

<figure><img src="../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Você também pode gerenciar as permissões do relatório na tela de gerenciamento de relatórios, só que o contexto passa a ser o relatório específico e não o grupo.
{% endhint %}



### Usuários

Aqui você associa o grupo a um ou mais usuários.

Para adicionar o usuário ao grupo, basta marcar os usuários e depois clicar no botão "Salvar".

Para remover o usuário do grupo, basta desmarcar os usuários e depois clicar no botão "Salvar".

Quando o usuário faz parte de um grupo, as permissões de acesso ao relatório, configurações de RLS e permissões são herdadas do grupo, que se somam com as permissões que o usuário já possui.

<figure><img src="../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Você também pode gerenciar a associação entre Usuários e Grupos na tela de [Gerenciamento de Usuários](../usuarios/), só que o contexto passa a ser o usuário específico e não o grupo.
{% endhint %}



### Assistentes

Se você estiver utilizando assistentes do Power Pilot (IA Generativa) no Power Embedded, essa aba permite definir quais assistentes estarão disponíveis para o grupo.

Nesta tela você especifica quais assistentes podem ser utilizados pelo grupo. [O que é um assistente](https://powerembedded.com.br/power-pilot-ia/)

<figure><img src="../../.gitbook/assets/image (185).png" alt=""><figcaption></figcaption></figure>

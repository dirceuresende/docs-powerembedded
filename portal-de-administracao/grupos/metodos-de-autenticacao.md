# Métodos de autenticação

Com essa opção é possível definir quais os métodos de autenticação que cada grupo pode utilizar.

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Você  poderá ter diferentes métodos de autenticação conforme o grupos dos usuários, onde os membros do grupo “Colaboradores”, por exemplo, poderão autenticar apenas utilizando autenticação Microsoft, enquanto os membros do grupo “Usuários externos” poderão entrar com qualquer método de autenticação.



### Regras de prioridade e funcionamento

* Quando um método de autenticação está desmarcado na tela de Configurações, ele não será mostrado na tela de login e não poderá ser utilizado por nenhum usuário, mesmo que aquele método de autenticação esteja marcado para o usuário.
* Caso o método de autenticação esteja permitido na tela de Configurações, o sistema então verifica se o usuário pode utilizar o método de autenticação escolhido, validando essa propriedade no cadastro do usuário ou se o usuário faz parte de algum grupo que tenha essa permissão habilitada.
* Se nenhum método de autenticação estiver selecionado, todos estarão permitidos.
* Caso o usuário faça parte de algum grupo que não tenha nenhum método de autenticação habilitado, esse usuário poderá entrar no portal utilizando qualquer método de autenticação.


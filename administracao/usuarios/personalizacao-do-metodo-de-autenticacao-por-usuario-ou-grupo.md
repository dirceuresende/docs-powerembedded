# Personalização do método de autenticação por usuário ou grupo

O Power Embedded está sempre em evolução e buscando formas de melhorar a segurança dos seus relatórios.

Por conta disso, o Power Embedded permite escolher os métodos de autenticação suportados para acessar o portal de relatórios.

Os administradores do sistema podem definir os métodos de autenticação permitidos para o portal, onde o sistema irá mostrar na tela de login, apenas os botões permitidos na tela abaixo:

<figure><img src="../../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure>



Para personalizar ainda mais a segurança do sistema, o Power Embedded entrega mais um nível de configuração dos métodos de login, onde você pode definir quais os métodos de autenticação que cada usuário ou grupo pode utilizar.

<figure><img src="../../.gitbook/assets/image (364).png" alt=""><figcaption></figcaption></figure>

Com essa funcionalidade, você pode ter diferentes métodos de autenticação de acordo com o perfil dos usuários, onde os membros do grupo “Coordenadores”, por exemplo, poderão autenticar apenas utilizando autenticação Microsoft, enquanto os membros do grupo “Usuários externos” poderão logar no portal de relatórios utilizando qualquer método de autenticação suportado pelo Power Embedded.



### **Regras de prioridade e funcionamento**

* A maior prioridade é da da tela de Configurações. Caso a autenticação Microsoft não esteja marcada, ela não será permitida, mesmo que ela esteja marcada no usuário ou grupo.
* A verificação se o usuário pode utilizar um método de autenticação valida essa propriedade no cadastro do usuário ou se o usuário faz parte de algum grupo que tenha essa permissão habilitada.
* Caso nenhum método de autenticação seja selecionado, todos estarão permitidos.
* Caso o usuário faça parte de algum grupo que não tenha nenhum método de autenticação habilitado, esse usuário poderá logar no portal utilizando qualquer método de autenticação.

# Autenticação de 2 fatores

### Introdução

Um dos pilares do Power Embedded desde a sua primeira versão sempre foi a segurança do acesso aos dados e relatórios.

Visando garantir a melhor segurança e governança possível em termos de autenticação dos usuários, o sistema oferece autenticação integrada com Microsoft e Google utilizando o protocolo OAuth2, de modo que o usuário não precisa criar mais uma senha, pois é utilizada a mesma senha do provedor de identidade e ao bloquear/remover esse usuário no Entra ID ou Google Workspace, o acesso é automaticamente bloqueado também no Power Embedded.

Para ser possível o acesso aos relatórios por usuários externos, como clientes e fornecedores, o Power Embedded também permite o acesso ao sistema utilizando autenticação interna com email e senha de acesso, onde bastava informar esses dados para conseguir acessar os relatórios.

Para aumentar a segurança dos usuários que utilizam email e senha para entrar no portal, **foi implementado a autenticação de dois fatores** no portal de visualização.

Uma vez ativado no usuário em questão, ao fazer login com email e senha, será enviado um email com o código de confirmação, que deverá ser informado para completar o processo de Login no sistema.

Essa medida garante uma camada extra de segurança para proteger as informações dos usuários.



### Como ativar a autenticação de 2 fatores (MFA)

Para ativar essa opção, basta ir no Portal de Administração > Usuários ou [clicar aqui](https://admin.powerembedded.com.br/Users).

Clique no botão Ações > Editar.

Agora ative a opção _**Autenticação de 2 fatores ao logar utilizando email e senha**_.

<figure><img src="../../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>



### Exemplo prático

Ao ativar a autenticação de dois fatores, sempre que o usuário fizer login no portal de relatórios usando email e senha, será enviado um código de verificação para o seu e-mail.

<figure><img src="../../.gitbook/assets/image (177).png" alt=""><figcaption></figcaption></figure>



Após receber o email com o código de acesso, o usuário deverá inserir o código nesta tela e clicar no botão _**Validar código**_ para continuar o processo de login.

<figure><img src="../../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Caso o usuário utilize a autenticação Microsoft ou Google, essa permissão não terá efeito, pois o acesso é validado pelo provedor de identidade e as configurações de MFA são gerenciadas pelos responsáveis de segurança / TI da sua empresa.



Devido a disso, caso a sua empresa force o uso de MFA, você precisará confirmar o código pelo método de MFA utilizado para conseguir autenticar no Power Embedded.
{% endhint %}

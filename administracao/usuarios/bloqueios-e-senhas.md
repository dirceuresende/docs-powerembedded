# Bloqueios e senhas

### Portal de Administração

No portal é possível o administrador realizar várias ações administrativas com os usuários, como criar/alterar senha, bloquear/desbloquear o usuário e muito mais.

* **Criar Senha:** Permite que o administrador possa criar manualmente uma senha para o usuário em questão digitando numa tela. Não é permitido a criação de senhas fracas.
* **Alterar Senha:** Permite que o administrador possa alterar manualmente uma senha para o usuário em questão digitando numa tela. Não é permitido a criação de senhas fracas.
* **Redefinir Senha:** Permite que o administrador possa solicitar o envio de um email para que o próprio usuário altere a sua senha de acesso.
* **Bloquear:** Bloqueia o acesso do usuário ao sistema e ao portal de relatórios. Vale lembrar que mesmo bloqueado, o usuário continua sendo cobrado até ser removido.
* **Desbloquear Senha:** Permite remover o bloqueio temporário de 30 minutos que o sistema adiciona automaticamente sempre que um usuário erra a senha 5 vezes seguidas.

{% hint style="warning" %}
A melhor opção para autenticação do Power Embedded é utilizando a autenticação integrada (Google e Microsoft), pois o sistema não precisa gerenciar senhas, já tem MFA integrado e caso a conta seja bloqueada no diretório da empresa, o acesso é bloqueado automaticamente.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (174).png" alt=""><figcaption></figcaption></figure>



### Autogerenciamento de senhas

Embora o Administrador do Power Embedded possa criar/alterar senha para o usuário e forçar a redefinição da senha, o sistema permite que o próprio usuário faça o autogerenciamento da sua senha, para criar uma senha para o primeiro acesso e também para redefinir/recuperar a sua senha.

<figure><img src="../../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Lembre-se: A melhor opção para autenticação do Power Embedded é utilizando a autenticação integrada (Google e Microsoft), pois o sistema não precisa gerenciar senhas, já tem MFA integrado e caso a conta seja bloqueada no diretório da empresa, o acesso é bloqueado automaticamente.
{% endhint %}



### Usuário esqueceu a senha

Na opção de "[Esqueceu a senha?](https://relatorios.powerembedded.com.br/Identity/ForgotPassword)", o próprio usuário poderá digitar o seu email e o Power Embedded irá enviar por email, um link de redefinição de senha, onde o usuário irá clicar no link e digitar sua nova senha para acessar o portal.

<div align="left">

<figure><img src="../../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

</div>



### Criar senha para primeiro acesso

Caso o usuário tenha sido recém criado no portal e o administrador não tenha definido nenhuma senha para este usuário, a própria pessoa poderá clicar no link "[Criar senha para primeiro acesso](https://relatorios.powerembedded.com.br/Identity/Register)"

Nesta tela, o usuário poderá digitar o email cadastrado e criar uma nova senha para acessar o portal. Senhas fracas não serão aceitas.

<div align="left">

<figure><img src="../../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="warning" %}
O usuário não poderá se cadastrar no sistema utilizando esse link. Essa tela serve apenas para que o próprio usuário possa criar a sua senha no primeiro acesso, mas o usuário precisa ter sido criado previamente no [Portal de Administração](https://admin.powerembedded.com.br/).
{% endhint %}

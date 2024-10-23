# Atualização de token

### Por que o token expira

Quando um usuário está com a tela aberta em um relatório por mais de 1 hora sem interagir com o relatório, esse token de autenticação expira e você poderá ver uma mensagem de erro "ClientError\_TokenExpired" após esse tempo.

Caso o usuário veja essa mensagem de erro, a solução é bem simples: Basta atualizar a página que o relatório será carregado novamente.

O token do **Power BI Embedded** expira para manter a segurança e controlar quem pode acessar os relatórios. Como ele permite acesso temporário, a expiração evita que alguém continue usando o sistema se o token for compartilhado ou exposto por acidente. Além disso, essa medida garante que, se houver mudanças nas permissões ou necessidade de bloquear um acesso, isso aconteça rapidamente, sem deixar brechas.

Por padrão, o token da API do Power BI Embedded tem validade de **1 hora**. Esse tempo é pensado para ser suficiente para uma sessão de uso normal, mas curto o bastante para evitar riscos. Se for necessário continuar usando o sistema após esse período, um novo token precisa ser gerado pela aplicação. Isso mantém o acesso sempre atualizado e seguro.



### Atualização de token automática

O Power Embedded possui um recurso que atualiza os tokens de acesso automaticamente quando você interage com o relatório, como aplicar um filtro, trocar uma página do relatório ou clicar em um visual.

Entretanto, caso o usuário fique mais de 1 hora sem interagir com o relatório (ex: relatório em uma TV), o token pode expirar, mostrar a mensagem de erro de token expirado e você ter que atualizar a página.

Para resolver esse problema, o Power Embedded implementou a atualização de token temporizada.



### Atualização de token temporizada

Para forçar a atualização temporizada do token de autenticação do Power Embedded, acesse a página de **Configurações.**

Nesta tela, temos a opção de **“Atualizar Token a cada” x minutos**. Essa opção fará com que o Power Embedded force a atualização do token na quantidade de minutos selecionada.

Caso o usuário deixe a tela aberta, sem interagir com o relatório, o token pode expirar. Configurar esta opção permite atualizar o token periodicamente, evitando desconexões por expiração, mesmo que o relatório esteja ocioso.



#### Como configurar a atualização de token temporizada

1. Acesse o **Portal de Administração**.
2. Navegue até a página de **Configurações**.
3. Localize a opção **“Atualizar token a cada”**.
4. Defina o intervalo de tempo desejado e clique em **Salvar**.

<figure><img src="../../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
**ATENÇÃO**: Caso você tenha configurado para a capacidade desligar automaticamente baseado na inatividade de X minutos, **essa configuração irá impedir** que a capacidade seja desligada.



Uma alternativa para isso é configurar que apenas alguns usuários possam ligar ou manter a capacidade ligada.
{% endhint %}


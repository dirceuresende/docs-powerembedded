# Este relatório possui Row-level security (RLS) habilitado e o usuário não está associado

<figure><img src="../../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
Este relatório possui Row-level security (RLS) habilitado e o usuário atual '%User%' não está associado à nenhuma regra de segurança.
{% endhint %}

Esse erro é bem comum e acontece quando um relatório possui segurança a nível de linha (RLS), mas o usuário que está tentando acessar o relatório não está associado a nenhuma regra do RLS.

{% hint style="warning" %}
Diferente do Power BI serviço, onde os usuários administradores não são afetados pelo RLS, no Power Embedded, TODOS os usuários são afetados pelo RLS.

Se um usuário administrador não estiver em nenhuma regra de segurança, irá receber essa mensagem de erro acima. Caso esse usuário precise visualizar todos os dados, crie uma regra de segurança sem nenhum filtro e associe o usuário à essa regra de segurança.
{% endhint %}



### Como gerenciar as regras de RLS

Para associar um usuário a uma regra de RLS, você tem 3 formas de fazer essa configuração:

1.  Na tela de [Relatórios](https://admin.powerembedded.com.br/Reports), pesquise o relatório que deseja gerenciar as regras de RLS, clique no botão **Ações** e depois clique no item **Segurança.** \
    \
    Se o relatório tiver RLS e esse botão não estiver aparecendo, entre na página de [**Conjuntos de dados**](https://admin.powerembedded.com.br/Datasets) e clique no botão **Recarregar.**\
    \


    <figure><img src="../../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure>


2.  Na página de [Relatórios](https://admin.powerembedded.com.br/Reports), pesquise o relatório que deseja gerenciar as regras de RLS, clique no botão **Ações** e depois clique no item **Editar.** \
    \
    Você deverá ver um botão amarelo chamado **Editar RLS.** Se o relatório tiver RLS e esse botão não estiver aparecendo, entre na página de [**Conjuntos de dados**](https://admin.powerembedded.com.br/Datasets) e clique no botão **Recarregar**\
    \


    <figure><img src="../../.gitbook/assets/image (341).png" alt=""><figcaption></figcaption></figure>


3.  Na página de [**Conjuntos de dados**](https://admin.powerembedded.com.br/Datasets), pesquise o conjunto de dados que deseja gerenciar as regras de RLS, clique no botão **Ações** e depois clique no item **Segurança.**\
    \


    <figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>



Na página de Segurança, você poderá configurar as regras de segurança a nível de linha (RLS) ou a nível de objeto/tabela/coluna (OLS).

{% hint style="info" %}
Para saber mais sobre essa configuração, acesse o artigo [Segurança (RLS)](../../portal-de-administracao/power-bi/relatorios/seguranca-rls/).
{% endhint %}

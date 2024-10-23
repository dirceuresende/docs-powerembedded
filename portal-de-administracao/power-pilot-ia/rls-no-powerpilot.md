# RLS no PowerPilot

Para restringir acesso a determinados dados do relatório com base nas credenciais dos usuários, agora o Power Pilot também oferece suporte para Row Level security (RLS).&#x20;

Com isso, se seu conjunto de dados estiver configurado com a função DAX CUSTOMDATA() e os usuários tiverem acesso ao Power Pilot, os filtros de segurança serão aplicados, garantindo que cada usuário veja apenas as informações pertinentes a ele, o que reforça a segurança dos dados.



### Como Funciona

Diferente da RLS padrão, que utiliza as funções USERNAME() ou USERPRINCIPALNAME(), o Power Pilot utiliza a função CUSTOMDATA(). Esta função é fácil de configurar e permite um controle eficaz sobre os dados visíveis para cada usuário.



### Configuração no Power BI Desktop

No Power BI Desktop, são necessárias duas configurações de RLS:

1° Regra: Utilize as funções USERNAME() ou USERPRINCIPALNAME() para criar filtros baseados em uma tabela de usuários. Esta configuração é essencial para a RLS dinâmica.

2 ° Regra: Utilize a mesma tabela para filtrar porém agora passe a função CUSTOMDATA() para aplicar o filtro.

{% hint style="warning" %}
A configuração da RLS dinâmica é um pré-requisito para a configuração da CUSTOMDATA(). A RLS estática não é compatível com este cenário.
{% endhint %}



**Configuração da RLS Dinâmica:** Configure a RLS dinâmica passando USERNAME() ou USERPRINCIPALNAME() como função.

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>



**Configuração da RLS para o Power Pilot:** Utilize a função CUSTOMDATA().

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

Com as RLS criada basta publicar o relatório no Power Bi serviço.



### Configuração no Power Embedded

Para configurar a RLS do Power Pilot vá ao portal de administração, Artefatos > Conjuntos de dados > Recarregar

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

Feito o processo de recarregar o conjunto de dados, busque pelo conjunto de dados que foi configurado o RLS, clique em Ações > Segurança.



Para configurar a regra, siga duas etapas:

1° Etapa: No menu de Segurança Dinâmica, selecione a função configurada.

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

No menu de Segurança Power Pilot, selecione a função CUSTOMDATA().

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

Após essas configurações, o Power Pilot estará com a RLS devidamente configurada e cada usuário verá apenas as informações pertinentes a ele.

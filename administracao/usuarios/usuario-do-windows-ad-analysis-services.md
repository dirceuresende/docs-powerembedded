# Usuário do Windows AD (Analysis Services)

Ao utilizar o Analysis Services e implementar uma regra de RLS (Row-Level Security), é comum enfrentar o desafio de ter que mapear usuários individualmente no Power BI.&#x20;

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Mapeamento que você precisa fazer para cada usuário, em cada cubo do SSAS</p></figcaption></figure>



Caso você não faça esse mapeamento, você irá ver a seguinte mensagem de erro no Power BI ao tentar acessar o relatório que está conectado ao Analysis Services (SSAS):

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

Esse processo se torna ainda mais complexo quando há múltiplos cubos, exigindo a configuração repetitiva para cada cubo, o que pode ser um tanto trabalhoso quanto propenso à erros.

Para acessar um relatório que esteja utilizando um Analysis Services no Power BI serviço, você tem que configurar um mapeamento de usuários, informando o usuário do Entra ID (usuario@dominio.com.br) e o usuário do Windows Active Directory (DOMINIO\usuario) para cada usuário e em cada cubo que for acessar.

Se você tem 100 usuários e 20 cubos, vai precisar criar 2.000 mapeamentos! E não existe API do Power BI para automatizar isso.



### Power Embedded sempre inovando

Para melhorar a experiência dos nossos usuários, o Power Embedded está introduzindo melhorias significativas para simplificar essa configuração.

Na tela de criação/edição de um usuário, você pode informar o nome de usuário do Windows Active Directory (AD) para este usuário.

<figure><img src="../../.gitbook/assets/image (362).png" alt=""><figcaption></figcaption></figure>

Ao acessar um relatório que utilize uma fonte de dados do tipo “AnalysisServices”, o Power Embedded vai informar esse usuário do Windows AD, eliminando a necessidade de configurar manualmente o mapeamento do usuário no Power BI serviço para cada usuário/cubo.

Com a nova funcionalidade, uma vez que o campo “Usuário do Windows AD” é preenchido, o Power Embedded aplica automaticamente essa configuração para todos os cubos acessíveis deste usuário, reduzindo significativamente a complexidade e o esforço necessário para manter a segurança dos dados.

Embora o Power BI não tenha uma API para automatizar esse mapeamento de usuários, no Power Embedded [existe uma API](https://api.powerembedded.com.br/) onde você pode automatizar o cadastro/alteração de usuários e informar o valor deste campo.

Essas melhorias não apenas otimizam a administração de segurança, mas também reduzem a carga de trabalho associada à configuração e manutenção de RLS em ambientes complexos e de grande escala, proporcionando uma gestão de dados mais eficiente e menos sujeita a erros.

{% hint style="warning" %}
**Observação:** Essa funcionalidade tem prioridade sobre a configuração de fixação de usuários por empresa no cadastro das Fontes de Dados ([Ajuda – Fontes de dados](https://docs.powerembedded.com.br/administracao/artefatos/fontes-de-dados)). Com esse campo preenchido, o sistema usará esse valor no mapeamento do AD do usuário e ignora a configuração de fixação de usuários.
{% endhint %}



### Adicionar permissão de Administrador ao Gateway

Para ser possível utilizar corretamente os gateways para acessar o Power Embedded e implementar o RLS, é necessário liberar uma permissão para o usuário do aplicativo (PowerEmbedded-App) no Power BI Serviço.

Acesse a tela de [Gerenciar conexões e gateways](https://app.powerbi.com/groups/me/gateways) e clique na opção _**Gerenciar gateways de dados locais.**_

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Agora você irá clicar nas 3 elipses (…) ao lado do gateway que deseja liberar a permissão e selecionar a opção Gerenciar Usuários.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Na tela de gerenciamento de usuários, pesquise pelo nome do aplicativo que você está utilizando no Power Embedded (o nome padrão é _PowerEmbedded-App_), marque a permissão de Administrador e clique no botão **Share**.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Agora repita esse processo para todos os gateways que você precisar gerenciar e acessar dados pelo Power Embedded, **especialmente se for utilizar conexão com o Analysis Services (SSAS).**

{% hint style="warning" %}
**IMPORTANTE:** Não é necessário alterar as permissões nas fontes de dados, uma vez que o usuário do Power Embedded já possui permissão de administrador no Gateway.

Isso reduz bastante o esforço de ter que configurar essas permissões em cada um das fontes de dados, uma vez que a quantidade de fontes de dados é bem maior que a quantidade de gateways.
{% endhint %}

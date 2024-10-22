# Google Analytics

Já imaginou poder analisar o comportamento dos seus usuários e extrair insights valiosos, como: quais relatórios eles acessam com mais frequência, quanto tempo passam em cada página, qual menu é o mais acessado, até onde eles rolam a tela e outros eventos importantes?&#x20;

Isso é possível graças à integração que o Power Embedded oferece com o Google Analytics. Descubra mais sobre a usabilidade do seu portal através dessa ferramenta poderosa.

Abaixo, você encontrará uma documentação completa com um passo a passo detalhado para configurar e utilizar essa integração de forma eficaz.&#x20;

Aproveite para explorar todas as funcionalidades e otimizar a experiência do usuário em seu portal.



### Configurando o Google Analytics

Vamos dividir o processo em alguns passos para tornar a configuração o mais fácil possível.

<details>

<summary>NÃO tenho conta do Google Analytics</summary>



Para criar sua conta do Google Analytics e começar a coletar os dados do seu sistema, siga os passos abaixo:

Acesse o link: [analytics.google.com/analytics/web](https://analytics.google.com/analytics/web).

Clique em “Começar a medir”.

<img src="../../../.gitbook/assets/image (158).png" alt="" data-size="original">

Defina um nome para sua conta. As permissões padrão geralmente são suficientes, então mantenha as configurações padrão e clique em próximo.

<img src="../../../.gitbook/assets/image (159).png" alt="" data-size="original">

**Passo 2: Configuração da Propriedade**

1. Defina um nome para sua propriedade.
2. Configure o fuso horário (deixe como Brasil, se aplicável). A configuração da moeda não é necessária para esta integração, mas você pode configurá-la se desejar.
3. Clique em “Próximo”.

<img src="../../../.gitbook/assets/image (160).png" alt="" data-size="original">

**Passo 3: Configuração do Negócio**

1. Defina os detalhes do negócio e clique em próximo.

<img src="../../../.gitbook/assets/image (161).png" alt="" data-size="original">

**Passo 4: Objetivos do negócio**

1. Escolha a opção “Examine o comportamento do usuário” como o objetivo principal desta configuração.

<img src="../../../.gitbook/assets/image (162).png" alt="" data-size="original">

Selecione o Brasil e clique em “Aceitar” para prosseguir.&#x20;

<img src="../../../.gitbook/assets/image (163).png" alt="" data-size="original">

Na etapa seguinte, escolha a opção “Rede” ou “Web” (em inglês, “Web”).

<img src="../../../.gitbook/assets/image (164).png" alt="" data-size="original">

**Passo 5: Preenchimento da URL**

1. Preencha o campo de URL do site com o subdomínio utilizado para acessar o portal de relatórios do Power Embedded.
2. Dê um nome para esse fluxo e clique em Criar e continuar

<img src="../../../.gitbook/assets/image (165).png" alt="" data-size="original">

Nessa aba, antes de clicar em “Próximo”, clique sobre a propriedade criada para pegar o código de rastreamento do Google Analytics.

<img src="../../../.gitbook/assets/image (166).png" alt="" data-size="original">

Você será redirecionado para essa página, onde está disponível o código de rastreamento.

<img src="../../../.gitbook/assets/image (168).png" alt="" data-size="original">

</details>

<details>

<summary>Já tenho conta do Google Analytics</summary>



Se você já possui uma conta do Google Analytics e quer criar uma nova propriedade para começar a coletar os dados do seu sistema, siga os passos abaixo:

Acesse o link: [https://analytics.google.com/analytics/web](https://analytics.google.com/analytics/web).

Clique no botão _Administrador_, na parte inferior da página

<img src="../../../.gitbook/assets/image (169).png" alt="" data-size="original">

Clique no botão _Criar_ e depois _Propriedade_.

<img src="../../../.gitbook/assets/image (170).png" alt="" data-size="original">

Na tela de _Criação de propriedade_, digite o nome da propriedade (Nome do seu site) e configure o País, fuso horário e moeda

<img src="../../../.gitbook/assets/image (171).png" alt="" data-size="original">

Na detalha de _Detalhes comerciais_, informe o setor e tamanho da sua empresa

<img src="../../../.gitbook/assets/image (172).png" alt="" data-size="original">

Na tela de _Objetivos de negócios_, selecione o objetivo de usar o Google Analytics no seu site

<img src="../../../.gitbook/assets/image (149).png" alt="" data-size="original">

Na tela de _Coleta de dados_, selecione a opção _Web_

<img src="../../../.gitbook/assets/image (151).png" alt="" data-size="original">

Ao clicar no botão, vai abrir a tela de _Configurar fluxo de dados_. Preencha com a URL do seu site e o nome do seu site e depois clique no botão _Criar e continuar_.

<img src="../../../.gitbook/assets/image (152).png" alt="" data-size="original">

Na tela de _Configurar uma tag do Google_, marque a opção Instalar manualmente e você irá encontrar o código JavaScript para inserir o código de rastreamento no seu site (caso ainda não tenha).

No trecho marcado, você irá encontrar o código de rastreamento do Google Analytics, que você precisará copiar e inserir no Power Embedded para rastrear o comportamento dos usuários no portal de visualização.

<img src="../../../.gitbook/assets/image (153).png" alt="" data-size="original">

</details>



### Como configurar no Power Embedded

Com esse valor do código do Google Analytics copiado, basta ir no portal do portal de administração do Power Embedded > Configurações e colar no campo “Código de rastreamento do Google Analytics”.

<figure><img src="../../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>



### Como visualizar os dados

Para visualizar os dados coletados no site do Google Analytics, acesse a página inicial.

Caso você tenha acabado de criar a propriedade, não vai conter dado nenhum, pois o código de rastreamento não captou nada ainda, é exibido um aviso como o da tela abaixo.

<figure><img src="../../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

Após realizar alguns acessos no portal de visualização, o Google Analytics passará a criar as métricas no dashboard e o aviso na tela irá mudar.

<figure><img src="../../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

Com o rastreamento funcionando, basta ir fazendo suas análises sobre o comportamento dos usuários.&#x20;

Uma visão muito interessante de analisar é ver em tempo real, que possibilita ter uma visão ampla dos dados e dos principais eventos.

<figure><img src="../../../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

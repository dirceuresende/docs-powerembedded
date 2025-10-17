# Você atingiu o limite de uso de uma capacidade compartilhada (Pro ou PPU) para embeddar relatórios

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### O que essa mensagem de erro significa

Se você está visualizando essa mensagem de erro no portal de relatórios ao tentar acessar um relatório, isso quer dizer que esse relatório ou o conjunto de dados que o relatório utiliza, está em um workspace que **não** está utilizando uma capacidade dedicada (Fabric ou Power BI Embedded).

Provavelmente, o workspace do relatório ou conjunto de dados está associado com uma capacidade Pro ou Premium por usuário, e a quantidade de tokens desse usuário atingiu o limite de uso.

<figure><img src="../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>



### Como corrigir o problema

Quando esse limite é atingido, não é possível gerar novos tokens de incorporação com essa conta.&#x20;

Para voltar a renderizar os relatórios, **você precisará contratar uma capacidade** ou iniciar um período de avaliação do Fabric, caso ainda tenha disponibilidade para algum usuário na sua empresa.

Se você precisar de ajuda para realizar esse processo de contratação de capacidade, alteração do workspace e tiver outras dúvidas, entre em contato com o time de suporte através do grupo de comunicação criado na instalação, ou [envie um email para a gente](mailto:suporte@powerembedded.com.br) ou [abra um chamado](https://admin.powerembedded.com.br/Support).

Se você não tem um parceiro Microsoft para contratar as licenças do Power BI, qualquer outra licença Microsoft, capacidades do Fabric ou qualquer outro recurso no Azure, [acesse essa página aqui](https://powertuning.com.br/parceria-azure/) para entender como a Power Tuning pode ajudar a sua empresa a reduzir custoso com o Azure.



### O que a Microsoft diz sobre isso

Conforme está explicado no artigo [Perguntas frequentes sobre licenciamento](../../perguntas-frequentes/licenciamento/), é possível utilizar uma capacidade Pro ou Premium por Usuário para gerar tokens para inserir os relatórios no Power Embedded, mas de acordo com a [documentação oficial da Microsoft:](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/move-to-production)

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



A página de [perguntas e respostas do Power BI Embedded](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#quantos-tokens-inseridos-posso-criar-) reafirma que contas Pro não podem ser utilizadas para soluções de Embedded em produção:

<figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>



A página [Cenários de uso do Power BI: inserir para clientes – Power BI | Microsoft Learn](https://learn.microsoft.com/pt-br/power-bi/guidance/powerbi-implementation-planning-usage-scenario-embed-for-your-customers#licensing) também reforça que o uso de uma capacidade é obrigatório para utilizar tecnologias de Embedded

<figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>



Além disso, o conteúdo que será mostrado na aplicação NÃO PODE estar em um workspace pessoal

<figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
**Caso você esteja utilizando uma plataforma que utilize uma conta Pro para gerar os tokens de inserção de relatórios, sem utilizar uma capacidade para isso, você provavelmente está violando os termos de uso do Power BI e sua empresa pode sofrer multas e sanções pela Microsoft.**
{% endhint %}


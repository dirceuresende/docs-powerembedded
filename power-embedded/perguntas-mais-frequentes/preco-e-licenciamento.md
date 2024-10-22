# Preço e Licenciamento

### Quanto custa o Power Embedded?

Para ter acesso ao Power Embedded e começar a economizar no licenciamento de Power BI, você precisará fazer apenas 3 investimentos, sendo 2 mensais e 1 que você irá pagar única vez, que são:

\
**Investimento único**

* R$ 1.500,00 para instalação e configuração inicial do ambiente.

**Investimentos mensais**

* A partir de R$ 427,54 pelo licenciamento da capacidade, variando conforme necessidade.
* R$ 5,00 por usuário que você criar no sistema.

{% hint style="info" %}
Para acessar a calculadora e gerar um orçamento, acesse a página da [Calculadora](https://powerembedded.com.br/calculadora).
{% endhint %}



Valores estimados das capacidades do Fabric e Power BI Embedded (considerando escala 12x5)

<figure><img src="../../.gitbook/assets/Preço das Capacidades.png" alt=""><figcaption></figcaption></figure>



### Posso utilizar o Power BI Pro ou Premium por Usuário para Embeddar?

Sim, é possível gerar tokens para Embeddar relatórios em uma capacidade Pro ou Premium por Usuário, mas de acordo com a [documentação oficial da Microsoft:](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/move-to-production)

“Os tokens incorporados com licença Pro ou Premium por usuário (PPU) destinam-se a testes de desenvolvimento, portanto, uma conta mestra ou Service Principal do Power BI só pode gerar um número limitado de tokens.

Adquira uma capacidade para incorporação em um ambiente de produção. Não há limite para quantos tokens incorporados você pode gerar ao comprar uma capacidade.

Nos testes de desenvolvimento, você pode usar tokens de avaliação incorporados gratuitos com uma licença Pro. **Para incorporar em um ambiente de produção, você deve adquirir uma capacidade.**

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/05/Power-Embedded-Mover-aplicacao-para-producao.png" alt=""><figcaption></figcaption></figure>

&#x20;

A página de [perguntas e respostas do Power BI Embedded](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#quantos-tokens-inseridos-posso-criar-) reafirma que contas Pro não podem ser utilizadas para soluções de Embedded em produção:

“Os tokens inseridos com a licença Pro ou PPU (Premium por usuário) destinam-se para teste de desenvolvimento, portanto, uma conta mestre ou [entidade de serviço](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embed-service-principal) do Power BI pode gerar apenas um número limitado de tokens. [Compre uma capacidade](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#technical) para inserir em um ambiente de produção. Não há limites para a quantidade de tokens inseridos que você pode gerar ao comprar uma capacidade. Em testes de desenvolvimento, você pode usar tokens de avaliação de inserção gratuitos com uma licença Pro. Para fazer uma inserção em um ambiente de produção, você deve comprar uma capacidade."

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded-3.png" alt=""><figcaption></figcaption></figure>

&#x20;

A página [Cenários de uso do Power BI: inserir para clientes – Power BI | Microsoft Learn](https://learn.microsoft.com/pt-br/power-bi/guidance/powerbi-implementation-planning-usage-scenario-embed-for-your-customers#licensing) também reforça que o uso de uma capacidade é obrigatório para utilizar tecnologias de Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded.png" alt=""><figcaption></figcaption></figure>



Além disso, o conteúdo que será mostrado na aplicação NÃO PODE estar em um workspace pessoal

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded-4.png" alt=""><figcaption></figcaption></figure>



**Caso você esteja utilizando uma plataforma que utilize uma conta Pro para gerar os tokens de inserção de relatórios, sem utilizar uma capacidade para isso, você provavelmente está violando os termos de uso do Power BI e sua empresa pode sofrer multas e sanções pela Microsoft.**



### Ainda preciso de licença Pro do Power BI, mesmo com Embedded?

Mesmo utilizando uma licença por capacidade do Power BI, seja o Power BI Embedded, o Fabric, ou até mesmo o Power BI Premium por capacidade (aquela que custa R$ 32.000,00 por mês), todos os usuários que publicam relatórios precisam de uma licença Pro ou PPU (Premium por usuário).

Para não precisar ter uma licença Pro para cada usuário que publique relatórios, uma alternativa é utilizar o Azure DevOps para a publicação automática com CI/CD, por exemplo, que a Power Tuning oferece suporte e pode ajudar a implantação desse processo na sua empresa através de consultoria.



### Eu não consigo compartilhar os relatórios sem pagar nenhuma licença?

Utilizando a licença gratuita do Power BI, você poderá utilizar o Power BI Desktop livremente, sem nenhuma limitação. E ainda poderá publicar os seus relatórios no seu workspace pessoal e testar à vontade.

A partir do momento em que você precisa compartilhar os relatórios com outras pessoas, a licença Pro se faz necessária, pois é através dela (ou de licenças mais caras) que você poderá compartilhar os relatórios.

As únicas formas de compartilhar relatórios sem precisar comprar uma licença de Power BI, é enviando o arquivo PBIX para a pessoa ou utilizando o recurso “Publicar na Web”, que permite compartilhar o relatório com qualquer pessoa que tenha acesso ao link do relatório, mas não possui nenhum tipo de segurança.

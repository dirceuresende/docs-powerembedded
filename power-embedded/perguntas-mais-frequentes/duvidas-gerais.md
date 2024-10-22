# Dúvidas gerais

### Como funciona essa economia do Power Embedded?

A economia do Power Embedded funciona assim: Ao invés de acessar o portal do Power BI (powerbi.com), exigindo assim uma licença para cada pessoa, os seus usuários irão acessar os relatórios pelo portal da Power Tuning, que não requer conta Microsoft e nem licença de Power BI, pois a capacidade contratada permite o acesso aos relatórios por meio de uma aplicação.

Sua empresa contrata uma capacidade dedicada com a Microsoft (Capacidade Fabric ou Embedded), através do portal do Azure, nós configuramos o sistema para integrar com o seu Power BI, utilizando uma conta de serviço da sua empresa (criada durante a instalação), e os seus usuários passam a acessar os relatórios pelo Power Embedded ao invés de usar o portal do Power BI.

Tudo isso de forma legal e em compliance com a Microsoft, pois as capacidades Embedded foram criadas justamente para isso.

Não é possível utilizar o Power Embedded sem uma capacidade dedicada.

A não ser que você contrate uma capacidade F64 ou superior, também não é possível utilizar uma capacidade dedicada para visualizar relatórios sem precisar de uma conta Pro para cada usuário se você não tiver um portal externo de visualização, como o Power Embedded.



### A partir de quantos usuários o Power Embedded é vantajoso para minha empresa?

Para estimar a partir de quantos usuários o Power Embedded é mais barato que a sua licença atual, dependemos de algumas informações do seu ambiente e de qual o tipo de licenciamento que você utiliza atualmente.

A nossa equipe de suporte faz um levantamento de informações no seu ambiente para avaliar previamente como a nossa solução poderá atingir o máximo de economia possível, sem perder performance, numa análise personalizada e individual para cada cliente.

Para licenças Power BI Pro, e em empresas em que o relatório não precise ficar disponível 24h por dia, a partir de 15 usuários você já consegue economizar 50% em relação ao custo das licenças Pro. Se você utiliza licença Premium por Usuário (PPU), a economia chega a 76%.

Caso seu ambiente tenha um ambiente com vários relatórios grandes (acima de 200 MB), talvez a capacidade Fabric F2 não atenda e seja necessário utilizar uma capacidade maior. Isso é avaliado e conversado durante a análise de capacidade.

Nesse cenário, a partir de 30 usuários você já estará economizando ao utilizar o Power Embedded, e quanto maior a quantidade de usuários, maior será a economia em relação à sua licença atual.

A tabela abaixo pode ajudar a visualizar os cenários quando o Power Embedded é mais vantajoso

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/10/Tabela-de-Precos-Power-Embedded-Outubro-de-2023-1024x538.png" alt=""><figcaption></figcaption></figure>



### A Microsoft permite o uso do Power Embedded? Isso é realmente legal?

Com certeza, a Microsoft permite o uso do Power Embedded e é uma solução 100% legal. A Power Tuning é uma empresa Microsoft Solutions Partner desde 2018, e uma das líderes em vendas de Azure no Brasil e, portanto, tem um forte relacionamento com a Microsoft e a distribuidora TD Synnex, e em hipótese alguma iria desenvolver um produto que utilizasse alguma licença ilegal ou mecanismo que quebre o contrato de uso com a Microsoft.

O Power Embedded também está disponível para ser acessado e contratado pelo [Azure Marketplace](https://azuremarketplace.microsoft.com/pt-br/marketplace/apps/powertuningperformanceemdados1702567987391.powerembedded?tab=overview), o que indica um forte relacionamento com a Microsoft para suportar o produto

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/05/Power-Embedded-no-Marketplace-da-Microsoft.png" alt=""><figcaption></figcaption></figure>

Falando sobre o licenciamento por capacidade, no [link abaixo](https://azure.microsoft.com/pt-br/pricing/details/power-bi-embedded/), a Microsoft deixa bem claro que os usuários que estão vendo o conteúdo publicado no Power BI Embedded não precisam de licenças do Power BI atribuídas a eles, portanto, não é necessário uma licença PRO para visualização dos relatórios através do Power Embedded

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/O-Power-Embedded-e-legal-Print-1-768x455.png" alt=""><figcaption></figcaption></figure>

Neste [link aqui](https://powerbi.microsoft.com/pt-br/blog/power-bi-embedded-with-microsoft-fabric/), a Microsoft mostra que o Microsoft Fabric também pode ser utilizado normalmente para inserir relatórios em aplicações terceiras, sem problema algum

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/O-Power-Embedded-e-legal-Print-3.png" alt=""><figcaption></figcaption></figure>

Neste[ link abaixo](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#quem-precisa-de-uma-licen-a-power-bi-pro-ou-ppu--premium-por-usu-rio--para-o-power-bi-embedded-e-por-qu--), a Microsoft deixa explícito que alteração e criação de relatórios por meio de um portal que utilize o licenciamento do Power BI Embedded, não requer uma licença PRO ou PPU para isso, e por tanto, a alteração e criação de relatórios pelo Power Embedded é totalmente legal e suportada.

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/O-Power-Embedded-e-legal-Print-2-1024x439.png" alt=""><figcaption></figcaption></figure>



### O que eu preciso ter para utilizar o Power Embedded?

Como o Power Embedded é um sistema no formato SaaS, você não precisará contratar ou gerenciar nenhum servidor, aplicação ou banco de dados, irá apenas utilizar o software como um serviço.

Para configurar o Power Embedded na sua empresa, precisamos que os seguintes pré-requisitos sejam atendidos antes de agendarmos a instalação:

* Conta de um usuário do Azure com permissão para criar a capacidade Fabric ou Embedded.
* Conta de um usuário do Azure com permissão para criar grupos e service principals no Azure AD.
* Conta de um usuário do Azure que possua a role “Fabric administrator” para acessar o [portal de administração do Power BI.](https://app.powerbi.com/admin-portal/tenantSettings)

Durante a reunião de instalação do sistema, que é feita junto com o cliente, precisamos que seja fornecido um usuário com as permissões listadas acima, ou que tenha alguma pessoa do time do cliente, com essas permissões, que possa compartilhar a tela e executar as ações que serão instruídas.



### É possível testar ou fazer uma PoC o Power Embedded?

Sempre encorajamos que as empresas testem exaustivamente a nossa solução para garantir que ela atenda bem e supere as expectativas dos nossos clientes.

E é por esse compromisso, e a certeza que nossa ferramenta é a melhor do mercado, nós damos 30 dias GRATUITOS para você importar seus relatórios, usuários e testar à vontade o sistema.

Nos primeiros 30 dias de uso, contados a partir da data da instalação, não iremos cobrar a mensalidade dos usuários e você só paga a instalação/configuração se você decidir permanecer utilizando a ferramenta após os 30 dias.

O único custo que não conseguimos incluir na gratuidade é o licenciamento da capacidade, que é feito diretamente com a Microsoft pelo portal do Azure, mas que a Microsoft libera 60 dias GRATUITAMENTE uma capacidade F64 para avaliação.



### Preciso contratar o portal da Power Tuning? Não posso usar o da Microsoft?

A Microsoft disponibiliza a contratação da capacidade do Power BI Embedded (ou Fabric) pelo Azure, que nada mais é que um recurso que permite gerar uma quantidade ILIMITADA de tokens para embeddar relatórios.

Caso você utilize o Portal padrão do Power BI, aí você continua no cenário atual, onde precisa de uma licença Pro (ou Premium por Usuário) para cada usuário que for publicar ou visualizar relatórios.

Para utilizar esse tipo de licenciamento, que é diferente de todos os outros tipos de licenciamentos do Power BI, você obrigatoriamente precisa utilizar uma aplicação Web para gerar esses tokens de forma automática e disponibilizar os relatórios para os seus usuários, pois a Microsoft NÃO disponibiliza um portal ou código-fonte de um portal pronto para ser utilizado.

Você pode criar o seu próprio portal, utilizando uma linguagem de programação, onde você vai implementar todo o código para gerenciar usuários e permissões, renderizar os relatórios, criar o layout do site, implementar a segurança, gerenciar o servidor de aplicação, banco de dados, corrigir problemas, implementar novas funcionalidades, etc.

Outra opção é contratar um portal já pronto, com tudo isso (e MUITO mais) já criado e pronto para uso, no modelo SaaS (Software As A Service), onde você não tem nenhuma preocupação ou nada para gerenciar, apenas utiliza o sistema, que é atualizado de forma constante e bem frequente.



### Quanto tempo demora para ter o Power Embedded na minha empresa?

A partir do momento em que a proposta comercial de utilização do Power Embedded for aprovada, em até 16h úteis nós faremos o contato para agendar a instalação do sistema, que geralmente demora de 20 a 60 minutos.

Lembre-se de conferir se todos os pré-requisitos para a instalação (tópico acima) foram atendidos antes de agendar a instalação.



### Os meus usuários poderão acessar os relatórios usando dispositivos móveis (celulares) ?

Sim, todo o sistema é responsivo e funciona perfeitamente em dispositivos móveis, como celulares e tablets.

Caso o relatório tenha sido criado no Power BI Desktop com suporte a layout mobile e o usuário esteja acessando o relatório através de um dispositivo móvel, o relatório será mostrado utilizando esse layout otimizado para dispositivos móveis, sem a necessidade de instalar aplicativos (nem o Power BI tradicional faz isso).



### Posso cancelar o Power Embedded? Existe alguma multa?

Pode cancelar a qualquer momento, basta nos comunicar que iremos gerar e enviar o faturamento do mês atual para pagamento.

Após a compensação do pagamento, iremos excluir todos os dados referentes aos usuários, relatórios importados, logs, etc.

# Perguntas mais frequentes

### Preço e Licenciamento

Para ter acesso ao Power Embedded e começar a economizar no licenciamento de Power BI, você precisará fazer apenas 3 investimentos, sendo 2 mensais e 1 que você irá pagar única vez, que são:

\
**Investimento único**

* R$ 1.500,00 para instalação e configuração inicial do ambiente.

**Investimentos mensais**

* A partir de R$ 427,54 pelo licenciamento da capacidade, variando conforme necessidade.
* R$ 5,00 por usuário que você criar no sistema.

Sim, é possível gerar tokens para Embeddar relatórios em uma capacidade Pro ou Premium por Usuário, mas de acordo com a [documentação oficial da Microsoft:](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/move-to-production)

“Os tokens incorporados com licença Pro ou Premium por usuário (PPU) destinam-se a testes de desenvolvimento, portanto, uma conta mestra ou Service Principal do Power BI só pode gerar um número limitado de tokens.

Adquira uma capacidade para incorporação em um ambiente de produção. Não há limite para quantos tokens incorporados você pode gerar ao comprar uma capacidade.

Nos testes de desenvolvimento, você pode usar tokens de avaliação incorporados gratuitos com uma licença Pro. **Para incorporar em um ambiente de produção, você deve adquirir uma capacidade.**“

[![](https://powerembedded.com.br/wp-content/uploads/2024/05/Power-Embedded-Mover-aplicacao-para-producao.png)](https://powerembedded.com.br/wp-content/uploads/2024/05/Power-Embedded-Mover-aplicacao-para-producao.png)

A página de [perguntas e respostas do Power BI Embedded](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#quantos-tokens-inseridos-posso-criar-) reafirma que contas Pro não podem ser utilizadas para soluções de Embedded em produção:

“Os tokens inseridos com a licença Pro ou PPU (Premium por usuário) destinam-se para teste de desenvolvimento, portanto, uma conta mestre ou [entidade de serviço](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embed-service-principal) do Power BI pode gerar apenas um número limitado de tokens. [Compre uma capacidade](https://learn.microsoft.com/pt-br/power-bi/developer/embedded/embedded-faq#technical) para inserir em um ambiente de produção. Não há limites para a quantidade de tokens inseridos que você pode gerar ao comprar uma capacidade. Em testes de desenvolvimento, você pode usar tokens de avaliação de inserção gratuitos com uma licença Pro. Para fazer uma inserção em um ambiente de produção, você deve comprar uma capacidade.”

[![](https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded-3.png)](https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded-3.png)

A página [Cenários de uso do Power BI: inserir para clientes – Power BI | Microsoft Learn](https://learn.microsoft.com/pt-br/power-bi/guidance/powerbi-implementation-planning-usage-scenario-embed-for-your-customers#licensing) também reforça que o uso de uma capacidade é obrigatório para utilizar tecnologias de Embedded:

[![](https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded.png)](https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded.png)

Além disso, o conteúdo que será mostrado na aplicação NÃO PODE estar em um workspace pessoal:

[![](https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded-4.png)](https://powerembedded.com.br/wp-content/uploads/2024/08/Power-Embedded-Guias-para-uso-da-licenca-de-Embedded-4.png)

**Caso você esteja utilizando uma plataforma que utilize uma conta Pro para gerar os tokens de inserção de relatórios, sem utilizar uma capacidade para isso, você provavelmente está violando os termos de uso do Power BI e sua empresa pode sofrer multas e sanções pela Microsoft.**

Para estimar a partir de quantos usuários o Power Embedded é mais barato que a sua licença atual, dependemos de algumas informações do seu ambiente e de qual o tipo de licenciamento que você utiliza atualmente.

A nossa equipe comercial irá fazer um levantamento de informações no seu ambiente para avaliar previamente como a nossa solução poderá atingir o máximo de economia possível, sem perder performance, numa análise personalizada e individual para cada cliente.

Para licenças Power BI Pro, e em empresas em que o relatório não precise ficar disponível 24h por dia, a partir de 20 usuários você já consegue economizar 50% em relação ao custo das licenças Pro. Se você utiliza licença Premium por Usuário (PPU), a economia chega a 76%.

Caso seu ambiente tenha um ambiente com vários relatórios grandes (acima de 200 MB), talvez a capacidade Fabric não atenda e seja necessário utilizar a capacidade Embedded.

Nesse cenário, a partir de 30 usuários você já estará economizando ao utilizar o Power Embedded, e quanto maior a quantidade de usuários, maior será a economia em relação à sua licença atual.

A tabela abaixo pode ajudar a visualizar os cenários quando o Power Embedded é mais vantajoso:

[![](https://powerembedded.com.br/wp-content/uploads/2023/10/Tabela-de-Precos-Power-Embedded-Outubro-de-2023.png)](https://powerembedded.com.br/wp-content/uploads/2023/10/Tabela-de-Precos-Power-Embedded-Outubro-de-2023.png)

Mesmo utilizando uma licença por capacidade do Power BI, seja o Power BI Embedded, o Fabric, ou até mesmo o Power BI Premium por capacidade (aquela que custa R$ 32.000,00 por mês), todos os usuários que publicam relatórios precisam de uma licença Pro ou PPU (Premium por usuário).

Para não precisar ter uma licença Pro para cada usuário que publique relatórios, uma alternativa é utilizar o Azure DevOps para a publicação automática com CI/CD, por exemplo, que a Power Tuning oferece suporte e pode ajudar a implantação desse processo na sua empresa através de consultoria.

Utilizando a licença gratuita do Power BI, você poderá utilizar o Power BI Desktop livremente, sem nenhuma limitação. E ainda poderá publicar os seus relatórios no seu workspace pessoal e testar à vontade.

A partir do momento em que você precisa compartilhar os relatórios com outras pessoas, a licença Pro se faz necessária, pois é através dela (ou de licenças mais caras) que você poderá compartilhar os relatórios.

As únicas formas de compartilhar relatórios sem precisar comprar uma licença de Power BI, é enviando o arquivo PBIX para a pessoa ou utilizando o recurso “Publicar na Web”, que permite compartilhar o relatório com qualquer pessoa que tenha acesso ao link do relatório, mas não possui nenhum tipo de segurança.

### Dúvidas sobre capacidades (Fabric ou Power BI Embedded)

As capacidades são recursos do Power BI que licenciam a solução do Power Embedded junto à Microsoft e permitem utilizar as API’s, de forma legal e ilimitada, para inserir os relatórios publicados no sistema e não precisar de licença para visualizar os relatórios.

Sem uma capacidade contratada, utilizando uma conta Pro ou PPU, você tem uma quantidade limitada de tokens para inserção de relatórios. Após um tempo, esse limite é atingido e o Power BI não permite mais inserir relatórios e o Power Embedded iria parar de funcionar. **Por este motivo, é obrigatório ter uma capacidade** **contratada para utilizar o Power Embedded.**

Tipos de capacidades (todas são suportadas pelo Power Embedded):

* Fabric: Mais nova, flexível, mais recursos e pode começar mais barato.
* Power BI Embedded: Mais estável, confiável e pode ser mais barato no modelo pago pelo uso, dependendo da região e tamanho.
* Premium por Capacidade: Capacidade que foi descontinuada e o custo inicial é 32 mil reais por mês.

Observações:

* As capacidades são contratadas direto com a Microsoft (ou parceiro) pelo Azure.
* Ter uma capacidade é um requisito para o Power Embedded funcionar.
* Microsoft libera um período de avaliação gratuito de 60 dias para o Fabric.

Enquanto a capacidade estiver pausada, ninguém acessa os relatórios, nem mesmo acessando pelo powerbi.com com uma conta Pro ou PPU. Os conjuntos de dados também não serão atualizados.

**Um enorme diferencial do Power Embedded**\
O sistema Power Embedded já possui um mecanismo que permite definir os horários em que o recurso ficará sempre ativo e o próprio sistema pausa e inicia a capacidade automaticamente.

Quando o recurso estiver pausado e algum usuário tentar acessar um relatório, o sistema irá iniciar automaticamente a capacidade, para permitir que o usuário acesse o relatório mesmo fora dos horários definidos e irá monitorar se os relatórios ainda estão sendo acessados.

Quando o Power Embedded identificar que não tem mais usuários acessandos os relatórios há mais que X minutos (tempo determinado pelo administrador), o sistema irá pausar novamente, de forma automática, a capacidade para voltar a economizar com o recurso pausado.

A cobrança do Power BI Embedded e do Fabric são calculadas por hora em que a capacidade ficou ligada e essas horas são somadas ao final do faturamento para gerar o valor que você irá pagar no mês.

Ambas permitem que você pause a capacidade e assim, evita a cobrança nos horários em que o recurso ficou pausado, aumentando ainda mais a economia com o Power Embedded.

Esses siglas de 24×7, significa que o sistema ficará disponível 24h por dia, durante 7 dias na semana, ou seja, ficará sempre ligado, sem pausado em nenhum momento.

Na maioria dos clientes, o cenário 14×6 atende as necessidades dos usuários, onde os relatórios ficariam disponíveis 14h por dia, durante 6 dias na semana (seg-sáb). Essa opção representa uma economia de 53% em relação ao 24×7.

Em alguns cenários, o cenário 12×5 atende as necessidades dos usuários, onde os relatórios ficariam disponíveis 12h por dia, durante 5 dias na semana (seg-sex). Essa opção representa uma economia de 67% em relação ao 24×7.

Essas siglas 24×7, 14×6 e 12×5 são apenas alguns exemplos de opções para pausar e iniciar automaticamente as capacidades, e esses horários e tempos serão definidos conforme o cenário de cada cliente.

Vale lembrar que quando a capacidade do Fabric ou Embedded está pausada, para economia de custos, os relatórios não ficam acessíveis, mesmo acessando pelo portal do powerbi.com, utilizando uma conta Pro (a não ser que você altere o tipo do Workspace de volta para Pro).

Se a sua empresa já possui o Power BI Premium (por capacidade), seus usuários podem acessar os relatórios que estão publicados no próprio portal do Power BI (powerbi.com) sem precisar de licença para visualizar.

Se mesmo assim, você quiser embeddar os relatórios num Sharepoint, aplicação ou website, desde o tier P1 você já pode utilizar as capacidades de Embedded da licença Premium, pois a capacidade Premium já inclui o Power BI Embedded.

Como trabalhamos com os preços oficiais da Microsoft, não é possível conseguir um preço mais baixo, uma vez que não temos **nenhuma** margem de lucro em cima da capacidade, inclusive, fazemos a contratação da capacidade direto pelo portal do Azure, com o cliente acompanhando todo o processo.

Existem várias formas de tentar burlar os processos corretos e oficias da Microsoft para tentar baratear o valor da licença, como usar contas Pro/PPU ao invés de contratar uma capacidade dedicada e usar algumas técnicas para lidar com os tokens expirados, mas como já foi mencionado em um tópico acima, isso é ilegal e fere o contrato da Microsoft e, por este motivo, não concordamos com esse tipo de prática, mesmo que isso signifique perder alguns clientes que optem por esse caminho.

Outra forma de conseguir reduzir o valor do Embedded, é alocando vários clientes numa mesma capacidade, o que também não concordamos por não entregar uma performance controlada, estável e otimizada conforme nossos padrões de qualidade.

Sim, claro! Sem problema algum.

Antes de agendarmos a instalação do sistema, vamos ajudá-los a criar uma conta no Azure, necessária para a contratação da capacidade do Embedded ou Fabric.

A [Power Tuning](https://powertuning.com.br/) é parceira Microsoft e, caso você não tenha um parceiro ainda, ou deseja trocar o seu parceiro para a Power, vamos ajudá-lo em todo esse processo, **de forma gratuita**.

Ter um parceiro ao invés de contratar direto com a Microsoft é muito importante e traz uma série de vantagens que são muito benéficas para a sua empresa.

**Contratação de serviços do Azure direto com a Microsoft (SEM um parceiro)**

* Irá pagar via cartão de crédito, o que já gera uma cobrança **EXTRA** de 6,38% de IOF sobre o valor total da sua fatura do Azure.
* Você paga em dólar ou pode pagar em real (com cotação bem acima do dólar comercial)
* Você não receberá Nota Fiscal pelo valor pago de Azure.
* Você terá que recolher todos os impostos **manualmente**, como ICMS, PIS e COFINS.
* Suporte técnico N1 demora dias e o Premier custa mais de 1.000 USD por mês.

**Contratação de serviços do Azure com a Power Tuning sendo sua parceira Microsoft**

* Você vai pagar a **fatura via boleto**, com todos os impostos já recolhidos e sem pagar IOF.
* Você irá receber **Nota Fiscal** do valor pago de Azure.
* **Suporte técnico 24×7** com o nosso time de Cloud e caso necessário, suporte Premier com o time de engenheiros da Microsoft.
* **Licença mais baratas:** Precisa de licença de Power BI, Windows, SQL Server ou Office? Nós tentaremos chegar ao menor valor possível para qualquer licença Microsoft que você precise para sua empresa. A licença de Power BI Pro no site da Microsoft, está R$ 65,00 por usuário, enquanto a gente consegue a R$ 55,00 (cotação pode variar).
* **Ferramenta de análise de custos:** Nosso sistema interno analisa o seu custo médio de hora em hora, e qualquer desvio no custo médio diário e projetado, irá gerar um alerta para entrarmos em contato para verificar se o aumento é algo planejado ou não.
* **Ferramenta de análise de redução de custos:** Nosso sistema interno fica constantemente analisando os recursos criados para verificar se há possibilidade de redução de custos, como máquinas virtuais sub-utilizadas, máquinas virtuais que não possuem instância reservada (economia de até 70%), recursos não utilizados, discos não associados à VM’s e MUITO mais.
* **Ferramenta de detecção de invasão**: Qualquer recurso criado fora dos padrões existentes, como tamanhos e regiões, irá gerar um alerta e entraremos em contato com a sua empresa.
* **Todos esses serviços e ferramentas, nós oferecemos DE GRAÇA**.

Quer ter a Power Tuning como sua parceira Microsoft?

[Clique aqui](https://powertuning.com.br/parceria-azure) para cadastrar a Power Tuning como sua parceira de nuvem / Microsoft.

### Dúvidas Técnicas

[![](https://powerembedded.com.br/wp-content/uploads/2024/04/Power-Embedded-Internals-Exibicao-do-Relatorio.png)](https://powerembedded.com.br/wp-content/uploads/2024/04/Power-Embedded-Internals-Exibicao-do-Relatorio.png)

O funcionamento interno do Power Embedded para exibição dos relatórios está descrito abaixo:

1\) Power Embedded verifica se o usuário logado pode acessar o relatório e envia os dados para aplicar o RLS (se houver)

2\) Power Embedded se autentica na API do Azure e recupera um token para autenticação

3\) Power Embedded envia os metadados necessários para as API’s do Power BI (IDs do Workspace, Relatório e Conjunto de dados)

4\) API do Power BI carrega os dados que estão armazenados nos workspaces e o relatório

5\) API do Power BI monta o elemento iframe apontando para o relatório já pronto e retorna para o sistema

6\) Power Embedded exibe o iframe retornado para o usuário. NENHUM dado do relatório é lido, acessado, armazenado ou trafega pelos servidores do sistema

[![](https://powerembedded.com.br/wp-content/uploads/2024/04/Power-Embedded-Internals-Importacao-de-Relatorios.png)](https://powerembedded.com.br/wp-content/uploads/2024/04/Power-Embedded-Internals-Importacao-de-Relatorios.png)

O funcionamento interno para importação dos relatórios do Power BI para o Power Embedded está descrito abaixo:

1\) Power Embedded interage com as API’s do Power BI

2\) API retorna os metadados necessários para exibição (IDs do Workspace, Relatório e Conjunto de dados)

3\) Power Embedded armazena os metadados retornados

4\) Administrador gerencia as permissões, RLS, estrutura de pastas e demais atributos do relatório

5\) NENHUM dado pessoal é armazenado pelo Power Embedded, apenas o email e nome dos usuários.

6\) NENHUM dado de relatório é armazenado ou trafega pela rede ou pelos servidores do Power Embedded

A segurança interna do Power Embedded é extremamente robusta e o sistema utiliza uma arquitetura toda baseada em recursos SaaS auto-gerenciados no Azure, onde a gestão é feita pela Microsoft, backups automáticos e alta disponibilidade da aplicação e do banco de dados por zonas de disponibilidade com failover automático e com garantia de disponibilidade de 99,99%.

O sistema é submetido à diversos e complexos pentests de forma periódica, tanto automáticos feitos por ferramentas de pentest quanto validações e testes manuais, feitos por especialistas de segurança de empresas contratadas.

Todo o ambiente de nuvem é protegido pelo Microsoft Defender for Cloud, que faz a proteção, análise e recomendações de forma proativa e contínua.

O acesso aos recursos do Azure é bloqueado para internet e só acessível através de VPN.

A comunicação entre o sistema e o navegador é criptografa utilizando certificados SSL (HTTPS).

A chave de acesso ao Power BI é armazenada no banco de dados criptografada utilizando o algoritmo mais seguro do mercado (RSA-OEAP) e vários mecanismos de proteção para garantir que mesmo em um eventual acesso indevido ao banco de dados, essa chave não possa ser decodificada, uma vez que o acesso à chave de segurança para descriptografar (que é individual por cliente) fica em um Azure KeyVault onde somente a aplicação possui permissão e conectividade para acessar.

A chave da API pública é criptografada utilizando um algoritmo de HASH que não permite recuperação do valor gerado, assim como o secret de um KeyVault.

O processo de embeddar os relatórios no sistema não requer o carregamento ou leitura de nenhum dado dos nossos clientes.

Todos os dados ficam armazenados nos servidores do Power BI mesmo, em um conjunto de dados publicado em um workspace e o sistema apenas utiliza a API do Power BI para a renderização do relatório (também já publicado no workspace) dentro do sistema.

Sendo assim, não lemos ou coletamos nenhuma informação, apenas realizamos uma chamada HTTP na API do Power BI, que lê os dados e exibe na tela.

Os únicos dados da empresa que são armazenados, são os nomes e e-mails dos usuários cadastrados no sistema, para gerenciamento dos acessos.

A nível de segurança, toda a comunicação do Power Embedded é criptografada ponta-a-ponta, utilizando segurança SSL e HTTPS, além de Azure Firewall e diversos mecanismos de segurança do Azure.

Embora as 3 opções permitem embeddar relatórios em websites, sharepoint, e-mail, teams, etc.., elas são bem diferentes.

**Embedded**

É uma licença por capacidade, que permite visualizar relatórios de forma segurança (com permissões, RLS, OLS, auditorias de acessos, bloqueios por IP, etc) através de uma aplicação, sem a necessidade de quem está visualizando ter uma licença do Power BI, e controlar todos os visuais, cores, temas, páginas e componentes dos relatórios utilizando linguagem de programação.

**Inserir relatório**

Essa é uma forma de compartilhar relatórios em websites, aplicativos, sharepoint, teams, etc.. de forma segura, mantendo todos os controles de segurança do Power BI, como permissões, RLS, OLS e auditorias de acesso.

Diferente do Embedded, nesse modo de compartilhamento, **todos os usuários que vão acessar o relatório, precisam de ter uma licença** Pro ou PPU (ou capacidade Premium).

Além disso, você **NÃO** consegue controlar os elementos do relatório via linguagem de programação para criar/editar visuais dinamicamente, trocar temas, criar/excluir páginas, etc..

**Publicar na Web**

É uma forma de compartilhar relatórios de graça, sem que a pessoa que está visualizando precise ter uma conta ou licença do Power BI. Ela funciona muito bem quando você precisa compartilhar relatórios que contém **dados públicos**, isto é, não há preocupação com vazamento de dados.

Diferente do Embedded, no “Publicar na Web” não existe nenhuma segurança: Qualquer pessoa que tenha acesso ao link do relatório, irá visualizá-lo, sem qualquer controle a nível de usuário, como RLS ou OLS, não há necessidade de quem está visualizando ser cadastrado em nenhuma aplicação e não há auditoria para saber quem está visualizando o relatório. Qualquer pessoa poderá estar visualizando os dados da sua empresa e você não saberá quem.

Além disso, como já amplamente divulgado na internet, todos os relatórios publicados desta forma, podem ser acessados através de consultas simples ao Google, mesmo que o link nunca tenha sido publicado em nenhum local.

Mesmo que você tente bloquear o acesso utilizando uma senha para abrir o portal, esse tipo de mecanismo é facilmente quebrado em poucos segundos, utilizando a opção de Developer Tools do navegador e a pessoa terá acesso irrestrito aos dados publicados no relatório.

O processo de importação e publicação dos relatórios no Power Embedded é praticamente o mesmo que já existe no Power BI serviço tradicional:

* Usuário abre o Power BI Desktop e cria o relatório.
* Usuário publica o relatório no workspace desejado.
*   Administrador do Power Embedded importa o relatório do workspace do Power BI para o sistema.

    [![](https://powerembedded.com.br/wp-content/uploads/2023/09/Importar-Relatorios.png)](https://powerembedded.com.br/wp-content/uploads/2023/09/Importar-Relatorios.png)
* Administrador do Power Embedded atribui as permissões via grupo ou usuário individualmente.
* Administrador do Power Embedded define as regras de RLS do conjunto de dados (caso tenha).
* Usuário acessa o relatório pelo Portal de visualização do Power Embedded.

Sim, com certeza!

O Power Embedded é um sistema muito dinâmico, e o nosso time está sempre atento aos pedidos e necessidades dos nossos clientes e também aos novos recursos disponibilizados pela Microsoft.

Temos um tempo de desenvolvimento e implanetação bem rápido, o que nos permite realizar de 2 a 5 atualizações de melhorias e novas funcionalidades **por semana**.

Sempre que uma funcionalidade ou melhoria for implementada, aplicamos e disponibilizados **gratuitamente** para todos os nossos clientes, de forma automática.

Sim, fazemos sim.

Neste caso, onde a personalização não será aplicada para os demais clientes e ficará restrita apenas para a sua empresa, iremos agendar uma reunião com a sua equipe para entender melhor a sua necessidade e enviaremos uma proposta comercial para implantar essa personalização no sistema.

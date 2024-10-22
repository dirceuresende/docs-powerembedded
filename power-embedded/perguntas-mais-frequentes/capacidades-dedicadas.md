# Capacidades dedicadas

### Fabric? Power BI Embedded? O que são essas capacidades?

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



### Enquanto a capacidade estiver pausada, ninguém acessa os relatórios?

Enquanto a capacidade estiver pausada, ninguém acessa os relatórios, nem mesmo acessando pelo powerbi.com com uma conta Pro ou PPU. Os conjuntos de dados também não serão atualizados.

**Um enorme diferencial do Power Embedded**\
O sistema Power Embedded já possui um mecanismo que permite definir os horários em que o recurso ficará sempre ativo e o próprio sistema pausa e inicia a capacidade automaticamente.

Quando o recurso estiver pausado e algum usuário tentar acessar um relatório, o sistema irá iniciar automaticamente a capacidade, para permitir que o usuário acesse o relatório mesmo fora dos horários definidos e irá monitorar se os relatórios ainda estão sendo acessados.

Quando o Power Embedded identificar que não tem mais usuários acessandos os relatórios há mais que X minutos (tempo determinado pelo administrador), o sistema irá pausar novamente, de forma automática, a capacidade para voltar a economizar com o recurso pausado.



### O que seria isso de 24x7, 14x6 e 12x5?

A cobrança do Power BI Embedded e do Fabric são calculadas por hora em que a capacidade ficou ligada e essas horas são somadas ao final do faturamento para gerar o valor que você irá pagar no mês.

Ambas permitem que você pause a capacidade e assim, evita a cobrança nos horários em que o recurso ficou pausado, aumentando ainda mais a economia com o Power Embedded.

Esses siglas de 24×7, significa que o sistema ficará disponível 24h por dia, durante 7 dias na semana, ou seja, ficará sempre ligado, sem pausado em nenhum momento.

Na maioria dos clientes, o cenário 14×6 atende as necessidades dos usuários, onde os relatórios ficariam disponíveis 14h por dia, durante 6 dias na semana (seg-sáb). Essa opção representa uma economia de 53% em relação ao 24×7.

Em alguns cenários, o cenário 12×5 atende as necessidades dos usuários, onde os relatórios ficariam disponíveis 12h por dia, durante 5 dias na semana (seg-sex). Essa opção representa uma economia de 67% em relação ao 24×7.

Essas siglas 24×7, 14×6 e 12×5 são apenas alguns exemplos de opções para pausar e iniciar automaticamente as capacidades, e esses horários e tempos serão definidos conforme o cenário de cada cliente.

Vale lembrar que quando a capacidade do Fabric ou Embedded está pausada, para economia de custos, os relatórios não ficam acessíveis, mesmo acessando pelo portal do powerbi.com, utilizando uma conta Pro (a não ser que você altere o tipo do Workspace de volta para Pro).



### Minha empresa já tem o Power BI Premium. Preciso contratar o Embedded?

Se a sua empresa já possui o Power BI Premium (por capacidade), seus usuários podem acessar os relatórios que estão publicados no próprio portal do Power BI (powerbi.com) sem precisar de licença para visualizar.

Se mesmo assim, você quiser embeddar os relatórios num Sharepoint, aplicação ou website, desde o tier P1 você já pode utilizar as capacidades de Embedded da licença Premium, pois a capacidade Premium já inclui o Power BI Embedded.

{% hint style="danger" %}
As capacidades Premium (tier P) foram descontinuadas e substituídas pelo Fabric
{% endhint %}



### Uma empresa concorrente conseguiu um valor bem mais baixo do Embedded

Como trabalhamos com os preços oficiais da Microsoft, não é possível conseguir um preço mais baixo, uma vez que não temos **nenhuma** margem de lucro em cima da capacidade, inclusive, fazemos a contratação da capacidade direto pelo portal do Azure, com o cliente acompanhando todo o processo.

Existem várias formas de tentar burlar os processos corretos e oficias da Microsoft para tentar baratear o valor da licença, como usar contas Pro/PPU ao invés de contratar uma capacidade dedicada e usar algumas técnicas para lidar com os tokens expirados, mas como já foi mencionado em um tópico acima, isso é ilegal e fere o contrato da Microsoft e, por este motivo, não concordamos com esse tipo de prática, mesmo que isso signifique perder alguns clientes que optem por esse caminho.

Outra forma de conseguir reduzir o valor do Embedded, é alocando vários clientes numa mesma capacidade, o que também não concordamos por não entregar uma performance controlada, estável e otimizada conforme nossos padrões de qualidade.



### Não tenho conta do Azure para contratar a capacidade

Sem problema algum, podemos te ajudar na contração da capacidade.

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



{% hint style="success" %}
**Quer ter a Power Tuning como sua parceira Microsoft?**

[Clique aqui](https://powertuning.com.br/parceria-azure) para cadastrar a Power Tuning como sua parceira de nuvem / Microsoft.
{% endhint %}

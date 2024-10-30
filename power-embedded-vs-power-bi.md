---
icon: square-poll-vertical
---

# Power Embedded vs Power BI

### 1. Introdução

Uma das dúvidas mais comuns que recebemos é sobre a diferença entre o Power BI e o Power Embedded. Embora ambos se complementem, existem diferenças importantes, e por isso preparamos esta documentação para auxiliar nesse entendimento.

É fundamental entender que o Power Embedded não substitui o Power BI. Pelo contrário, ele amplia as capacidades do Power BI, permitindo uma visão ainda mais detalhada dos seus dados e melhorando a organização do ambiente de BI, além de oferecer funcionalidades exclusivas.

Se você já quis entregar um portal personalizado para seus clientes, compartilhar relatórios com usuários externos, obter insights detalhados sobre quais relatórios estão sendo mais acessados, ou até contar com um assistente de IA que ajude a analisar seus dados de maneira eficiente, e, ao mesmo tempo, reduzir custos com licenças do Power BI, o Power Embedded pode ser a solução ideal para esses e outros desafios.

O Power Embedded é uma solução SaaS que utiliza as capacidades oficiais da Microsoft para incorporar (embed) os relatórios publicados no serviço Power BI diretamente em sua aplicação, o que pode reduzir os custos mensais de licenciamento do Power BI em até 90%.

Além de reduzir os custos, o Power Embedded ainda oferece uma série de funcionalidades adicionais, que descreveremos ao longo desta documentação.



### 2. Tabela comparativa entre Power BI e o Power Embedded

Embora algumas funções sejam similares, o Power Embedded traz algumas melhorias significativas.

Segue abaixo uma tabela comparando as principais semelhanças e diferenças entre as duas soluções.&#x20;

<table><thead><tr><th>Funcionalidade</th><th width="207" data-type="checkbox">Power BI</th><th data-type="checkbox">Power Embedded</th></tr></thead><tbody><tr><td><a href="inicio/quanto-custa-o-power-embedded.md">Custo por usuário a R$ 5,00</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/configuracoes/tela-de-login/metodos-de-autenticacao.md">Autenticação Integrada com Entra ID (Microsoft)</a></td><td>true</td><td>true</td></tr><tr><td><a href="portal-de-administracao/grupos/sincronizar-com-entra-id.md">Sincronização automática de usuários com Entra ID</a></td><td>true</td><td>true</td></tr><tr><td><a href="portal-de-administracao/configuracoes/tela-de-login/metodos-de-autenticacao.md">Autenticação Integrada com Google</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/configuracoes/tela-de-login/metodos-de-autenticacao.md">Autenticação utilizando apenas email e senha</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/power-pilot-ia/">IA Generativa com baixo custo</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/power-pilot-ia/ia-no-whatsapp.md">IA Generativa no WhatsApp</a></td><td>false</td><td>true</td></tr><tr><td><a href="documentacao-tecnica/api/mostrar-relatorio-no-seu-sistema.md">Permite incorporar os relatórios no meu sistema</a></td><td>true</td><td>true</td></tr><tr><td><a href="portal-de-administracao/aplicativos.md">Aplicativo (Agrupar vários relatórios)</a></td><td>true</td><td>true</td></tr><tr><td><a href="portal-de-administracao/aplicativos.md#relatorios">Aplicativo - Segurança ao nível de página</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/aplicativos.md#modo-tv">Aplicativo - Modo TV</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/aplicativos.md#criar-editar-aplicativo">Aplicativo - Relatórios de diferentes workspaces</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/aplicativos.md#criar-editar-aplicativo">Aplicativo - Incluir Dashboards, Links Externos e Relatórios Paginados</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-relatorios/assinatura-de-relatorio.md">Assinatura de relatório por email incluindo anexo</a></td><td>true</td><td>true</td></tr><tr><td><a href="portal-de-administracao/relatorios/assinatura-de-relatorios.md#suporte-a-row-level-security-rls">Assinatura de relatório por email com RLS</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/artefatos/capacidades/otimizacao-de-custos.md">Controle de capacidades - Liga/desliga por agendamento</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/artefatos/capacidades/otimizacao-de-custos.md">Controle de capacidades - Liga/desliga por demanda</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/artefatos/capacidades/redimensionamento-automatico.md">Controle de capacidades - Resize da capacidade por agendamento</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/relatorios/modelos-dinamicos.md">Modelos dinâmicos</a></td><td>false</td><td>true</td></tr><tr><td><a href="principais-funcionalidades/modo-escuro.md">Modo escuro na navegação</a></td><td>false</td><td>true</td></tr><tr><td><a href="principais-funcionalidades/agendamento-de-atualizacao-dos-dados.md">Atualização dos dados - Sem limite de atualizações</a></td><td>false</td><td>true</td></tr><tr><td><a href="principais-funcionalidades/agendamento-de-atualizacao-dos-dados.md">Atualização dos dados - Intervalos a cada 5 minutos</a></td><td>false</td><td>true</td></tr><tr><td><a href="principais-funcionalidades/agendamento-de-atualizacao-dos-dados.md">Atualização dos dados - Mesmo após 5 falhas, continua funcionando</a></td><td>false</td><td>true</td></tr><tr><td><a href="principais-funcionalidades/agendamento-de-atualizacao-dos-dados.md">Atualização dos dados - Não precisa tomar o controle para gerenciar, ou seja, várias pessoas podem administrar</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/configuracoes/parametros/personalizacoes-gerais.md#tipo-de-visualizacao-padrao-dos-relatorios">Listagem de relatórios - 3 tipos de visualização</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/configuracoes/parametros/personalizacoes-gerais.md#tipo-de-visualizacao-padrao-dos-relatorios">Listagem de relatórios - Visão unificada, independente de workspace ou pasta</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/auditorias/firewall.md">Firewall</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/auditorias/relatorios.md">Auditoria de relatórios unificada</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/auditorias/acessos.md">Auditoria de login/logout</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/auditorias/permissoes.md">Auditoria de permissões</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/auditorias/catalogo-de-relatorios.md">Auditoria de liberação de acessos</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-relatorios/catalogo-de-relatorios.md">Catálogo de relatórios</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/configuracoes/portal-de-visualizacao/">Personalização da tela de login e portal de visualização</a></td><td>false</td><td>true</td></tr><tr><td><a href="principais-funcionalidades/compartilhamento-com-usuarios-externos.md">Compartilhamento com usuários externos sem passar pelo AD</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/avisos.md">Avisos e notificações para os usuários</a></td><td>false</td><td>true</td></tr><tr><td><a href="portal-de-administracao/configuracoes/organizacao/google-analytics.md">Integração com Google Analytics</a></td><td>false</td><td>true</td></tr><tr><td>Todos os dados são facilmente exportáveis</td><td>false</td><td>true</td></tr></tbody></table>



### 3. Novas Funcionalidades do Power Embedded

**IA Generativa de baixo custo**

* **Power BI**: O Power BI conta com o Copilot, uma IA generativa robusta que auxilia na análise dos dados. No entanto, essa funcionalidade está disponível apenas no SKU F64 do Microsoft Fabric, o que pode não ser financeiramente viável para algumas organizações devido ao seu custo elevado.
* **Power Embedded**: No Power Embedded, há uma IA generativa chamada Power Pilot, que também permite responder perguntas de negócios de forma rápida e eficiente. O grande diferencial é que o Power Pilot oferece essa funcionalidade a um custo significativamente mais acessível, tornando a solução mais atraente do ponto de vista financeiro.

#### **Controle de Acessos por Firewall**

* **Power BI**: No Power Bi, você não consegue de forma nativa restringir os acessos por IP.
* **Power Embedded**: O Power Embedded oferece essa funcionalidade de forma nativa, permitindo que você restrinja o acesso dos usuários com base em endereços IP.

#### **Auditorias**

* **Power BI**: As auditorias no Power BI são limitadas a métricas de uso, que muitas vezes não fornecem as informações detalhadas que você realmente precisa, estão geralmente desatualizadas e a visão é por workspace, o que torna inviável ao ter vários.
* **Power Embedded**: No Power Embedded, você tem acesso a auditorias detalhadas que fornecem métricas como acessos, permissões e relatórios mais utilizados, entre outras auditorias, em uma visão unificada de todo o ambiente, API para consultar esses dados ou exportar para CSV/Excel.

#### Modelos dinâmicos

* **Power BI:** Disponível apenas através da API.
* **Power Embedded:** Funcionalidade exclusiva do Power Embedded, desenvolvida para cenários nos quais um único relatório é acessado por diferentes clientes, cada um utilizando um modelo semântico diferente, e por isso, visualizam dados diferentes. Isso é muito útil para separar os dados de acordo com cada cliente sem depender de RLS e mantendo o tamanho de cada modelo pequeno. Isso ajuda bastante na performance dos relatórios.

**Modo escuro (Dark Mode) - Funcionalidade**

* **Power BI**: Disponível apenas no Power BI Desktop recentemente.
* **Power Embedded**: O modo escuro está disponível de forma nativa na versão web do Power BI Embedded desde o lançamento da ferramenta.

#### **Identidade visual personalizada (White-label)**

* **Power BI**: O Power BI oferece gráficos incríveis, mas não é possível personalizar um ambiente com a identidade visual específica de cada cliente.
* **Power Embedded**: No Power Embedded, você pode criar um ambiente personalizado com identidade visual específica para seus clientes ou departamentos, proporcionando uma experiência totalmente customizada.

#### **Catálogo de relatórios**

* **Power BI**: Não há uma funcionalidade nativa para exibir relatórios que os usuários não têm acesso, mas que podem ser úteis para eles.
* **Power Embedded**: Com o catálogo de relatórios no Power Embedded, você pode mostrar relatórios para os usuários, mesmo que eles ainda não tenham acesso direto, permitindo que eles solicitem permissão se necessário.

#### Avisos e notificações

* **Power BI:** Não há uma funcionalidade nativa para mostrar avisos, notificações e alertas para os usuários que estão navegando no portal.
* **Power Embedded:** Existe uma funcionalidade de [**Avisos**](portal-de-administracao/avisos.md), onde é possível agendar avisos e notificações, utilizando texto rico e imagens, para que os usuários que estão navegando no portal e visualizando relatórios possam ficar cientes desses recados.

#### Todos os dados são facilmente exportáveis

* **Power BI:** Não há opções para exportação de regras de RLS, usuários, auditorias, etc.
* **Power Embedded:** Todas as auditorias, regras de RLS, usuários e auditorias permitem a exportação e importação dos dados utilizando arquivos. A auditoria de acessos a relatórios tem até API para leitura dos dados em tempo real.



### 4. Melhorias do Power Embedded

#### **Aplicativo**

* **Power BI**: No Power BI, o aplicativo é uma maneira de compartilhar relatórios, onde você pode agrupar vários dashboards, relatórios em um único local e compartilhar com diferentes audiências. Somente relatórios podem ser incluídos e precisam estar no mesmo workspace.
* **Power Embedded**: No Power Embedded, essa funcionalidade está disponível com algumas melhorias. É possível criar quantos aplicativos forem necessários, adicionar relatórios de diferentes workspaces e usar o modo TV, que permite a exibição dos relatórios em uma tela com funcionalidade de slideshow de forma nativa. Além disso, a segurança por nível de página (Page Level Security) permite que você defina quais páginas do relatório deseja disponibilizar para cada usuário.

#### **Compartilhamento com usuários externos**

* **Power BI**: No Power BI, compartilhar relatórios com usuários externos pode ser complicado, exigindo que os usuários tenham uma conta corporativa ou uma licença específica (Pro ou PPU).
* **Power  Embedded**: No Power Embedded, que utiliza licenças Power BI Embedded ou Fabric, você pode compartilhar seus relatórios de maneira mais flexível com usuários externos sem as mesmas restrições de licença.

#### **Atualização de conjunto de dados**

* **Power BI**: Você pode agendar atualizações de dados no Power BI, mas está limitado a 8 atualizações diárias na licença Pro ou 48 na PPU.
* **Power Embedded**: No Power Embedded, além de agendar atualizações, você tem funcionalidades extras, como a possibilidade de não precisar tomar posse do conjunto de dados e de realizar atualizações sem o limite de 30 minutos entre cada uma e quando ocorrem mais de 5 falhas, a atualização do Power Embedded continua funcionando, enquanto a do Power BI para de funcionar. Via API, as atualizações são ilimitadas.



### 5. Limitações do Power Embedded

<mark style="color:red;">**Embora o Power Embedded ofereçam soluções poderosas, existem algumas limitações que, devido a não ter suporte na API oficial do Power BI, você perde acesso:**</mark>

* **Analisar no Excel**: Caso a quantidade de usuários que precisam dessa funcionalidade seja baixa, pode liberar algumas contas Pro para que eles continuem utilizando essa funcionalidade.
* **Direct Lake**: Não suportado ainda pela API.
* **Cálculos visuais**: Não suportado ainda pela API.



### 6. Principais Funcionalidades do Power Embedded

<table data-view="cards"><thead><tr><th></th><th data-hidden></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Aplicativo</strong></td><td></td><td><a href=".gitbook/assets/coleta-de-dados.png">coleta-de-dados.png</a></td><td><a href="principais-funcionalidades/aplicativo.md">aplicativo.md</a></td></tr><tr><td><strong>Dark Mode</strong></td><td></td><td><a href=".gitbook/assets/modo-escuro (1).png">modo-escuro (1).png</a></td><td><a href="principais-funcionalidades/modo-escuro.md">modo-escuro.md</a></td></tr><tr><td>A<strong>tualização agendada - Conjunto de dados</strong></td><td></td><td><a href=".gitbook/assets/big-data (2).png">big-data (2).png</a></td><td><a href="principais-funcionalidades/agendamento-de-atualizacao-dos-dados.md">agendamento-de-atualizacao-dos-dados.md</a></td></tr><tr><td><strong>Firewall</strong></td><td></td><td><a href=".gitbook/assets/firewall (2).png">firewall (2).png</a></td><td><a href="https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/firewall">https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/firewall</a></td></tr><tr><td><strong>Auditorias</strong></td><td></td><td><a href=".gitbook/assets/auditoria.png">auditoria.png</a></td><td><a href="https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/auditorias">https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/auditorias</a></td></tr><tr><td><strong>Catálogo de relatórios</strong></td><td></td><td><a href=".gitbook/assets/lupa.png">lupa.png</a></td><td><a href="principais-funcionalidades/catalogo-de-relatorios.md">catalogo-de-relatorios.md</a></td></tr><tr><td><strong>White Label</strong></td><td></td><td><a href=".gitbook/assets/web-design (1).png">web-design (1).png</a></td><td><a href="principais-funcionalidades/personalizacao-do-portal-e-tela-de-login.md">personalizacao-do-portal-e-tela-de-login.md</a></td></tr><tr><td><strong>Compartilhar relatórios com usuários externos</strong></td><td></td><td><a href=".gitbook/assets/fornecedor (1).png">fornecedor (1).png</a></td><td><a href="principais-funcionalidades/compartilhamento-com-usuarios-externos.md">compartilhamento-com-usuarios-externos.md</a></td></tr><tr><td><strong>Assistente de IA - Power Pilot</strong></td><td></td><td><a href=".gitbook/assets/Power Embedded - Ícone da Documentação (37).png">Power Embedded - Ícone da Documentação (37).png</a></td><td><a href="principais-funcionalidades/ia-generativa-power-pilot.md">ia-generativa-power-pilot.md</a></td></tr></tbody></table>




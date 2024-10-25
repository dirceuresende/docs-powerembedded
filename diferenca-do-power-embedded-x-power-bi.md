---
icon: square-poll-vertical
---

# Diferença do Power Embedded X Power BI

Uma das dúvidas mais comuns que recebemos é sobre a diferença entre o Power BI e o Power Embedded. Embora ambos se complementem, existem diferenças importantes, e por isso preparamos esta documentação

É fundamental entender que o Power  Embedded não substitui o Power BI. Pelo contrário, ele amplia as capacidades do Power BI, permitindo uma visão ainda mais detalhada dos seus dados e melhorando a organização do ambiente de BI, além de oferecer funcionalidades exclusivas. Se você já quis entregar um portal personalizado para seus clientes, compartilhar relatórios com usuários externos, obter insights detalhados sobre quais relatórios estão sendo mais acessados, ou até contar com um assistente de IA que ajude a analisar seus dados de maneira eficiente, e ao mesmo tempo reduzir custos com licenças do Power BI, o Power Embedded pode ser a solução ideal para esses e outros desafios

## O que é o Power Embedded ?

O Power Embedded é uma solução SaaS que utiliza as capacidades oficiais da Microsoft para incorporar (embed) os relatórios publicados no serviço Power BI diretamente em sua aplicação. Ele oferece uma série de funcionalidades adicionais, que descreveremos ao longo desta documentação. Abaixo, incluímos uma tabela comparando as principais funcionalidades entre as duas soluções. Embora algumas funções sejam semelhantes, o Power Embedded traz melhorias significativas

<table><thead><tr><th>Funcionalidade</th><th width="207" data-type="checkbox">Power BI</th><th data-type="checkbox">Power Embedded</th></tr></thead><tbody><tr><td>Aplicativo</td><td>true</td><td>true</td></tr><tr><td>Modo Escuro</td><td>true</td><td>true</td></tr><tr><td>Atualização Conjunto de dados</td><td>true</td><td>true</td></tr><tr><td>Firewall</td><td>false</td><td>true</td></tr><tr><td>Auditoria</td><td>false</td><td>true</td></tr><tr><td>Catálogo de relatório</td><td>false</td><td>true</td></tr><tr><td>White Label</td><td>false</td><td>true</td></tr><tr><td>Compartilhamento com usuários externos</td><td>false</td><td>true</td></tr><tr><td>IA Generativa</td><td>false</td><td>true</td></tr></tbody></table>

## Funcionalidades e Melhorias



**Aplicativo - Melhoria**

* **Power BI**: No Power BI, o aplicativo é uma maneira de compartilhar relatórios, onde você pode agrupar vários dashboards, relatórios em um único local e compartilhar com diferentes audiências.
* **Power Embedded**: No Power Embedded, essa funcionalidade está disponível com algumas melhorias. É possível criar quantos aplicativos forem necessários, adicionar relatórios de diferentes workspaces e usar o modo TV, que permite a exibição dos relatórios em uma tela com funcionalidade de slideshow de forma nativa. Além disso, a segurança por nível de página (Page Level Security) permite que você defina quais páginas do relatório deseja disponibilizar para cada usuário.

**Modo escuro (Dark Mode) - Funcionalidade**

* **Power BI**: Disponível apenas no Power BI Desktop recentemente.
* **Power Embedded**: O modo escuro está disponível de forma nativa na versão web do Power BI Embedded desde o lançamento da ferramenta.

**Atualização de conjunto de dados - Melhoria**

* **Power BI**: Você pode agendar atualizações de dados no Power BI, mas está limitado a 8 atualizações diárias na licença Pro ou 48 na PPU.
* **Power Embedded**: No Power Embedded, além de agendar atualizações, você tem funcionalidades extras, como a possibilidade de não precisar tomar posse do conjunto de dados e de realizar atualizações sem o limite de 30 minutos entre cada uma. Via API, as atualizações são ilimitadas.

**Firewall - Funcionalidade**

* **Power BI**: No Power Bi, você não consegue de forma nativa restringir os acessos por IP.
* **Power Embedded**: O Power Embedded oferece essa funcionalidade de forma nativa, permitindo que você restrinja o acesso dos usuários com base em endereços IP.

**Auditorias - Melhoria**

* **Power BI**: As auditorias no Power BI são limitadas a métricas de uso, que muitas vezes não fornecem as informações detalhadas que você realmente precisa.
* **Power Embedded**: No Power Embedded, você tem acesso a auditorias detalhadas que fornecem métricas como acessos, permissões e relatórios mais utilizados entre outras auditorias.

**Catálogo de relatórios - Funcionalidade**

* **Power BI**: Não há uma funcionalidade nativa para exibir relatórios que os usuários não têm acesso, mas que podem ser úteis para eles.
* **Power Embedded**: Com o catálogo de relatórios no Power Embedded, você pode mostrar relatórios para os usuários, mesmo que eles ainda não tenham acesso direto, permitindo que eles solicitem permissão se necessário.

**White Label - Melhoria**

* **Power BI**: O Power BI oferece gráficos incríveis, mas não é possível personalizar um ambiente com a identidade visual especifica de cada cliente.
* **Power Embedded**: No Power  Embedded, você pode criar um ambiente personalizado com identidade visual específica para seus clientes ou departamentos, proporcionando uma experiência totalmente customizada.

**Compartilhamento com usuários externos - Melhoria**

* **Power BI**: No Power BI, compartilhar relatórios com usuários externos pode ser complicado, exigindo que os usuários tenham uma conta corporativa ou uma licença específica (Pro ou PPU).
* **Power  Embedded**: No Power Embedded, que utiliza licenças Power BI Embedded ou Fabric, você pode compartilhar seus relatórios de maneira mais flexível com usuários externos sem as mesmas restrições de licença.

**IA Generativa**

* **Power BI**: O Power BI conta com o Copilot, uma IA generativa robusta que auxilia na análise dos dados. No entanto, essa funcionalidade está disponível apenas no SKU F64 do Microsoft Fabric, o que pode não ser financeiramente vantajoso para algumas organizações devido ao seu custo elevado.
* **Power Embedded**: No Power Embedded, há uma IA generativa chamada Power Pilot, que também permite responder perguntas de negócios de forma rápida e eficiente. O grande diferencial é que o Power Pilot oferece essa funcionalidade a um custo significativamente mais acessível, tornando a solução mais atraente do ponto de vista financeiro.

<mark style="color:red;">**Embora o Power Embedded ofereçam soluções poderosas existe algumas limitações que devido a não ter suporte na API que vocês deixam de ter como:**</mark>

* Análise no Excel
* Direct Lake
* Cálculos visuais



## Funcionalidades



<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Aplicativo</strong></td><td></td><td><a href=".gitbook/assets/coleta-de-dados.png">coleta-de-dados.png</a></td><td><a href="principais-funcionalidades/aplicativo-compartilhamento.md">aplicativo-compartilhamento.md</a></td></tr><tr><td><strong>Dark Mode</strong></td><td></td><td><a href=".gitbook/assets/modo-escuro (1).png">modo-escuro (1).png</a></td><td><a href="principais-funcionalidades/modo-escuro.md">modo-escuro.md</a></td></tr><tr><td>A<strong>tualização agendada - Conjunto de dados</strong></td><td></td><td><a href=".gitbook/assets/big-data (2).png">big-data (2).png</a></td><td><a href="principais-funcionalidades/agendamento-de-atualizacao-de-conjunto-de-dados.md">agendamento-de-atualizacao-de-conjunto-de-dados.md</a></td></tr><tr><td><strong>Firewall</strong></td><td></td><td><a href=".gitbook/assets/firewall (2).png">firewall (2).png</a></td><td><a href="https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/firewall">https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/firewall</a></td></tr><tr><td><strong>Auditorias</strong></td><td></td><td><a href=".gitbook/assets/auditoria.png">auditoria.png</a></td><td><a href="https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/auditorias">https://app.gitbook.com/o/Ni2qlbLwzFhjF5ZJ9VB4/s/t2gQSHbraGsYbDGTmWAa/~/changes/194/principais-funcionalidade/auditorias</a></td></tr><tr><td><strong>Catálogo de relatórios</strong></td><td></td><td><a href=".gitbook/assets/lupa.png">lupa.png</a></td><td><a href="principais-funcionalidades/catalogo-de-relatorio.md">catalogo-de-relatorio.md</a></td></tr><tr><td><strong>White Label</strong></td><td></td><td><a href=".gitbook/assets/web-design (1).png">web-design (1).png</a></td><td><a href="principais-funcionalidades/white-label.md">white-label.md</a></td></tr><tr><td><strong>Compartilhar relatórios com usuários externos</strong></td><td></td><td><a href=".gitbook/assets/fornecedor (1).png">fornecedor (1).png</a></td><td><a href="principais-funcionalidades/compartilhamento-com-usuarios-externos.md">compartilhamento-com-usuarios-externos.md</a></td></tr><tr><td><strong>Assistente de IA - Power Pilot</strong></td><td></td><td><a href=".gitbook/assets/Power Embedded - Ícone da Documentação (37).png">Power Embedded - Ícone da Documentação (37).png</a></td><td><a href="principais-funcionalidades/ia-generativa-power-pilot.md">ia-generativa-power-pilot.md</a></td></tr></tbody></table>




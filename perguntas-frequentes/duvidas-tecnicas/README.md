# Dúvidas técnicas

### 1. Como o Power Embedded funciona internamente?

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/Power-Embedded-Internals-Exibicao-do-Relatorio.png" alt=""><figcaption></figcaption></figure>

O funcionamento interno do Power Embedded para exibição dos relatórios está descrito abaixo:

1\) Power Embedded verifica se o usuário logado pode acessar o relatório e envia os dados para aplicar o RLS (se houver)

2\) Power Embedded se autentica na API do Azure e recupera um token para autenticação

3\) Power Embedded envia os metadados necessários para as API’s do Power BI (IDs do Workspace, Relatório e Conjunto de dados)

4\) API do Power BI carrega os dados que estão armazenados nos workspaces e o relatório

5\) API do Power BI monta o elemento iframe apontando para o relatório já pronto e retorna para o sistema

6\) Power Embedded exibe o iframe retornado para o usuário. NENHUM dado do relatório é lido, acessado, armazenado ou trafega pelos servidores do sistema



<figure><img src="https://powerembedded.com.br/wp-content/uploads/2024/04/Power-Embedded-Internals-Importacao-de-Relatorios.png" alt=""><figcaption></figcaption></figure>

O funcionamento interno para importação dos relatórios do Power BI para o Power Embedded está descrito abaixo:

1\) Power Embedded interage com as API’s do Power BI

2\) API retorna os metadados necessários para exibição (IDs do Workspace, Relatório e Conjunto de dados)

3\) Power Embedded armazena os metadados retornados

4\) Administrador gerencia as permissões, RLS, estrutura de pastas e demais atributos do relatório

5\) NENHUM dado pessoal é armazenado pelo Power Embedded, apenas o email e nome dos usuários.

6\) NENHUM dado de relatório é armazenado ou trafega pela rede, ou pelos servidores do Power Embedded



### 2. Segurança interna do Power Embedded

A segurança interna do Power Embedded é extremamente robusta e o sistema utiliza uma arquitetura toda baseada em recursos SaaS auto-gerenciados no Azure, onde a gestão é feita pela Microsoft, backups automáticos e alta disponibilidade da aplicação e do banco de dados por zonas de disponibilidade com failover automático e com garantia de disponibilidade de 99,99%.

O sistema é submetido à diversos e complexos pentests de forma periódica, tanto automáticos feitos por ferramentas de pentest quanto validações e testes manuais, feitos por especialistas de segurança de empresas contratadas.

Todo o ambiente de nuvem é protegido pelo Microsoft Defender for Cloud, que faz a proteção, análise e recomendações de forma proativa e contínua.

O acesso aos recursos do Azure é bloqueado para internet e só acessível através de VPN.

A comunicação entre o sistema e o navegador é criptografa utilizando certificados SSL (HTTPS).

A chave de acesso ao Power BI é armazenada no banco de dados criptografada utilizando o algoritmo mais seguro do mercado (RSA-OEAP) e vários mecanismos de proteção para garantir que mesmo em um eventual acesso indevido ao banco de dados, essa chave não possa ser decodificada, uma vez que o acesso à chave de segurança para descriptografar (que é individual por cliente) fica em um Azure KeyVault onde somente a aplicação possui permissão e conectividade para acessar.

A chave da API pública é criptografada utilizando um algoritmo de HASH que não permite recuperação do valor gerado, assim como o secret de um KeyVault.



### 3. Controles de privacidade e LGPD

O processo de embeddar os relatórios no sistema não requer o carregamento ou leitura de nenhum dado dos nossos clientes.

Todos os dados ficam armazenados nos servidores do Power BI mesmo, em um conjunto de dados publicado em um workspace e o sistema apenas utiliza a API do Power BI para a renderização do relatório (também já publicado no workspace) dentro do sistema.

Sendo assim, não lemos ou coletamos nenhuma informação, apenas realizamos uma chamada HTTP na API do Power BI, que lê os dados e exibe na tela.

Os únicos dados da empresa que são armazenados, são os nomes e e-mails dos usuários cadastrados no sistema, para gerenciamento dos acessos.

A nível de segurança, toda a comunicação do Power Embedded é criptografada ponta-a-ponta, utilizando segurança SSL e HTTPS, além de Azure Firewall e diversos mecanismos de segurança do Azure.



### 4. Diferenças entre o Embedded, "Publicar na Web" e "Inserir Relatório"

Embora as 3 opções permitam embeddar relatórios em websites, sharepoint, e-mail, teams, etc.., elas são bem diferentes.



#### **Embedded**

É uma licença por capacidade, que permite visualizar relatórios de forma segurança (com permissões, RLS, OLS, auditorias de acessos, bloqueios por IP, etc) através de uma aplicação, sem a necessidade de quem está visualizando ter uma licença do Power BI, e controlar todos os visuais, cores, temas, páginas e componentes dos relatórios utilizando linguagem de programação.



#### **Inserir relatório**

Essa é uma forma de compartilhar relatórios em websites, aplicativos, sharepoint, teams, etc.. de forma segura, mantendo todos os controles de segurança do Power BI, como permissões, RLS, OLS e auditorias de acesso.

Diferente do Embedded, nesse modo de compartilhamento, **todos os usuários que vão acessar o relatório, precisam de ter uma licença** Pro ou PPU (ou capacidade Premium).

Além disso, você **NÃO** consegue controlar os elementos do relatório via linguagem de programação para criar/editar visuais dinamicamente, trocar temas, criar/excluir páginas, etc..



#### **Publicar na Web**

É uma forma de compartilhar relatórios de graça, sem que a pessoa que está visualizando precise ter uma conta ou licença do Power BI. Ela funciona muito bem quando você precisa compartilhar relatórios que contém **dados públicos**, isto é, não há preocupação com vazamento de dados.

Diferente do Embedded, no “Publicar na Web” não existe nenhuma segurança: Qualquer pessoa que tenha acesso ao link do relatório, irá visualizá-lo, sem qualquer controle a nível de usuário, como RLS ou OLS, não há necessidade de quem está visualizando ser cadastrado em nenhuma aplicação e não há auditoria para saber quem está visualizando o relatório. Qualquer pessoa poderá estar visualizando os dados da sua empresa e você não saberá quem.

Além disso, como já amplamente divulgado na internet, todos os relatórios publicados desta forma, podem ser acessados através de consultas simples ao Google, mesmo que o link nunca tenha sido publicado em nenhum local.

Mesmo que você tente bloquear o acesso utilizando uma senha para abrir o portal, esse tipo de mecanismo é facilmente quebrado em poucos segundos, utilizando a opção de Developer Tools do navegador e a pessoa terá acesso irrestrito aos dados publicados no relatório.



### 5. Processo de publicação dos relatórios

O processo de importação e publicação dos relatórios no Power Embedded é praticamente o mesmo que já existe no Power BI serviço tradicional:

* Usuário abre o Power BI Desktop e cria o relatório.
* Usuário publica o relatório no workspace desejado.
* Administrador do Power Embedded importa o relatório do workspace do Power BI para o sistema.

<figure><img src="https://powerembedded.com.br/wp-content/uploads/2023/09/Importar-Relatorios.png" alt=""><figcaption></figcaption></figure>



* Administrador do Power Embedded atribui as permissões via grupo ou usuário individualmente.
* Administrador do Power Embedded define as regras de RLS do conjunto de dados (caso tenha).
* Usuário acessa o relatório pelo Portal de visualização do Power Embedded.



### 6. Atualizações do sistema

O Power Embedded é um sistema muito dinâmico, e o nosso time está sempre atento aos pedidos e necessidades dos nossos clientes e também aos novos recursos disponibilizados pela Microsoft.

Temos um tempo de desenvolvimento e implantação bem rápido, o que nos permite realizar de 2 a 5 atualizações de melhorias e novas funcionalidades **por semana**.

Sempre que uma funcionalidade ou melhoria for implementada, aplicamos e disponibilizados **gratuitamente** para todos os nossos clientes, de forma automática.



### 7. Personalizações do sistema

Caso seja solicitada uma alteração no Power Embedded e personalização não poderá ser aplicada para os demais clientes e ficará restrita apenas para a sua empresa, iremos agendar uma reunião com a sua equipe para entender melhor a sua necessidade e enviaremos uma proposta comercial para implantar essa personalização no sistema.

Se a sua sugestão/ideia puder ser aplicada para os outros clientes, não há cobrança de desenvolvimento.

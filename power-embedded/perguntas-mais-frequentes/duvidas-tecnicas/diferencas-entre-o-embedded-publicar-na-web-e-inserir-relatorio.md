# Diferenças entre o Embedded, "Publicar na Web" e "Inserir Relatório"

Embora as 3 opções permitam embeddar relatórios em websites, sharepoint, e-mail, teams, etc.., elas são bem diferentes.



### **Embedded**

É uma licença por capacidade, que permite visualizar relatórios de forma segurança (com permissões, RLS, OLS, auditorias de acessos, bloqueios por IP, etc) através de uma aplicação, sem a necessidade de quem está visualizando ter uma licença do Power BI, e controlar todos os visuais, cores, temas, páginas e componentes dos relatórios utilizando linguagem de programação.



### **Inserir relatório**

Essa é uma forma de compartilhar relatórios em websites, aplicativos, sharepoint, teams, etc.. de forma segura, mantendo todos os controles de segurança do Power BI, como permissões, RLS, OLS e auditorias de acesso.

Diferente do Embedded, nesse modo de compartilhamento, **todos os usuários que vão acessar o relatório, precisam de ter uma licença** Pro ou PPU (ou capacidade Premium).

Além disso, você **NÃO** consegue controlar os elementos do relatório via linguagem de programação para criar/editar visuais dinamicamente, trocar temas, criar/excluir páginas, etc..



### **Publicar na Web**

É uma forma de compartilhar relatórios de graça, sem que a pessoa que está visualizando precise ter uma conta ou licença do Power BI. Ela funciona muito bem quando você precisa compartilhar relatórios que contém **dados públicos**, isto é, não há preocupação com vazamento de dados.

Diferente do Embedded, no “Publicar na Web” não existe nenhuma segurança: Qualquer pessoa que tenha acesso ao link do relatório, irá visualizá-lo, sem qualquer controle a nível de usuário, como RLS ou OLS, não há necessidade de quem está visualizando ser cadastrado em nenhuma aplicação e não há auditoria para saber quem está visualizando o relatório. Qualquer pessoa poderá estar visualizando os dados da sua empresa e você não saberá quem.

Além disso, como já amplamente divulgado na internet, todos os relatórios publicados desta forma, podem ser acessados através de consultas simples ao Google, mesmo que o link nunca tenha sido publicado em nenhum local.

Mesmo que você tente bloquear o acesso utilizando uma senha para abrir o portal, esse tipo de mecanismo é facilmente quebrado em poucos segundos, utilizando a opção de Developer Tools do navegador e a pessoa terá acesso irrestrito aos dados publicados no relatório.


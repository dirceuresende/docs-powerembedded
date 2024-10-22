# Controles de privacidade e LGPD

O processo de embeddar os relatórios no sistema não requer o carregamento ou leitura de nenhum dado dos nossos clientes.

Todos os dados ficam armazenados nos servidores do Power BI mesmo, em um conjunto de dados publicado em um workspace e o sistema apenas utiliza a API do Power BI para a renderização do relatório (também já publicado no workspace) dentro do sistema.

Sendo assim, não lemos ou coletamos nenhuma informação, apenas realizamos uma chamada HTTP na API do Power BI, que lê os dados e exibe na tela.

Os únicos dados da empresa que são armazenados, são os nomes e e-mails dos usuários cadastrados no sistema, para gerenciamento dos acessos.

A nível de segurança, toda a comunicação do Power Embedded é criptografada ponta-a-ponta, utilizando segurança SSL e HTTPS, além de Azure Firewall e diversos mecanismos de segurança do Azure.

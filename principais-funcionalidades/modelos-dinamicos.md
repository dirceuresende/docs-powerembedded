# Modelos Dinâmicos

Modelos dinâmicos ou Dynamic Dataset Binding, é uma funcionalidade exclusiva do Power Embedded e que não está disponível no Power BI serviço, onde permitem que um único relatório seja acessado por diferentes clientes, cada um visualizando dados específicos de acordo com seu modelo semântico. Isso elimina a necessidade de criar múltiplos relatórios, evitando inconsistências de dados e cálculos, já que todas as atualizações são aplicadas de forma centralizada.

Essa funcionalidade supera a segurança ao nível de linha (RLS) em desempenho e segurança. Enquanto o RLS aumenta o tamanho do modelo e o consumo de processamento devido às várias regras criadas para diferentes usuários, os modelos dinâmicos consultam apenas o modelo específico para cada cliente. Isso resulta em modelos menores, independentes e isolados, melhorando a eficiência e reduzindo riscos de falhas de segurança.

Os modelos dinâmicos permitem que diferentes clientes (Cliente A, Cliente B, Cliente C) acessem o mesmo relatório, aplicando filtros ao nível de modelo. Por exemplo, se o usuário está associado ao modelo A, o sistema irá conectar o relatório ao modelo A dinamicamente, sem precisar filtrar os dados.







<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td></td><td>Modelos Dinâmicos </td><td></td><td><a href="../.gitbook/assets/Group 37.png">Group 37.png</a></td><td><a href="../portal-de-administracao/relatorios/modelos-dinamicos.md">modelos-dinamicos.md</a></td></tr></tbody></table>

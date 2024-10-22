# Como o Power Embedded funciona internamente?

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



### Documentação interna do Power Embedded

{% embed url="https://powerembedded.com.br/arquitetura" %}

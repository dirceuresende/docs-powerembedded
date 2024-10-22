# Permissões

Ao acessar dados em diversos relatórios, é fundamental entender quais relatórios estão sendo consultados e as permissões e grupos aos quais o usuário está vinculado.

Para facilitar essa gestão, o Power Embedded oferece uma funcionalidade de auditoria de permissões, proporcionando uma visão clara e detalhada das permissões atribuídas aos usuários e grupos, incluindo regras de segurança (RLS).

<figure><img src="../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure>



### Tipos de Permissões

As permissões podem ser atribuídas de quatro formas diferentes:

* **Grupo – Permissão**\
  O usuário é associado a um grupo existente, que recebe acesso ao relatório com base nas permissões concedidas ao grupo.\

* **Grupo – RLS**\
  Grupos são vinculados a regras de _Row-Level Security_ (RLS) estáticas, garantindo que cada grupo visualize apenas os dados relevantes a ele.\

* **Usuário – Permissão**\
  Permissão direta é concedida ao usuário para acessar um relatório específico por meio de cadastro individual.\

* **Usuário – RLS**\
  Regras de RLS específicas são atribuídas ao relatório para controlar quais dados o usuário pode acessar.



### Exportação de Dados

O administrador tem a opção de exportar as informações de auditoria em formatos CSV ou Excel. Esses arquivos podem ser usados para análises aprofundadas no Power BI ou Excel, oferecendo um panorama detalhado das permissões e acessos.

<figure><img src="../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>



### Filtros Disponíveis

Para facilitar a busca, o portal permite filtrar as informações por:

* E-mail do usuário
* Nome do relatório
* Workspace
* Detalhe da permissão
* Tipo de permissão

<figure><img src="../../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>



Essa abordagem torna o gerenciamento de acessos mais eficiente e seguro, garantindo que cada usuário tenha a permissão adequada de acordo com seu perfil e necessidades.

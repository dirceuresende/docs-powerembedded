# Modelos dinâmicos

Modelos dinâmicos ou Dynamic Dataset Binding, é uma funcionalidade exclusiva do Power Embedded e que não está disponível no Power BI serviço, desenvolvida para cenários nos quais um único relatório é acessado por diferentes clientes, cada um utilizando um modelo semântico diferente, e por isso, visualizam dados diferentes.

Seria possível ter esse mesmo comportamento criando vários relatórios para atender essa necessidade de visualizar dados diferentes conforme o usuário que está visualizando, mas se você precisar ajustar medidas ou até mesmo melhorar um visual, teria que alterar todos os relatórios, o que poderia causar inconsistências de dados e cálculos entre os relatórios

Utilizando os modelos dinâmicos, ao atualizar um único relatório, todos visualizarão as mudanças da mesma forma, uma vez que será apenas um único relatório e N modelos associados dinamicamente.

A maior vantagem dessa funcionalidade em relação à segurança ao nível de linha (RLS) é na performance e na própria segurança.

Isso se deve ao fato de que, ao aplicar muitas regras de segurança ao nível de linha (RLS) em um modelo semântico, o modelo acaba ficando muito grande, pois contém dados de vários clientes, por exemplo, e isso pode causar um aumento significativo no consumo de capacidade de processamento, pois cada regra cria um subconjunto de dados separado internamente.

Um modelo dinâmico irá consultar um modelo específico conforme o usuário que está visualizando o relatório, resultando em modelos menores, independentes e isolados, o que não só pode melhorar o desempenho, mas também fortalecer a segurança, mesmo em casos de erros nas medidas que controlam o RLS.



**Exemplo de modelos dinâmicos**

<div align="left"><figure><img src="../../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure></div>

Os modelos dinâmicos permitem que diferentes clientes (Cliente A, Cliente B, Cliente C) acessem o mesmo relatório, aplicando filtros ao nível de modelo. Por exemplo, se o usuário está associado ao modelo A, o sistema irá conectar o relatório ao modelo A dinamicamente, sem precisar filtrar os dados.

\


**Exemplo de uso**

Ao adicionar um modelo, clicando no botão “Adicionar modelo”, você terá acesso a todos os conjuntos de dados importados.

<figure><img src="../../../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

Você poderá selecionar o conjunto de dados desejado e atribuir quais usuários pertencem a esse modelo.

<figure><img src="../../../.gitbook/assets/image (217).png" alt=""><figcaption></figcaption></figure>

A partir desse momento, quando o usuário acessar o relatório, será o modelo semântico será alterado automaticamente conforme a regra atribuída.

Por exemplo: Quando o usuário “cliente1@hotmail.com” acessar o portal, ele será identificado como parte do conjunto de dados “Demo 01” e visualizará apenas as informações relevantes ao seu perfil.&#x20;

É possível incluir vários usuários e/ou grupos em um único conjunto de dados e associar múltiplos conjuntos no relatório conforme necessário, lembrando que a estrutura dos dados (nome das tabelas, colunas, medidas e relacionamentos) deve ser igual entre os conjuntos de dados dinâmicos.

Para atribuir um usuário a um conjunto de dados, basta clicar em “Ações” > “Gerenciar” e escolher quais usuários ou grupos farão parte dele.

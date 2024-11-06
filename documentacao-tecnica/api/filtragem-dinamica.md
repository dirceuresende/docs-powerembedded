# Filtragem dinâmica

Quando você está utilizando o recurso de [mostrar os relatórios do Power BI no seu sistema](mostrar-relatorio-no-seu-sistema.md), muitas vezes é necessário aplicar uma filtragem nos dados automaticamente ao abrir o relatório.

Esse recurso se chama filtragem dinâmica e está disponível no Power Embedded.



### 1. Como configurar a filtragem dinâmica

Para configurar a filtragem dinâmica, acesse a página de [Conjuntos de dados](https://admin.powerembedded.com.br/Datasets).

Pesquise pelo conjunto de dados que você gostaria de configurar a filtragem dinâmica, clique no botão **Ações** e selecione a opção **Filtragem dinâmica (API)**.

<figure><img src="../../.gitbook/assets/image (390).png" alt=""><figcaption></figcaption></figure>



Essa é a tela de configuração da filtragem dinâmica:

<figure><img src="../../.gitbook/assets/image (398).png" alt=""><figcaption></figcaption></figure>



Na tela de filtragem dinâmica, você precisará configurar 3 parâmetros:

*   **Nome da propriedade na chamada da API**: Esse é o nome da propriedade que será utilizada para passar o valor a ser filtrado na chamada da API. Esse nome da propriedade pode ser definido por você, e deverá ser utilizado na chamada da API.\


    <figure><img src="../../.gitbook/assets/image (392).png" alt=""><figcaption></figcaption></figure>


*   **Nome do parâmetro no modelo**: Esse é o nome da tabela e da coluna que serão filtrados no seu relatório. O formato desse campo deve seguir o padrão tabela/coluna e é case sensitive, ou seja, existe diferença entre maiúsculo e minúsculo e deve ser igual ao que está no Power BI.\


    <figure><img src="../../.gitbook/assets/image (393).png" alt=""><figcaption></figcaption></figure>


* **Operador**: Qual o operador de comparação deve ser utilizado para filtrar os dados. Na grande maioria dos casos, o operador será o "=".



### 2. Como utilizar a filtragem dinâmica

Para utilizar a filtragem dinâmica, você irá utilizar o parâmetro **customFilters** no JSON da chamada da API.

Exemplo de requisição JSON com CustomFilters e 2 parâmetros:

```json
{
  "userEmail": "dirceu.resende@powertuning.com.br",
  "organizationId": "4b532635-a0c6-48ae-bea8-a5197c63f057",
  "reportId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "customFilters": [
    {
      "key": "_loja", // Parâmetro de Loja que irá filtrar dLojas/FD_LOJA
      "value": "5" // O código da loja que será filtrada
    },
    {
      "key": "_funcionario", // Parâmetro de funcionário que irá filtrar
      "value": "12" // O código do funcionário que será filtrado
    }
  ]
}
```



Retorno da chamada da API:

<figure><img src="../../.gitbook/assets/image (394).png" alt=""><figcaption></figcaption></figure>

Ao incorporar essa URL no seu sistema, o usuário será direcionado para essa URL:

_https://demo.powerembedded.com.br/Organization/4b532635-a0c6-48ae-bea8-a5197c63f057/Report/a91ff398-849d-40bd-b40a-e40229f273eb<mark style="color:red;">**?filter=dLojas/FD\_LOJA eq 5 and dFuncionarios/FD\_FUNCIONARIO eq 12**</mark>_



Ao abrir o relatório, podemos observar que os dados foram filtrados corretamente:

<figure><img src="../../.gitbook/assets/image (395).png" alt=""><figcaption></figcaption></figure>



### 3. Observações sobre a filtragem dinâmica

* As colunas que serão filtradas, obrigatoriamente devem estar listadas na barra de Filtros do relatório.
* O nome da tabela e da coluna é case sensitive, ou seja, tem diferença entre maiúsculo e minúsculo. O nome deve ser exatamente igual ao que está no modelo.
* Os nomes de **Tabela** e de **Campo** diferenciam maiúsculas de minúsculas, o de **valor** não.
* Os campos ocultos na exibição de relatório ainda podem ser filtrados.
* Evite utilizar acentos e espaços no nome da coluna ou tabela.
* Para mais informações, consulte [essa documentação](https://learn.microsoft.com/pt-br/power-bi/collaborate-share/service-url-filters) da Microsoft.

# Filtrar relatórios usando parâmetros de consulta na URL

Ao abrir um relatório do Power BI, cada página do relatório tem sua própria URL exclusiva. Para filtrar essa página do relatório, é possível usar o painel Filtros na tela de relatório. Outra opção é adicionar os parâmetros de consulta na URL para filtrar o relatório. Talvez você tenha um relatório que gostaria de mostrar aos colegas, mas antes deseja filtrá-lo previamente para enviar a eles. Uma maneira de filtrar isso é iniciar com a URL padrão do relatório, adicionar os parâmetros de filtro na URL.

Assim como o Power BI serviço suporta os [parâmetros de URL para filtrar os dados](https://learn.microsoft.com/pt-br/power-bi/collaborate-share/service-url-filters?wt.mc\_id=MVP\_398902), o Power Embedded agora também suporta os mesmos parâmetros para filtrar os dados dos relatórios.

&#x20;

### Sintaxe dos parâmetros da cadeia de caracteres de consulta para filtragem <a href="#query-string-parameter-syntax-for-filtering" id="query-string-parameter-syntax-for-filtering"></a>

_URL do relatório_**?filter=**_**Tabela**_**/Coluna eq '**_**valor**_**'**

\
**Exemplo:**\
https://relatorios.powerembedded.com.br/Organization/12201800-1a46-491a-bfe3-6ee5590e372e/Report/a0397cac-3ced-40e0-a1b4-6011518391c2**?filter=Participantes/email eq 'dirceu.resende@yahoo.com.br'**

<figure><img src="../../.gitbook/assets/image (399).png" alt=""><figcaption></figcaption></figure>

Para ver mais informações sobre os tipos de filtros suportados, como filtrar utilizando múltiplos valores e múltiplas campos, acesse a página [Filtrar relatórios usando parâmetros da cadeia de caracteres de consulta na URL](https://learn.microsoft.com/pt-br/power-bi/collaborate-share/service-url-filters?wt.mc\_id=MVP\_398902).

\
**Observações**

* Os nomes de **Tabela** e de **Campo** diferenciam maiúsculas de minúsculas, o de **valor** não.
* Os campos ocultos na exibição de relatório ainda podem ser filtrados.
* Para esse recurso funcionar, a coluna que será utilizada para filtrar os dados deve estar disponível painel lateral de filtros do relatório.

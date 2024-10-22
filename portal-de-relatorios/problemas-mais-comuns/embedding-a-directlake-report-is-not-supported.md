# Embedding a DirectLake report is not supported

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Essa mensagem é bem clara e significa que a API oficial do Power BI para inserir os relatórios no Power BI ainda não suporta relatórios que utilizem o modo de conexão DirectLake.

Essa informação pode ser confirmada na página [Direct Lake overview](https://learn.microsoft.com/en-us/fabric/get-started/direct-lake-overview#known-issues-and-limitations)

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



Enquanto a API oficial do Power BI não suportar essa funcionalidade, não será possível utilizar relatórios utilizando DirectLake no Power Embedded.

Uma alternativa para isso é alterar o modo de conexão para Import, conectado no Lakehouse ou Datawarehouse do Fabric.

No artigo [Direct Lake vs. Import mode in Power BI](https://www.sqlbi.com/blog/marco/2024/04/06/direct-lake-vs-import-mode-in-power-bi/) do Marco Russo e Alberto Ferrari (SQLBI), dois dos maiores especialistas em Power BI no mundo, eles explicam que o Direct Lake resolve problemas para 2-3% dos modelos que eram difíceis de gerenciar no modo de importação (aqueles modelos acima de 200/400 GB). No entanto, se seu modelo funciona bem no Import, não há razão para usar o Direct Lake. Você pode continuar a usar o Import do seu lakehouse se preferir armazenar dados em um lakehouse.

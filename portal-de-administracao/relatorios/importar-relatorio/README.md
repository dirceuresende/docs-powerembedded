# Importar relatório

### Opções de importação

Existem três tipos de importação de relatórios:

1. **Relatório do Power BI**: Esta opção permite importar relatórios que já existem no Power BI.
2. **Relatório da Web**: É possível importar relatórios de diversas fontes online, como Google Data Studio, documentos no OneDrive e Tableau, além de relatórios presentes nos Workspaces do Power BI.
3. **Arquivo do Power BI**: Com esta funcionalidade, você pode publicar arquivos PBIX diretamente no Power BI sem precisar utilizar o Power BI Desktop.



### **Relatório do Power BI**

Nesta opção, você pode visualizar os workspaces em que o Power Embedded tem permissão de Administrador e importar esses relatórios.

<figure><img src="../../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>



Ao selecionar o workspace, serão listados todos os relatórios do workspace que não foram importados ainda. Você pode optar por importá-los manualmente um a um ou importar todos de uma vez.

<figure><img src="../../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Caso o workspace do relatório que você quer importar não esteja aparecendo no drop-down acima, provavelmente é porque o usuário do Power Embedded (PowerEmbedded-App) não está com permissão de Administrador no workspace lá no Power BI Serviço.
{% endhint %}



### **Relatório Web**

No Power Embedded, você pode incorporar relatórios da Web ou documentos armazenados no SharePoint, OneDrive, entre outros.

Por exemplo, se você possui um dashboard no Google Data Studio e precisa visualizá-lo aqui, basta inserir o link e ele será automaticamente reconhecido como um relatório externo no portal.

<figure><img src="../../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

Como alguns sites não permitem esse processo de incorporação direta, oferecemos a opção de “Abrir em uma nova aba externa” para facilitar essa integração.



### **Arquivo do Power BI**

Também é possível publicar os relatórios do Power BI que estão localmente em seus computadores para os workspaces no Power BI serviço, dando uma liberdade e autonomia maior para os usuários.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Para saber mais sobre essa funcionalidade, acesse a página [Publicando relatórios no Power BI pelo Power Embedded](../publicar-relatorio-no-power-bi.md).
{% endhint %}

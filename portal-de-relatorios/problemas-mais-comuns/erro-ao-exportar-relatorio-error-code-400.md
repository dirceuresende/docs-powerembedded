# Erro ao exportar relatório - Error Code 400

<figure><img src="../../.gitbook/assets/Error exporting report.jpg" alt=""><figcaption></figcaption></figure>

Esse erro geralmente ocorre por falta de permissão para exportar dados, sendo mais comum quando está tentando exportar o relatório utilizando o formato "Imagem (PNG)".

Neste artigo, será explicado o passo a passo de como ativar essa permissão para conseguir realizar a exportação dos relatórios no formato desejado.



## 1. Acessar o Portal de Administração no Power BI Service

Utilizando um usuário com permissão de Administrador no Power BI (Fabric Administrator), acesse o [Portal de Administração do Power BI](https://app.powerbi.com/admin-portal/tenantSettings).



## 2. Como verificar se as permissões necessárias estão ativadas

Na página do Portal de Administração, no menu **Configurações de locatário**, pesquise pela palavra **"Exportar"** na barra de pesquisa que fica localizada na parte superior direita da tela.

Encontre a seção **"Configurações de compartilhamento e de exportação"** e veja se o Power BI está permitindo as exportações abaixo:

* Exportar para Excel (Usado pelo menu "Exportar dados" no visual)
* Exportar para .csv (Usado pelo menu "Exportar dados" no visual)
* Exportar relatório como apresentações em Power Point ou documentos PDF (Botão Exportar)
* Exportar os relatórios como arquivos de imagem (Botão Exportar)

<figure><img src="../../.gitbook/assets/image (387).png" alt=""><figcaption></figcaption></figure>



## 3. Como ativar as permissões necessárias

Caso alguma dessas permissões esteja desabilitada, algumas funcionalidades de exportação de dados não estarão disponíveis no Power Embedded ou apresentarão uma mensagem de erro ao tentar utilizá-las.

No exemplo abaixo, será demonstrado como **habilitar** a permissão "**Exportar os relatórios como arquivos de imagem**", que vem desabilitado por padrão.&#x20;

<figure><img src="../../.gitbook/assets/image (389).png" alt=""><figcaption></figcaption></figure>

Após a alteração acima, você poderá exportar seus relatórios como um arquivo de imagem PNG.


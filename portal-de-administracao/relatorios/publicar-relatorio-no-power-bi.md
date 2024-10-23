# Publicar relatório no Power BI

Uma das maiores solicitações dos usuários é conseguir publicar os relatórios do Power BI que estão localmente em seus computadores para os workspaces no Power BI serviço, dando uma liberdade e autonomia maior para os usuários.

Por este motivo, o Power Embedded passou a oferecer essa funcionalidade para todos os clientes.



### Publicando relatórios do Power BI

Para publicar relatórios do Power BI, diretamente pelo Power Embedded, acesse a página de [Relatórios](https://admin.powerembedded.com.br/Reports).

Clique no botão _**Importar**_ > _**Arquivo do Power BI**_

<figure><img src="../../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

Na tela que foi aberta, _**selecione o arquivo**_ que deseja publicar.

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

Após isso, selecione _**em qual workspace**_ você deseja publicar o relatório.

Agora você precisa definir o que fazer se já existir um modelo semântico com o mesmo nome do arquivo que você está importando:

* _**Ignorar (cria com o mesmo nome)**:_ Se já existir um conjunto de dados com o mesmo nome, a operação de importação criará um novo conjunto de dados com o mesmo nome.
* _**Cancelar o envio:**_ Se o conjunto de dados com o mesmo nome já existirem, a operação de importação será cancelada.
* _**Criar ou sobrescrever:**_ Se já existir um conjunto de dados com o mesmo nome, a operação de importação substituirá o conjunto de dados existente pelo novo. A operação de importação falhará se houver mais de um conjunto de dados existente com o mesmo nome.

Por fim, você pode marcar a opção _**Criar apenas o modelo semântico (não criar o relatório)**_, caso você queira apenas publicar o modelo semântico, sem criar o relatório automaticamente (que é o padrão do Power BI).



### Como criar uma conta de armazenamento

<details>

<summary>Clique aqui para visualizar esse tópico</summary>

Antes de configurar a integração entre o Power Embedded e a conta de armazenamento, você precisará [criar a sua conta de armazenamento](https://portal.azure.com/#browse/Microsoft.Storage%2FStorageAccounts) no Portal do Azure.

Para realizar a criação, pode utilizar os valores padrão, conforme demonstrado abaixo:

![](<../../.gitbook/assets/image (208).png>)



Ative a opção _**Permitir a habilitação do acesso anônimo em contêineres individuais:**_

![](<../../.gitbook/assets/image (209).png>)



Pode revisar as outras configurações, mas para fins deste tutorial, já pode avançar e concluir a criação da conta de armazenamento.

Após a criação, acesse a conta de armazenamento criada.

Expanda a seção _**Armazenamento de dados**_ e selecione a opção _**Contêineres**_.

Clique no botão _**+Contêiner**_

![](<../../.gitbook/assets/image (210).png>)



Digite o nome do contêiner que você deseja criar e clique no botão _**Criar**_, no final da tela.

Anote o nome do contêiner criado em um bloco de notas, pois você irá utilizá-lo futuramente para configurar a conta de armazenamento.

Expanda a seção _**Segurança + rede**_ e selecione a opção _**Chaves de acesso**_.

Nesta tela, você irá copiar e salvar em um bloco de notas, os valores dos campos _**Nome da conta de armazenamento**_ e _**Chave**_ (precisa clicar no botão _**Mostrar**_ para conseguir copiar a chave), pois iremos utilizar esses valores na configuração da conta de armazenamento.

![](<../../.gitbook/assets/image (211).png>)



Agora expanda a seção _**Configurações**_ e selecione a opção _**Compartilhamento de recursos (CORS)**_

![](<../../.gitbook/assets/image (212).png>)



Preencha os campos conforme a imagem acima:

* _**Origens permitidas**_: https://admin.powerembedded.com.br
* _**Métodos permitidos**_: PUT
* _**Cabeçalhos permitidos**_: \*

</details>



### Configuração da conta de armazenamento

<details>

<summary>Clique aqui para visualizar esse tópico</summary>

Para realizar a publicação dos relatórios, o Power BI precisa fazer o upload temporariamente do arquivo do Power BI que está no seu computador para uma conta de armazenamento do Azure.

Após esse envio, o Power Embedded faz uma chamada na API do Power BI, informando a URL do arquivo que está na conta de armazenamento (Azure Blob Storage) para importar no workspace. Após a importação, o arquivo é apagado do armazenamento temporário.

**Por padrão**, uma conta de armazenamento do próprio Power Embedded é utilizada para esse armazenamento temporários dos arquivos do Power BI. Sendo assim, você não precisa criar ou configurar uma integração do Power Embedded com uma conta de armazenamento.

Entretanto, é compreensível que você possa preferir utilizar uma conta de armazenamento da sua empresa, por questões de segurança e privacidade dos dados para armazenar temporariamente os arquivos que serão enviados e posteriormente, publicados no Power BI serviço.

Essa integração utilizando a conta de armazenamento da sua empresa pode ser configurada na tela abaixo, que fica na página de _**Configurações**_ > Aba _**Parâmetros**_:

![](<../../.gitbook/assets/image (213).png>)\


Abra o bloco de notas com as informações que você salvou e agora você pode configurar a sua integração entre o Power Embedded e a conta de armazenamento temporária criada por você.

Exemplo dessa tela de configuração com as informações devidamente preenchidas:

![](<../../.gitbook/assets/image (214).png>)

</details>



Pronto! Seus usuários já podem realizar a publicação dos arquivos do Power BI pelo Power Embedded.

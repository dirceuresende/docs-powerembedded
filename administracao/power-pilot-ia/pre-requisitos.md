# Pré-requisitos

### Como configurar o PowerPilot (IA) no Power Embedded

Para que você tenha um assistente no portal, é preciso fazer a configuração dos seguintes passos:

1. Validar os [pré-requisitos](pre-requisitos.md) no Portal de Administração do Power BI (você está aqui)
2. Contratar o modelo no [Azure OpenAI](contratacao-de-uma-ia/azure-openai.md) ou [OpenAI (ChatGPT)](contratacao-de-uma-ia/openai.md)
3. [Criar um modelo](modelos-de-ia.md) no Power Embedded
4. [Criar um assistente](assistentes-de-ia.md) no Power Embedded



Antes de prosseguir com a criação do seu modelo, verifique no Power BI se as permissões listadas abaixo estão ativadas.

A configuração dessas permissões é essencial para que você possa criar o assistente sem problemas.&#x20;

Algumas permissões já podem estar ativadas, pois são configuradas durante a instalação do Power Embedded.

No entanto, devido a atualizações frequentes do Power BI, pode ser necessário habilitar essas permissões manualmente para garantir o funcionamento correto do assistente.



### Permissões necessárias no Portal de Administração do Power BI

Utilizando um usuário com permissão de administrador do Power BI, acesse [este link aqui](https://app.powerbi.com/admin-portal/tenantSettings).

Desça a página até encontrar a seção **“Configurações do Desenvolvedor”** (ou busque por **“api”** na barra de busca à direita)

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

Marque a opção "**As entidades de serviço podem usar APIs do Fabric"**.

Por questões de segurança, marque a opção "**Especificar grupos de segurança"** na seção "Aplicar em:" e selecione o grupo de segurança que criamos no começo deste tópico (no meu caso, "PowerEmbedded-Group")

<figure><img src="../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

Clique no botão “Aplicar”.



Desça mais um pouco na página e repita o mesmo processo para os seguintes itens:

* **As entidades de serviço podem acessar APIs de administrador somente leitura**
* **Entidades de serviço podem acessar APIs de administrador usadas para atualizações**
* **Aprimorar as respostas das APIs de administração com metadados detalhados**
* **Aprimorar as respostas das APIs de administração com expressões DAX e Mashup (se estiver desativado, atualize a página do navegador e tente novamente)**

Isso deve ser feito na seção **Configurações da API de Administração**.

Após concluir essas etapas, podemos seguir para as próximas configurações.

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

Ainda na categoria **“Configurações do desenvolvedor”**, ou pesquisando por “inserir” na barra de busca, marque a opção **“Inserir conteúdo em aplicativos”** e adicione o grupo de segurança que você criou no filtro “Grupos de segurança específicos”, na opção “Aplicar em”.

Caso essa configuração já esteja ativada e permitida para toda a organização, sendo o padrão do Power BI, pode deixar assim.&#x20;

Alterar isso pode causar problemas em outros processos, caso estejam utilizando algo que necessite dessa permissão.

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

E por último, na seção **“Configurações de integração”**, faça o mesmo processo para a configuração **“Permitir pontos de extremidade XMLA e analisar no Excel com modelos semânticos locais”**, que serve para permitir a listagem das roles de RLS de forma automática.

Caso essa configuração já esteja ativada e permitida para toda a organização, sendo o padrão do Power BI, pode deixar assim.&#x20;

Alterar isso pode causar problemas em outros processos, caso estejam utilizando algo que necessite dessa permissão.

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

Pronto! Agora o Portal possui acesso ao seu ambiente do Power BI.

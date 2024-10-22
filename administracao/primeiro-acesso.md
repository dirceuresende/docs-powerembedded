---
description: >-
  Dicas das configurações inicias para ter uma boa experiência na utilização do
  Power Embedded
---

# Primeiro Acesso

{% hint style="info" %}
Para personalizar a URL do portal e utilizar o seu domínio, acesse [Configuração de DNS](configuracao-dns/)
{% endhint %}



### Criação dos usuários

O primeiro passo para começar a utilizar o Power Embedded, é configurar os usuários que irão administrar a plataforma e os que irão apenas visualizar os relatórios.

Para acessar essa tela, [clique aqui](https://admin.powerembedded.com.br/Users).



Após a criação dos usuários, lembre-se de definir as permissões desses usuários, configurar quais grupos eles fazem parte, quais relatórios irão acessar e as permissões que eles terão.

{% hint style="info" %}
Para saber mais sobre a criação e gerenciamento dos usuários, acesse a página Usuários
{% endhint %}



Você pode criar usuários de várias formas diferentes:

* Criar manualmente os usuários, preenchendo os campos do formulário de cadastro
* Importar uma lista de usuários a partir de arquivos CSV
* Importar uma lista de usuários a partir do Entra ID (Azure AD)
* Utilizar a API para integração com qualquer sistema ou linguagem de programação

<div data-full-width="false">

<figure><img src="../.gitbook/assets/2024-10-15 05 26 34.png" alt=""><figcaption><p>Tela inicial do cadastro de usuários</p></figcaption></figure>

</div>



### Criação dos grupos

Os grupos no Power Embedded são uma forma de facilitar a gestão e governança dos usuários, agrupando-os para facilitar o gerenciamento das permissões, RLS e acessos a relatórios.

Para acessar essa tela, [clique aqui](https://admin.powerembedded.com.br/Groups).

{% hint style="info" %}
Para saber mais sobre a criação e gerenciamento dos grupos, acesse a página Grupos.
{% endhint %}



Você pode criar os grupos de várias formas:

* Criar manualmente os grupos, preenchendo os campos do formulário manualmente
* Importar os grupos a partir de arquivos CSV
* Importar os grupos a partir do Entra ID (Azure AD) e opcionalmente, importar também os usuários deste grupos
* Sincronizar os grupos com o Entra ID (Azure AD), que irá criar/excluir os usuários no Power Embedded conforme o que acontece nesse grupo pelo Entra ID.

<figure><img src="../.gitbook/assets/Gerenciamento de grupos.png" alt=""><figcaption><p>Tela inicial do cadastro de grupos</p></figcaption></figure>



### Importação dos relatórios

Um passo crucial para que o portal funcione é a importação dos relatórios que serão acessados.

Para acessar essa tela, [clique aqui](https://admin.powerembedded.com.br/Reports).

#### Opções de importação

Existem três tipos de importação de relatórios:

1. **Relatório do Power BI**: Esta opção permite importar relatórios que já existem no Power BI.
2. **Relatório da Web**: É possível importar relatórios de diversas fontes online, como Google Data Studio, documentos no OneDrive, Tableau, etc, além de relatórios presentes nos Workspaces do Power BI.
3. **Arquivo do Power BI**: Com esta funcionalidade, você pode publicar arquivos PBIX diretamente no Power BI sem precisar utilizar o Power BI Desktop.



**Relatório do Power BI**

Nesta opção, você pode visualizar os workspaces em que o Power Embedded tem administração e importar esses relatórios.

<figure><img src="../.gitbook/assets/selecionar-workspace.png" alt=""><figcaption></figcaption></figure>

Ao selecionar o workspace, serão listados todos os relatórios atribuídos a ele. Você pode optar por importá-los manualmente um a um ou importar todos de uma vez.

<figure><img src="../.gitbook/assets/selecionar-relatorio2-1024x185.png" alt=""><figcaption></figcaption></figure>



**Relatório Web**

No Power Embedded, você pode incorporar relatórios da Web ou documentos armazenados no SharePoint, OneDrive, entre outros. Por exemplo, se você possui um dashboard no Google Data Studio e precisa visualizá-lo aqui, basta inserir o link e ele será automaticamente reconhecido como um relatório externo no portal.

![](../.gitbook/assets/report-web-2-e1719346288446.png)

Como alguns sites não permitem esse processo de incorporação direta, oferecemos a opção de “Abrir em uma nova aba externa” para facilitar essa integração.



**Arquivo do Power BI**

Também é possível  publicar os relatórios do Power BI que estão localmente em seus computadores para os workspaces no Power BI serviço, dando uma liberdade e autonomia maior para os usuários.

![](../.gitbook/assets/Arquivo-Power-BI.png)

Para saber mais sobre essa funcionalidade. [Acesse o link](https://powerembedded.com.br/publique-seus-relatorios-pelo-power-embedded/)



### Personalização do portal

Como o Power Embedded é um sistema white-label, totalmente personalizável, é nesta tela que você configura toda a personalização para uma experiência mais personalizada com a identidade visual da sua empresa.

{% hint style="info" %}
Para ver mais detalhes sobre essa tela, acesse a página Configurações
{% endhint %}



Na aba "Portal de visualização" você poderá definir as cores e imagens do portal de visualização.

<figure><img src="../.gitbook/assets/portal-de-visualizacao.png" alt=""><figcaption></figcaption></figure>



Na aba "Tela de login", você poderá definir as cores e imagens da tela de login do portal de visualização.

<figure><img src="../.gitbook/assets/Tela de login.png" alt=""><figcaption></figcaption></figure>



Você também poderá personalizar os métodos de autenticação suportados pela plataforma e configurar outras personalizações da tela de login

<figure><img src="../.gitbook/assets/Personalização do método de autenticação.png" alt=""><figcaption></figcaption></figure>

Caso você faça o bloqueio de algum método de autenticação, nenhum usuário conseguirá se autenticar utilizando esse método de login e ele não será mostrado na tela de login.

Se esse método de autenticação estiver ativado, ele será mostrado na tela de login, mas você poderá bloquear ao nível do usuário, para que esse usuário específico não consiga utilizar esse método de autenticação.

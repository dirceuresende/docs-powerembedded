# Importação automática de relatórios criados pelo portal de visualização

### 1. Introdução

No Power Embedded, é possível criar e editar relatórios diretamente pelo navegador, ao acessar um relatório já existente, entregando uma experiência de Self-service BI excelente para os usuários.

<figure><img src="../../../.gitbook/assets/image (376).png" alt=""><figcaption></figcaption></figure>

Para que o usuário tenha acesso ao menu "Modo" e consiga Editar ou Criar novos relatórios pelo portal de relatórios, é necessário que o usuário ou algum grupo que esse usuário esteja e tenha acesso à esse relatório, tenha as permissões de **Criar relatórios** ou **Editar relatórios.**

<figure><img src="../../../.gitbook/assets/image (377).png" alt=""><figcaption></figcaption></figure>

Para uma melhor governança sobre a edição e criação de relatórios, você pode receber notificações, escolher quais usuários serão notificados e, além disso, habilitar a importação automática dos relatórios com opções para automatizar os acessos.



### 2. Como configurar a importação automática de relatórios

Em **Configurações > Modo de Edição e Criação**, é possível visualizar os campos, como mostrado na imagem abaixo.

<div align="left"><figure><img src="../../../.gitbook/assets/image (371).png" alt=""><figcaption></figcaption></figure></div>

**Enviar notificações quando um relatório for criado ou alterado?**\
Se você habilitar esta opção, todos os relatórios que forem criados ou modificados serão notificados por e-mail.

**Quais eventos notificar?**\
Conforme mencionado acima, é possível selecionar quais ações deseja ser notificado, podendo escolher entre criar ou somente em caso de alteração, ou ambos.

**Quais perfis de usuários deverão ser notificados?**\
Para direcionar melhor as informações, também é possível escolher quais perfis serão notificados, podendo escolher todos os três, se desejar. Essa notificação é enviada tanto no email, quanto no próprio portal de administração.



### 3. Importar relatórios automaticamente

Com essa opção ativada, se um usuário criar ou alterar um relatório e salvar uma cópia, a cópia será importada automaticamente para o portal. Por padrão, essa cópia é salva no Workspace do relatório original e, sem essa permissão habilitada, seria necessário fazer a importação manualmente. Nesse caso, uma notificação será enviada no e-mail e no portal informando sobre relatórios pendentes.

Nesta tela, você consegue ter uma governança para analisar e verificar o que o usuário criou ou editou, podendo importar ou rejeitar esses relatórios. Além disso, nessa mesma permissão, existem outras funcionalidades relacionadas.

<figure><img src="../../../.gitbook/assets/image (372).png" alt=""><figcaption></figcaption></figure>

Nesta habilitação, existem três possibilidades:

* **Apenas importar o relatório:** O relatório será importado sem nenhuma permissão e será necessário atribuir quais usuários irão visualizar.
* **Copiar permissões do relatório original:** As mesmas permissões que o relatório origem tem, essa cópia herda.
* **Importar e dar permissão a quem criou:** O relatório é importado automaticamente com o acesso somente de quem criou.

&#x20;

**Importar relatório para a mesma pasta do relatório original?** Caso esta opção esteja habilitada, o relatório será automaticamente importado para a mesma pasta do relatório original.

<div align="left"><figure><img src="../../../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure></div>



### 4. Notificações da importação do relatório

Quando o administrador do portal receber uma notificação no email, ele será redirecionado para uma tela de importação e análise do relatório, como mostrado na imagem abaixo.

<figure><img src="../../../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>

O administrador também terá acesso a essas notificações diretamente na tela inicial do portal de administração.

<figure><img src="../../../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

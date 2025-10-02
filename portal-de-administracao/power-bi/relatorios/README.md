---
description: Importe e gerencie relatórios, permissões e RLS no Power Embedded
---

# Relatórios

{% embed url="https://www.youtube.com/watch?v=cf5Y56fbztk" %}

Nesta tela é onde você poderá importar os relatórios, configurar segurança ao nível de linha (RLS), permissões de relatórios e muito mais.

Após a importação dos relatórios, é necessário editar o relatório e configurar os acessos.

<figure><img src="../../../.gitbook/assets/Screenshot_65.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Após a importação, os relatórios estarão disponíveis na aba de relatórios, mas inicialmente nem mesmo os administradores terão acesso ao relatório.

Você deve editar o relatório e liberar acesso para o usuário ou grupo.

Todas as permissões em relatórios devem ser liberadas explicitamente, até para gerar auditoria desse evento de liberação de permissão.
{% endhint %}



### **Filtros**

Pensando em praticidade na gestão das permissões de relatórios, na mesma tela você pode aplicar filtros para encontrar facilmente o relatório específico ao qual deseja aplicar as permissões necessárias.

<figure><img src="../../../.gitbook/assets/Screenshot_64.png" alt=""><figcaption></figcaption></figure>

### Botões de ações

Ao clicar em “Ações”, você terá acesso às funcionalidades para realizar essas configurações.

<figure><img src="../../../.gitbook/assets/Screenshot_açoes.png" alt=""><figcaption></figcaption></figure>

* **Visualizar:** Caso seu usuário tenha acesso ao relatório, você será redirecionado para o portal de visualização e abrirá esse relatório.
* **Editar:** Permite configurar várias propriedades e permissão do relatório.
* **Desabilitar:** Desativa temporariamente o relatório para que ele não fique visível para os usuários.
* **Assinaturas de Relatórios:** Permite que usuários autorizados configurem o envio automático de relatórios por e-mail com uma programação pré-definida.
* **Comentários:** Permite os usuários colaborarem diretamente nos relatórios, compartilhando observações, ideias ou questionamentos.
* **Baixar arquivo PBIX:** Permite baixar o arquivo do Power BI para o seu computador.
* **Agendar atualização:** Configurar atualizações agendadas dos conjuntos de dados diretamente pelo Power Embedded, deixa o processo não apenas mais simples, mas também muito mais flexível.
* **Vincular para todos os usuários**: Permite atribuir o relatório a todos os usuários cadastrados.
* **Desvincular para todos os usuários:** Remove o acesso do relatório para todos os usuários.
* **Auditoria de Entidades:** Lista as alterações realizadas nesse relatório.
* **Auditoria de Relatórios:** Lista todas as vezes que o relatório foi acessado no portal de relatórios.



### **Ações em massa**

Ao selecionar todos os relatórios através da caixa de seleção ao lado do nome, um botão de edição é exibido.

<figure><img src="../../../.gitbook/assets/Screenshot_60.png" alt=""><figcaption></figcaption></figure>

Isso permite atribuir um responsável para todos os relatórios e definir algumas permissões em massa para editar todos os relatórios selecionados de uma vez.

<figure><img src="../../../.gitbook/assets/Screenshot_63.png" alt=""><figcaption></figcaption></figure>

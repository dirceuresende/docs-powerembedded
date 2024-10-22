# Atribuir um workspace à uma capacidade

Para associar um workspace a uma capacidade contratada, [acesse o Power BI serviço](https://app.powerbi.com/).

Acesse o workspace que você quer alterar a capacidade e clique no botão **Configurações de Workspace.**

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>



Na tela que foi aberta, clique na opção **Informações da Licença** e depois clique no botão **Editar**

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>



Na lista de capacidades, escolha a sua capacidade contratada e depois clique no botão **Aplicar.**

<figure><img src="../../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

Após concluir o processo, é importante acessar a página de [**Workspaces**](https://admin.powerembedded.com.br/Workspaces) e clicar no botão **Recarregar** para confirmar que o workspace agora está associado à capacidade correta.&#x20;

Para que a otimização de custos seja aplicada corretamente, o nome da capacidade deve aparecer no campo de capacidade do Workspace, conforme mostrado na imagem abaixo.

<figure><img src="../../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
**ATENÇÃO:** Embora não seja muito comum, essas trocas de capacidade durante o horário comercial podem causar indisponibilidade em relatórios daquele workspace, pois podem acontecer casos em que alguns modelos ficam em estado bloqueado, necessitando um processo de atualização do conjunto de dados para desbloquear, o que pode demorar bastante tempo, dependendo do modelo de dados.

Além disso, tome cuidado se estiver alterando a capacidade para uma MENOR que a anterior, ou se estiver migrando de uma capacidade PRO ou PPU para uma capacidade dedicada (Fabric, Embedded ou Premium), pois pode haver perda de performance.
{% endhint %}




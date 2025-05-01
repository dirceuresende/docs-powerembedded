# A capacidade não está ligando quando um usuário acessa um relatório

### Introdução

O recurso da otimização de custos facilita o gerenciamento da capacidade do Microsoft Fabric ou Power BI Embedded de forma eficiente.

Esse recurso visa reduzir custos e ajustar o tamanho da capacidade para atender a picos de demanda, proporcionando uma administração mais eficaz, especialmente em modelos de cobrança baseados no uso.

{% hint style="info" %}
Se você está utilizando o período de avaliação do Fabric, você não conseguirá iniciar ou pausar a capacidade, pois é um recurso interno que você não tem controle.

Esse artigo só se aplica se você já contratou sua capacidade dedicada no portal do Azure.
{% endhint %}



### Como funciona a otimização de capacidade

<figure><img src="../../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

*   Quando essa otimização está ativada, somente usuários com permissões de nível de usuário ou grupo poderão visualizar um relatório se a capacidade estiver desligada. Se a capacidade estiver desligada e o usuário tiver permissão para reativá-la, o sistema irá mostrar o pop-up abaixo e a capacidade será ligada por demanda e o relatório será carregado automaticamente.\


    <figure><img src="../../.gitbook/assets/image (342).png" alt=""><figcaption></figcaption></figure>
*   Se um usuário sem a permissão de ativar a capacidade automaticamente tentar acessar um relatório enquanto a capacidade estiver desligada, ele não conseguirá visualizar o relatório.\


    <figure><img src="../../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>
* Você pode definir o período de minutos durante o qual sua capacidade pode permanecer inativa (ou seja, sem relatórios abertos). Quando o sistema detecta que nenhum relatório foi acessado durante esse período, a capacidade é automaticamente pausada.
* Durante o período em que a capacidade está pausada, você não será cobrado. Embora a reativação da capacidade seja rápida e quase imperceptível, alguns usuários podem achar o processo inconveniente. Para minimizar esse impacto, você pode agendar a reativação da capacidade.



Caso o usuário esteja tentando acessar o relatório quando a capacidade está desligada e não está sendo ligado automaticamente, você pode verificar os passos para identificar qual a configuração que não foi feita corretamente.



### 1. Verifique se as permissões foram atribuídas no Azure

{% hint style="info" %}
Acesse a página [Permissões no Azure](../../portal-de-administracao/power-bi/capacidades/permissoes-no-azure.md) para verificar como atribuir as permissões corretamente e o Power Embedded conseguir controlar a capacidade.
{% endhint %}



### 2. Verifique se a capacidade foi importada para o Power Embedded

Acesse a [página de Capacidades](https://admin.powerembedded.com.br/Capacities) e verifique se a capacidade contratada aparece na lista.

Caso não esteja, clique no botão **Recarregar** para atualizar a lista de capacidade&#x73;**.**

<figure><img src="../../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>



### 3. Verifique se a capacidade está configurada corretamente

Caso você veja a mensagem "Não configurado" ao lado da capacidade, quer dizer que a capacidade precisa ser configurada para funcionar no Power Embedded.

<figure><img src="../../.gitbook/assets/image (346).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Precisa de ajuda? Acesse a página [Configurar a capacidade no Power Embedded](../../portal-de-administracao/power-bi/capacidades/configurar-a-capacidade-no-power-embedded.md).
{% endhint %}



### 4. Verifique se o workspace está associado à capacidade no Power BI serviço

Para associar um workspace a uma capacidade contratada, [acesse o Power BI serviço](https://app.powerbi.com/).

Acesse o workspace que você quer alterar a capacidade e clique no botão **Configurações de Workspace.**

<figure><img src="https://docs.powerembedded.com.br/~gitbook/image?url=https%3A%2F%2F2938845060-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Ft2gQSHbraGsYbDGTmWAa%252Fuploads%252F7zIwdNTPrCDIwsccW3qJ%252Fimage.png%3Falt%3Dmedia%26token%3Decb19a94-af0f-4bdc-a8a5-513ba8e66c92&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=93b3d51f&#x26;sv=1" alt=""><figcaption></figcaption></figure>

Na tela que foi aberta, clique na opção **Informações da Licença** e depois clique no botão **Editar**

<figure><img src="https://docs.powerembedded.com.br/~gitbook/image?url=https%3A%2F%2F2938845060-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Ft2gQSHbraGsYbDGTmWAa%252Fuploads%252FOxbJxNg8FO0B5PIXdoQR%252Fimage.png%3Falt%3Dmedia%26token%3D626346e7-092d-491b-a80c-9da767b5baba&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=1274ee31&#x26;sv=1" alt=""><figcaption></figcaption></figure>

Na lista de capacidades, escolha a sua capacidade contratada e depois clique no botão **Aplicar.**

<figure><img src="https://docs.powerembedded.com.br/~gitbook/image?url=https%3A%2F%2F2938845060-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Ft2gQSHbraGsYbDGTmWAa%252Fuploads%252FjOjfaER1bIG0a2eQ0s82%252Fimage.png%3Falt%3Dmedia%26token%3D5d3ad3ab-5953-499c-a53e-2e40997f5400&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=30d59f2e&#x26;sv=1" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
**ATENÇÃO:** Embora não seja muito comum, essas trocas de capacidade durante o horário comercial podem causar indisponibilidade em relatórios daquele workspace, pois podem acontecer casos em que alguns modelos ficam em estado bloqueado, necessitando um processo de atualização do conjunto de dados para desbloquear, o que pode demorar bastante tempo, dependendo do modelo de dados.

Além disso, tome cuidado se estiver alterando a capacidade para uma MENOR que a anterior, ou se estiver migrando de uma capacidade PRO ou PPU para uma capacidade dedicada (Fabric, Embedded ou Premium), pois pode haver perda de performance.
{% endhint %}



### 5. Verifique se o workspace está associado à capacidade no Power Embedded

Após concluir o processo anterior, é importante acessar a página de [**Workspaces**](https://admin.powerembedded.com.br/Workspaces) e clicar no botão **Recarregar** para confirmar que o workspace agora está associado à capacidade correta.

Para que a otimização de custos seja aplicada corretamente, o nome da capacidade deve aparecer no campo de capacidade do Workspace, conforme mostrado na imagem abaixo.

<figure><img src="https://docs.powerembedded.com.br/~gitbook/image?url=https%3A%2F%2F2938845060-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Ft2gQSHbraGsYbDGTmWAa%252Fuploads%252FNSlcczP2LM5K5K3D2IUv%252Fimage.png%3Falt%3Dmedia%26token%3D0473ae1a-40c5-4087-a41c-5700c1011c4a&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=70df7e8&#x26;sv=1" alt=""><figcaption></figcaption></figure>



### 6. Verifique se a otimização de custos da capacidade está ligada

Após realizar todos os passos anteriores, clique no botão **Ações** > **Editar.**

<figure><img src="../../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure>

Ao clicar no botão de ações e selecionar “Editar”, você poderá definir as configurações de otimização de custos no portal.

Você precisa marcar o toggle "Ativar otimização de custos (Pausar e iniciar automaticamente)", selecionar o tempo de inatividade para pausar o recurso e salvar as alterações.

<figure><img src="../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>



### 7. Verifique se o usuário possui permissão de ligar a capacidade (ou está em um grupo com essa permissão)

É importante verifique se o usuário que está tentando acessar o relatório possui permissão para ligar uma capacidade desligada.

Para fazer isso, acesse a [página de Usuários](https://admin.powerembedded.com.br/Users), clique em **Ações** > **Editar** e olhe a aba **Permissões:**

<figure><img src="../../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

Verifique os grupos que esse usuário está e acesse a [página de Grupos](https://admin.powerembedded.com.br/Groups) para verificar se algum dos grupos tem essa permissão de ligar a capacidade e também tem acesso à esse relatório.

{% hint style="warning" %}
As permissões concedidas para o usuário são aplicadas em TODOS os relatórios que esse usuário tenha acesso. Se você precisa limitar essas permissões para relatórios específicos, libere essa permissão utilizando Grupos.
{% endhint %}



### 8. Verifique se a permissão global de bloquear ligar a capacidade NÃO está marcada

Acesse a página de "**Configurações"**, navegue pela aba "**Parâmetros"** e expanda a seção "**Permissões Globais**".

Verifique se a permissão "**Não pode ligar capacidade de relatório**" NÃO está marcada.

<figure><img src="../../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>



Após finalizar os passos acima, a capacidade já estará configurada e deverá ligar automaticamente quando estiver desligada e um usuário, com permissão de ligar a capacidade, tentar acessar o relatório.

# Otimização de custos

### Configurando a otimização manual

Ao ter completado todas as etapas anteriores, ao clicar em ‘recarregar’, serão listadas todas as capacidades criadas e quais o PowerEmbedded-App tem permissão.

Após isso, um botão será exibido, permitindo ligar e desligar manualmente. Nessa mesma tela, já é possível visualizar algumas informações importantes da capacidade.

<figure><img src="../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>



### Configurando a otimização de custo por demanda

Ao clicar no botão de ações e selecionar “Editar”, você poderá definir as configurações de otimização de custos no portal.

**Ativar otimização de custos (Pausar e iniciar automaticamente):**

* Quando essa otimização está ativada, somente usuários com permissões de nível de usuário ou grupo poderão visualizar um relatório se a capacidade estiver desligada. Se a capacidade estiver desligada e o usuário tiver permissão para reativá-la, ele conseguirá acessar o relatório automaticamente.
* Se um usuário sem a permissão de ativar a capacidade automaticamente tentar acessar um relatório enquanto a capacidade estiver desligada, ele não conseguirá visualizar o relatório.
* Você pode definir o período de minutos durante o qual sua capacidade pode permanecer inativa (ou seja, sem relatórios abertos). Quando o sistema detecta que nenhum relatório foi acessado durante esse período, a capacidade é automaticamente pausada.
* Durante o período em que a capacidade está pausada, você não será cobrado. Embora a reativação da capacidade seja rápida e quase imperceptível, alguns usuários podem achar o processo inconveniente. Para minimizar esse impacto, você pode agendar a reativação da capacidade.

<figure><img src="../../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>



### Configurando a otimização de custos por horário

Na tela de "Otimização de custos", você encontrará a opção de “Definir horário para otimização de custos”.

<figure><img src="../../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

Nessa aba, você pode programar os horários e dias da semana em que sua capacidade deve ligar e desligar ou até mesmo mudar de tamanho.

Ao clicar em “Adicionar”, dois campos serão exibidos: hora e ação. Aqui você pode programar os horários para ligar e desligar o recurso.

{% hint style="info" %}
Utilize a opção “Copiar para” para aplicar a mesma configuração para outros dias da semana e economizar seu tempo.
{% endhint %}

{% hint style="warning" %}
**Atenção:** Durante o intervalo definido, a capacidade ficará sempre ligada, independente se os usuários estão acessando os relatórios ou não.

Fora desse horário, a capacidade funcionará com base na demanda. Por exemplo, se você definiu que a capacidade liga às 08:00 e desliga às 17:00, ela permanecerá ligada durante esse período. Antes das 08:00 e após às 17:00, a capacidade funcionará com base na demanda.&#x20;

Se algum usuário tentar acessar o relatório fora do horário programado e ele tiver a permissão ativa no cadastro de usuário ou grupo, a capacidade será ligada, e quando atingir o tempo de inatividade definido por você, ela será desligada.
{% endhint %}


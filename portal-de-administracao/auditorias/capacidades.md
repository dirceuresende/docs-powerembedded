# Capacidades

{% embed url="https://www.youtube.com/watch?v=qQbat3QZ0l4" %}

Toda vez que o sistema liga ou desliga a capacidade, seja por botão, agendamento, demanda ou por inatividade, esse histórico da atividade é registrado.

O registro inclui informações sobre a data e hora do evento (ligar/desligar), a capacidade afetada e o usuário que realizou a ação.

Esse recurso de auditoria tem como diferencial mapear os usuários que estão sempre acessando o sistema fora do horário pré-estabelecido e, consequentemente, aumentando o custo da capacidade.

<figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Para saber mais sobre como configurar a capacidade, acesse a página [Capacidades](capacidades.md).
{% endhint %}



### Tipos de evento (ação)

* **Iniciado Manualmente / Pausando Manualmente**\
  Essa ação ocorre quando você clica no botão de desligar/ligar. \
  \
  A informação que é gerada traz qual foi o usuário que fez ação(clicar no botão), a data/hora que esse evento ocorreu.\

* **Iniciado por Demanda / Suspenso por Inatividade**\
  É quando a capacidade está desligada e um usuário acessa um relatório e com isso a capacidade liga automaticamente devido a essa ação do usuário.\
  \
  A informação que é gerada traz qual foi o usuário que fez essa ação (acessar o sistema após horário) e a data/hora que esse evento ocorreu. Quando o sistema desliga automaticamente devido à inatividade, é gerado o evento “Pausado por inatividade”.\

* **Iniciado Por Agendamento / Pausado por Agendamento**\
  Essa ação ocorre quando é criado um agendamento para ligar ou desligar a capacidade automaticamente.\
  \
  Exemplo: Se a capacidade está agendada para ligar às 7h da manhã, o evento vai ser descrito como “Iniciado por Agendamento” e se o agendamento está configurado para desligar às 20h, o evento gerado será “Pausado por Agendamento”\
  \
  **Observação:** Se às 20h ainda houver usuários acessando o sistema, ele não será desligado nesse horário. Em vez disso, ele começará a verificar a inatividade a partir do horário definido (configuração da capacidade). Se ocorrer a suspensão da capacidade devido à inatividade, o evento será registrado como “Pausado por Inatividade”.



### Exportar

Os registros da auditoria de capacidade podem ser exportados como arquivos CSV ou Excel para uma análise mais detalhada.

<figure><img src="../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>



### Filtrar

É possível aplicar filtros de usuário, capacidades, ações e data/hora para obter informações sobre quem está acessando fora do horário comercial, por exemplo, entre outras especificações.

<figure><img src="../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

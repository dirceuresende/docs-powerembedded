# Capacidades

{% embed url="https://www.youtube.com/watch?v=qQbat3QZ0l4" %}

Essa funcionalidade do portal facilita o gerenciamento da capacidade do Microsoft Fabric ou Power BI Embedded de forma eficiente.&#x20;

Ela visa reduzir custos e ajustar o tamanho da capacidade para atender a picos de demanda, proporcionando uma administração mais eficaz, especialmente em modelos de cobrança baseados no uso.



### Tipos de gerenciamento da capacidade

Para gerenciar as capacidades, seja o Microsoft Fabric ou Power BI Embedded via portal, há três maneiras:

**Manual:** Ao acessar o menu de capacidades e ter concluído todas as configurações prévias necessárias, a funcionalidade será exibida, juntamente com um botão para ligar e desligar. Aqui, o administrador pode ficar responsável pela gestão do recurso.

**Por demanda:** Aqui, o Power Embedded ativa a capacidade automaticamente quando um usuário tenta acessar um relatório, isso acontece somente se o usuário tiver permissão ao nível de usuário ou grupo. Quando atingir o tempo de inatividade que você definir, ela é pausada para evitar cobranças.

**Por Agendamento:** Neste método, você pode planejar quando a capacidade deve ser ligada e desligada e até mesmo mudar a capacidade por agendamento. Isso oferece um controle mais previsível sobre os recursos, permitindo ajustar conforme a demanda ou horários específicos de uso.

**Mudar a capacidade:** Nessa ação, você pode agendar um horário para que a sua capacidade mude de SKU, ou seja, em horário de pico muito alto de consumo você pode aumentar esse recurso e quando diminuir esse consumo pode reduzir para uma capacidade inferior.

{% hint style="warning" %}
É importante ressaltar que quando uma capacidade está desligada, o usuário não consegue visualizar o relatório e o conjunto de dados não é atualizado.&#x20;

É crucial planejar o horário de uso para evitar possíveis falhas no ambiente.
{% endhint %}



### Funcionalidades do menu

Logo abaixo uma descrição das funcionalidades do menu.

<figure><img src="../../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

**Filtrar**: Permite buscar por nome de capacidade, útil quando há várias capacidades listadas.

**Recarregar:** Utilizado após configurar no Portal do Azure para atualizar os metadados da capacidade e exibir o botão de controle.

**Exportar:** Permite exportar dados para Excel ou CSV, incluindo informações da tabela de capacidade.

**Ligar/Desligar**: Botão para iniciar ou pausar a capacidade manualmente.



Ao clicar no botão de **ações**, é exibido uma lista de funcionalidades.

* **Editar:** Usado para configurações iniciais e otimização de custos.
* **Remover:** Exclui a capacidade da gestão do Power Embedded.
* **Auditoria de Entidade:** Visão das atividades realizadas pelos usuários que acessam o portal de administração. Saiba mais em [Auditoria de Entidades](../../auditorias/entidades-alteracoes.md).
* **Auditoria de Capacidade:** Detalha ações ocorridas com a capacidade ao longo do tempo. Saiba mais em [Auditoria de Capacidade](../../auditorias/capacidades.md).

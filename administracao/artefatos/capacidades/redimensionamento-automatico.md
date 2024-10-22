# Redimensionamento automático

Você já se deparou com a necessidade de ajustar a capacidade no Azure durante períodos de alta demanda por relatórios?&#x20;

Com o Power Embedded, agora você pode fazer isso de forma simples e rápida diretamente pelo portal.

A nova funcionalidade permite alterar o SKU da capacidade com base em um agendamento, tornando o processo muito mais eficiente.



### Como funciona

Anteriormente, era possível apenas ligar e desligar o recurso pelo portal. Agora, com a nova funcionalidade, é possível gerenciar o SKU da capacidade, ou seja, fazer upscale e downscale em horários específicos da semana ou até mesmo em dias específicos.

Para usar essa funcionalidade, vá até _**Artefatos > Capacidades > Otimização de Custos**_ e habilite a permissão **Definir horário para otimização de custos**. Isso permitirá que você trabalhe com agendamentos.

Após habilitar um dia da semana, você verá os campos _Hora_ e _Ação_. O campo _Hora_ define quando a ação será realizada, e o campo _Ação_ permite escolher entre ligar, desligar ou mudar a capacidade.&#x20;

Anteriormente, as únicas opções disponíveis eram ligar e desligar, mas agora você também pode optar por mudar a capacidade, e é sobre isso que vamos detalhar.

<figure><img src="../../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

Ao selecionar a ação de “mudar capacidade”, será exibido um campo onde você pode escolher o nível de capacidade desejado, com informações sobre tamanho, processamento e custo. Quando você contrata um recurso, define um tamanho no Azure.&#x20;

Com a nova funcionalidade, se seu modelo for pago pelo uso e você precisar ajustar a capacidade em um determinado período, basta definir uma ação para mudar a capacidade. Isso ocorrerá automaticamente sem que você precise acessar o Azure.&#x20;

Além disso, você pode definir um horário ou dia específico para que a capacidade retorne ao valor inicial.



### Exemplo prático de configuração

Após configurar tudo no Azure para gerenciar o recurso diretamente no portal, siga estas etapas para otimizar a capacidade:

1. Acesse a tela de [Gerenciamento de capacidades](https://admin.powerembedded.com.br/Capacities)
2. Verifique se a capacidade que você quer controlar está sendo mostrada na lista de capacidades. Caso não esteja, clique no botão _**Recarregar**_
3. Caso apareça a mensagem “Não configurado” ao lado da capacidade que você quer controlar, você precisará configurar a capacidade corretamente no Power Embedded e liberar as permissões necessárias para o sistema poder gerenciar a capacidade. Veja mais em [Permissões do Azure](permissoes-no-azure.md).
4. Clique no botão _**Ações**_ ao lado da capacidade que você quer alterar e clique na opção _**Editar**_
5. Na tela de edição de capacidades, clique na aba _**Otimização de Custo**_
6. Ative a opção _**Otimização de Custo**_ e selecione _**Definir horário para otimização de custos**_** para iniciar a configuração.** Isso será permitir a alterações agendadas da capacidade.



No exemplo abaixo, o SKU inicialmente contratado no Azure foi um F2.

<figure><img src="../../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

Observa-se que a capacidade é ativada às 08:00 da manhã. Durante o período das 12:00, quando ocorre um processo de atualização intensivo e a atividade dos usuários é alta, optamos por aumentar a capacidade para um nível superior, como de F2 para F4. Conforme as métricas analisadas no Fabric Capacity Metrics, uma F4 é adequada para lidar com picos de demanda no nosso cenário.

Às 16:00, quando o consumo de capacidade diminui, realizamos um downgrade para um nível menor.&#x20;

Por fim, às 18:00, a capacidade é desligada e passa a ser ativada por demanda, caso você habilite a permissão para usuários ou grupos.&#x20;

Esse é um exemplo prático da usabilidade dessa nova funcionalidade, importante ressaltar que fica disponível o copiar para onde é possível copiar essas informações para outros dias da semana.



### Regras de funcionamento

1. A funcionalidade só está disponível se o recurso estiver contratado. A avaliação do Fabric não permite gerenciar a capacidade.
2. A capacidade precisa estar configurada para aparecer no Power Embedded. Para entender melhor como realizar essa configuração, acesse [Configuração da capacidade](configurar-a-capacidade-no-power-embedded.md).
3. Ao alterar o tamanho da capacidade, ela só retornará ao valor inicial se você criar alguma ação para trocar a capacidade novamente ou alterar manualmente pelo portal do Azure.
4. Você não precisa ligar a capacidade para mudar a capacidade, ou seja, é possível mudar a capacidade mesmo estando pausada e isso não muda a cobrança enquanto ela está pausada.
5. Esse controle de ligar/desligar a capacidade para reduzir os custos só faz sentido para o modelo de pagamento **Pago pelo uso**. Pausar uma capacidade que está no modo **Instância reservada** não irá reduzir em nada o seu custo mensal, fixo (só varia com o dólar) e só vai gerar indisponibilidade no acesso aos relatórios.
6. Caso sua capacidade esteja no modo **Instância reservada** e você altere a capacidade para um SKU maior que o atual, você continuará sendo cobrado pela instância reservada normalmente, além do tempo que utilizou a capacidade maior que a reserva contratada.\
   \
   Ex: Você tem uma reserva de F2 e durante 8h, você alterou para a F8. Você será cobrado normalmente pela sua instância reservada F2, e a Microsoft irá cobrar um valor equivalente a um F6 (F8 – F2), no modo **Pago pelo uso**, por um período de 8h.

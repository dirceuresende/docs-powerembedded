# Pausar a capacidade quando não estiver utilizando reduz o custo?

Sim, **pausar a capacidade do Microsoft Fabric e do Power BI Embedded reduz o custo,** que são cobradas por hora de uso.

#### ✅ Quando a pausa reduz custo:

* **Fabric Capacity (SKU F)**: cobradas por hora de provisionamento. Pausar a capacidade suspende a cobrança enquanto ela estiver parada.
* **Power BI Embedded (SKU A1 a A6)**: também são cobradas por hora de execução. Pausar a capacidade (via Azure Portal, PowerShell ou REST API) suspende a cobrança.

\
Entretanto, no caso do Fabric, essa regra nem sempre irá refletir em uma redução de custos.



#### ⚠️ **Microsoft Fabric usa smoothing e bursting**, o que muda a lógica tradicional de "pausar = economizar":

**🔹 Smoothing:**

* O Fabric utiliza o conceito de "pré-alocação proporcional de uso futuro".
* Quando você executa tarefas pesadas, como refresh de Lakehouse, notebooks ou pipelines, o sistema prevê e **amortiza o custo ao longo das próximas horas** (ex: 6h a 24h).
* Se você **pausa a capacidade antes do smoothing completar**, o sistema entende que você interrompeu a "janela de pagamento" e pode:
  * Cobrar imediatamente o uso restante, que pode **até dobrar o custo estimado** se estiver considerando apenas a quantidade de horas ligadas, sem considerar o smoothing.
  * Aplicar **bursting credit fees**.
  * Reduzir o throughput quando reativar.

\
**🔹 Bursting:**

* É o direito de consumir além da sua capacidade alocada, por picos temporários.
* Você só consegue burstar se tiver **histórico contínuo de capacidade ligada**.
* Ao pausar com frequência, o sistema **limita ou nega bursting**, afetando performance.

***

#### ✅ Quando faz sentido pausar o **Microsoft Fabric**:

* Fora de **horários fixos de execução de pipelines** (ex: 00:00–06:00).
* Se você tem controle sobre o agendamento de tarefas e **nenhum smoothing em aberto**.
* Ideal com **monitoramento**: antes de pausar, verifique o **smoothing buffer ativo**.

***

#### ✅ Quando faz sentido pausar o **Power BI Embedded**:

* Sempre que não estiver com relatórios embutidos em uso — não há smoothing, só cobrança por uptime da capacidade.

***

#### ✅ Boas práticas:

1. **Evite pausar imediatamente após tarefas pesadas** no Fabric.
2. Use um **script para verificar o status de smoothing ativo**.
3. Planeje **janelas fixas de disponibilidade da capacidade** com agendamentos alinhados.
4. Considere **escalar para uma SKU menor em vez de pausar**, se uso for contínuo, mas leve.
5. Em muitos cenários, faz mais sentido **ativar a reserva da instância** e deixar ligado 24x7 do que ficar pausando a capacidade para reduzir custos

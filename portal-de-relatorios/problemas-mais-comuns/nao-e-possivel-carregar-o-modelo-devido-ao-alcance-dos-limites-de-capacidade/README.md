# Não é possível carregar o modelo devido ao alcance dos limites de capacidade

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Esse erro ocorre quando a sua capacidade atingiu o limite de uso. Provavelmente algum relatório, pipeline ou dataflow consumiu muitos recursos e acabou derrubando o ambiente.

Para resolver rapidamente esse erro, de forma temporária, **reinicie a sua capacidade** pelo [portal do Azure](https://portal.azure.com/#browse/Microsoft.Fabric%2Fcapacities) ou na página de [Gerenciamento de Capacidades](https://admin.powerembedded.com.br/Capacities). Isso vai fazer com que o uso futuro do Fabric seja reiniciado e a capacidade volte a carregar os relatórios.

Agora você precisa analisar o relatório [Fabric Capacity Metrics](https://appsource.microsoft.com/en-us/product/power-bi/pbi_pcmm.microsoftpremiumfabricpreviewreport) para identificar o que consumiu tanta capacidade e decidir se chegou o momento de ter que aumentar a capacidade ou otimizar algum processo para que consuma menos recursos.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Abaixo, você tem a opção de reiniciar e alterar a capacidade de duas maneiras, pelo Azure ou diretamente pelo Power Embedded.



{% embed url="https://docs.powerembedded.com.br/portal-de-relatorios/problemas-mais-comuns/nao-e-possivel-carregar-o-modelo-devido-ao-alcance-dos-limites-de-capacidade/como-reiniciar-ou-alterar-a-capacidade-pelo-power-embedded" %}

{% embed url="https://docs.powerembedded.com.br/portal-de-relatorios/problemas-mais-comuns/nao-e-possivel-carregar-o-modelo-devido-ao-alcance-dos-limites-de-capacidade/como-reiniciar-ou-alterar-a-capacidade-pelo-azure" %}

Se precisar de ajuda para realizar essa análise, [agende uma reunião](https://powerembedded.com.br/reuniao-suporte) com o time de suporte.

{% hint style="info" %}
**Observação:** Clientes do Power Embedded têm acesso GRATUITO ao workshop do Rafael Mendonça sobre [análise de capacidade do Fabric](https://cursos.powertuning.com.br/course/microsoft-fabric-analise-de-capacidade).
{% endhint %}

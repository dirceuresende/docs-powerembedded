# Permissões no Azure

### Role de contribuidor

No portal do Azure, pesquise pelo capacidade contratado e abra o recurso.

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>



Para adicionar o usuário como contribuidor vá em **Access control (IAM) > Add > Add role assignment.**

<figure><img src="../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>



Nessa nova tela, clique na aba **Members**, depois **Priveleged admnistrator roles** e marque a permissão **Contributor.**

{% hint style="warning" %}
A permissão de **Contributor** na capacidade para o usuário do Power Embedded (PowerEmbedded-App) é necessária para permitir o sistema possa alterar o SKU (Tamanho) da capacidade, seja manualmente ou na Otimização de custos.

Se não for necessário que o Power Embedded possa alterar o SKU da capacidade, se limitando apenas à ligar/desligar a capacidade, você pode liberar a permissão de **Reader (Leitor)** ao invés de **Contributor**, que é menos permissiva. Essa permissão de Reader fica na aba **Job function roles**.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>



Na tela de membros clique em **Select members** para buscar pelo usuário PowerEmbedded-App e selecioná-lo.

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

Agora clique em **Review + assign** para finalizar esse processo.



### Capacity Administrator

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

Ainda na tela da capacidade contratada, vá em **Settings > Capacity administrators** e clique no botão **Add.**

Ao abrir a tela, pesquise por _**PowerEmbedded-App**_ e clique em **Select.**

Nesta aba, você pode adicionar as pessoas que terão permissão para atribuir um workspace à capacidade.



Para validar de fato essa alteração clique em **Save** para salvar a informação.

<div align="left">

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

</div>

Com essas configurações feitas agora podemos configurar Power Embedded.

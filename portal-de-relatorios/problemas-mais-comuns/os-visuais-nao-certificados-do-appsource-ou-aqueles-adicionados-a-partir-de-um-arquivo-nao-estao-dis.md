# Os visuais não certificados do AppSource ou aqueles adicionados a partir de um arquivo não estão dis

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

Esse erro ocorre quando você tenta utilizar um visual não certificado no Power BI e o administrador configurou o serviço para permitir apenas o uso de visuais certificados. Essa configuração é aplicada diretamente no portal de administração do Power BI Serviço.

### Como resolver ?

Para corrigir esse problema e permitir o uso de visuais não certificados, siga os passos abaixo:\


{% hint style="warning" %}
Para seu usuário conseguir realizar essa configuração ele precisa ter a função de Administrador do Fabric
{% endhint %}

Acesse o Portal de Administração do Power BI Serviço, [clique nesse link.](https://app.powerbi.com/admin-portal/tenantSettings?experience=power-bi)

No portal de administração, em configurações de locatário vá a barra de pesquisa a sua direita e busque por "Visuais do Power Bi"

Ao fazer essa busca, você vai ver o menu "Visuais do Power Bi" vá até a opção **"Adicionar e usar somente visuais certificados (bloquear os não certificados)".**

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Desabilite essa configuração, e clique em **aplicar.**

Após desabilitar, os visuais não certificados serão suportados novamente no Power BI, permitindo sua utilização sem restrições.

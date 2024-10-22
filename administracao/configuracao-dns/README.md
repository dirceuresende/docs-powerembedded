---
description: >-
  Aprenda como configurar a URL personalizada do portal, utilizando domínio
  interno ou próprio
---

# Configuração do DNS

O Power Embedded é uma plataforma SaaS no formato _white-label_, onde o sistema é totalmente personalizável para cada cliente, desde cores, imagens até a própria URL de acesso, que pode ser personalizada também.



### Criação dos registros no DNS

Para que você possa acessar o sistema utilizando uma URL personalizada, oferecemos 2 opções para nossos clientes:

1. Utilizar o seu próprio domínio. Ex: bi.suaempresa.com.br
2. Utilizar o domínio do Power Embedded. Ex: suaempresa.powerembedded.com.br



Caso você opte por utilizar o seu próprio domínio, você precisará adicionar os 2 registros no seu DNS (CNAME e TXT) para ser possível utilizar essa URL personalizada no Power Embedded:

| Tipo  | Nome     | Valor                                                            |
| ----- | -------- | ---------------------------------------------------------------- |
| CNAME | bi       | powerportal-client.azurewebsites.net                             |
| TXT   | asuid.bi | D1B15490F13A639D57FF7985A837F7E5242DD6F062BEEC8698E3CC36A6CBD693 |

O exemplo acima é para quando você está configurando o subdomínio bi.suaempresa.com.br



Caso você queira utilizar outro nome, como relatorios.minhaempresa.com.br, você irá utilizar o mesmos valores do campo "Valor", mas o valor do "Nome" será diferente:

* Para o registro CNAME, o valor seria "relatorios"
* Para o registro TXT, o valor seria "asuid.relatorios"

{% hint style="warning" %}
Após realizar as configurações indicadas, lembre-se de comunicar o time de suporte do Power Embedded para que eles realizem a liberação no sistema.

Utilize o site [DNSChecker](https://dnschecker.org/) para verificar se a criação dos registros no DNS já foi propagada.
{% endhint %}



### Configurar a nova URL no Power Embedded

Após as alterações realizadas no DNS e liberadas pelo time de suporte, agora você só precisa configurar no sistema essa nova URL.

Para fazer isso, acesse a página de Configurações e digite o sub-domínio personalizado

<figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>



### Como configurar em outras plataformas

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Cloudflare</strong></td><td>Aprenda a configurar</td><td></td><td><a href="cloudflare.md">cloudflare.md</a></td></tr></tbody></table>

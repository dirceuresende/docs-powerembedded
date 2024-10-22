# Empresas

{% embed url="https://www.youtube.com/watch?v=TDFan7WdbXM" %}

Visando oferecer um nível de personalização multinível para os clientes, o Power Embedded, dispõe de funcionalidades específicas para criar várias identidades visuais diferentes, conforme o usuário que está acessando o portal.

No portal, você tem a sua organização, onde é possível incluir várias empresas, conforme ilustrado na imagem abaixo:

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

Em cenários onde você deseja proporcionar uma experiência personalizada para seu cliente, departamento ou filial, é possível criar várias empresas e configurar desde o subdomínio até a personalização completa da identidade visual para cada empresa.

{% hint style="warning" %}
A associação do usuário com a empresa não tem influência nas permissões de acesso do usuário com o relatório, nem com o RLS ou permissões. Serve apenas para filtragens e para controlar a identidade visual do portal de acordo com a empresa do usuário.

Caso o usuário esteja em mais de uma empresa ou em nenhuma, a identidade visual será herdada das configurações gerais da organização.
{% endhint %}

{% hint style="info" %}
O Power Embedded também permite múltiplas organizações na mesma instalação, garantindo um nível ainda maior de personalização.
{% endhint %}



### Aba Empresa

Em configurações iniciais você preencha as informações abaixo:

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

A funcionalidade de “tipo de visualização padrão dos relatórios”, irá impactar diretamente na visualização do portal de relátórios, ou seja definindo qual vai ser o modo que ele irá visualizar os relatórios assim que ele logar.

**Observação:** Caso não deseje incorrer em custos adicionais com subdomínios, é possível simplesmente utilizar o subdomínio existente e personalizar apenas o portal de visualização. Quando o usuário acessar, será redirecionado para a empresa configurada.



### Portal de Visualização

Para personalizar a identidade visual da empresa basta acessar a página [Portal de visualização](../configuracoes/portal-de-visualizacao/).

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>



### Tela de login

Para personalizar a identidade visual da empresa, acesse a página [Tela de login](../configuracoes/tela-de-login/).

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>



### Emails

Existem diversas ações que acionam o envio de e-mails. Para garantir um nível maior de personalização na entrega dessas mensagens, é possível configurar uma conta SMTP da sua empresa.

Para saber mais, acesse a página [Emails](../configuracoes/emails.md).



### Usuários

Utilize essa aba para selecionar quais usuários estarão associados à empresa em questão.

Vale lembrar que essa associação não tem a ver com permissão e sim personalização visual e filtros.&#x20;

Se o usuário estiver associado a nenhuma ou mais de 1 empresa, a personalização da empresa não será aplicada, e será utilizada a identidade visual da organização.

<figure><img src="../../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>



### Relatórios

Permite associar o relatório a uma empresa. Essa associação serve apenas para filtros e facilitar a parte de permissão dos relatórios.

<figure><img src="../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>



### Existe custo adicional?

Não há custo adicional nem limite de empresas no portal.&#x20;

A cobrança adicional ocorre apenas se você desejar que cada empresa tenha um subdomínio personalizado.

O custo é de R$ 50 por mês para cada subdomínio personalizado.&#x20;

No entanto, não é obrigatório ter um subdomínio para cada empresa, exceto se você realmente gostaria que cada tenha empresa sua própria URL e tela de login personalizada.

Você pode utilizar o subdomínio existente na organização, criar várias empresas, personalizar com a identidade visual do seu cliente, que terá uma tela de login apenas, mas a personalização do portal de relatórios será aplicada mesmo assim.

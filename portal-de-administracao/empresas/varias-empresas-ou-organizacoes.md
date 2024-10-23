# Várias empresas ou organizações

Uma dúvida muito comum é a diferença entre criar várias empresas ou várias organizações para personalizar o portal de visualização.

Como vocês podem observar no desenho abaixo, você pode ter várias organizações no seu tenant. Em cada organização, você pode ter várias empresas.

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>



### Pontos em comum

As 2 opções atendem bem a essa necessidade de ter ambientes personalizados de acordo com seu cliente.

Tanto organização quanto empresa tem praticamente as mesmas personalizações disponíveis de cores e imagens para o portal de visualização e a tela de login.

Para criar URLs independentes para cada cliente/perfil também tem as mesmas opções de personalização e o mesmo custo de R$ 50,00/mês por sub-domínio adicional.



### Diferenças

Quanto você tem várias empresas na mesma organização, o cadastro de usuários, grupos e relatórios é o mesmo, e você pode definir quais empresas cada usuário vai fazer parte para personalizar a experiência do portal de relatórios.

Por ser apenas uma organização, algumas configurações são compartilhadas, pois não existem na empresa, como, por exemplo, a chave de API, personalização dos métodos de autenticação, integração com Google Analytics, etc.

Por outro lado, quando você tem várias organizações, os ambientes são totalmente isolados, ou seja, não compartilham nada entre as organizações: usuários, grupos, relatórios, parâmetros, tudo é isolado e se você precisa que o mesmo usuário exista em todas as organizações, você terá que criá-lo várias vezes (e ele será cobrado várias vezes).

Isso também pode ser um ponto positivo, por permitir ter chaves de API individuais para cada organização/cliente, além de outras configurações.



O Power Embedded tem 2 níveis de separação de personalizações e você pode utilizá-los e combiná-los conforme sua necessidade:

* Somente 1 organização
* Somente 1 organização e 1 empresa
* Somente 1 organização e várias empresas
* Várias organizações e nenhuma empresa
* Várias organizações e 1 empresa
* Várias organizações e várias empresas em cada



{% hint style="warning" %}
**IMPORTANTE:** A associação do usuário com a empresa não tem influência nas permissões de acesso do usuário com o relatório, nem com o RLS ou permissões. Serve apenas para filtragens e para controlar a identidade visual do portal de acordo com a empresa do usuário.

Caso o usuário esteja em mais de uma empresa ou em nenhuma, a identidade visual será herdada das configurações gerais da organização.
{% endhint %}


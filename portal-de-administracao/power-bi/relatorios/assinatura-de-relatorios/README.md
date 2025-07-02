# Assinatura de relatórios

A assinatura de relatório é um recurso que permite aos usuários com a permissão adequada configurar o envio automático de relatórios por e-mail com base em uma programação definida.&#x20;

Esse recurso é uma ferramenta poderosa para garantir que informações importantes sejam entregues de maneira consistente e pontual, e facilitando a análise de dados para usuários que gostam de receber as informações por e-mail sem precisar acessar o portal.

<figure><img src="../../../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>



### Gerenciamento de Assinatura de Relatórios

No menu de gerenciamento de assinaturas de relatórios, você pode visualizar quais relatórios possuem assinaturas ativas e acompanhar a frequência com que esses relatórios são enviados.&#x20;

Essa funcionalidade oferece uma visão detalhada das assinaturas existentes, facilitando o gerenciamento e a supervisão, e garantindo que você esteja sempre atualizado sobre as assinaturas criadas.

<figure><img src="../../../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

Além disso, nesse mesmo menu, ao clicar em **Ações**, você pode remover assinaturas de relatórios e editar as informações existentes.



### Como criar uma Assinaturas de Relatórios

Para criar uma assinatura de relatório pelo portal de relatórios, o usuário deve ter a permissão “Pode gerenciar assinaturas de email” ativada no seu perfil ou grupo.

Ao clicar em **Arquivo > Assinar Relatório**, será exibida uma tela onde o usuário pode configurar a assinatura do relatório. Nesta tela, é possível definir o nome da assinatura e preencher os campos do e-mail, incluindo o título que será exibido ao usuário e a mensagem no corpo do e-mail.

Além disso, você pode adicionar destinatários, permitindo a inclusão de múltiplos e-mails separados por vírgula (certifique-se de que os e-mails estejam cadastrados no portal e tenham acesso ao relatório).&#x20;

Também é possível escolher o formato do relatório, que pode ser PDF ou PowerPoint, e configurar os parâmetros de data para a assinatura, especificando a frequência e as datas de envio.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure></div>

Ao configurar sua assinatura de relatório, é necessário salvá-la e habilitar a regra para que ela funcione conforme o planejado. Para isso, marque o checkbox correspondente, que ficará azul quando ativado.&#x20;

Após concluir essas etapas, sua assinatura estará criada com sucesso.



**Pontos importantes da assinatura de relatório.**

* Todos os destinatários devem estar cadastrados no portal e ter acesso ao relatório.
* Ao clicar em salvar a assinatura não esqueça de habilitar.
* Se o relatório utilizar Row-Level Security (RLS), a configuração deve estar correta para garantir que os dados estejam adequadamente filtrados para cada destinatário.



### Suporte a Row-Level Security (RLS)

Se você utiliza a funcionalidade de assinatura de relatórios no Power Embedded e precisa garantir a segurança com as regras de RLS (Row-Level Security), então essa novidade é para você.

Agora o Power Embedded oferece uma solução robusta para isso. Esta funcionalidade, conhecida como _Data-Driven Subscription_, permite uma distribuição de relatórios que respeita as regras de segurança de dados de forma mais segura.



### Como funciona o RLS na Assinatura de Relatório

O sistema cria um relatório individualizado para cada usuário com base nas regras de RLS configuradas. Isso significa que cada relatório enviado por e-mail é especificamente filtrado para mostrar apenas os dados que o usuário está autorizado a ver, conforme definido pela RLS.

Com a Data-Driven Subscription, a segurança é garantida pela geração de arquivos para cada destinatário. Isso assegura que as regras de RLS são aplicadas de forma rigorosa, tanto no conteúdo do relatório quanto no acesso ao arquivo recebido por e-mail.



### Assinatura de relatório com RLS vs _Dynamic Subscription_

No Power BI Pro, essa funcionalidade análoga é chamada _Dynamic Subscription_.

Nessa abordagem, o administrador configura um filtro de dados para cada usuário, mas a segurança não é tão robusta quanto a do Power Embedded. Isso ocorre porque, embora o relatório enviado por e-mail seja filtrado conforme o filtro aplicado, os usuários ainda podem acessar o relatório diretamente no serviço do Power BI e visualizar todos os dados, dependendo das permissões concedidas.

No Power Embedded, o RLS aplicado na assinatura do relatório é o mesmo utilizado para filtrar os dados quando o usuário abre o relatório normalmente. O usuário não consegue ver os dados sem o RLS.

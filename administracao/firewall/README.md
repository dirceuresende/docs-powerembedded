---
description: Aprenda como controlar os acessos com o Firewall
---

# Firewall

O recurso de firewall é uma vantagem adicional oferecida pelo Power Embedded, que não está disponível no próprio Power BI.&#x20;

Essa funcionalidade permite bloquear o acesso ao portal de visualização de relatórios apenas para usuários que estejam utilizando determinados endereços de IP específicos, proporcionando maior controle e segurança aos dados.

{% embed url="https://www.youtube.com/watch?v=flT4N2CUwck" %}



### Como utilizar o Firewall

Para utilizar esse recurso, precisamos realizar duas etapas:

1. Habilitar a regra de firewall
2. Cadastrar regra de IP

Para que a regra de Firewall funcione corretamente, é necessário seguir as etapas listadas, pois uma complementa a outra.&#x20;

Não basta apenas cadastrar uma regra; é preciso habilitá-la no menu de configurações.



### Etapa 1: Habilitar regra de firewall

No portal de Administração, acesse a página de **Configurações**

<figure><img src="../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

Marque a opção **Habilitar regra de firewall** e depois clique em **Salvar.**

Ao realizar essa configuração, caso exista pelo menos 1 IP cadastrado na lista de bloqueios e o seu IP não esteja cadastrado nas regras, você não conseguirá acessar o portal de visualização.



### Etapa 2: Cadastrar regra de IP

No portal de administração, abra a página de [**Firewall**](https://admin.powerportal.cloud/Firewall) **> Regras de Firewall.**

Você pode clicar no botão **Adicionar meu endereço de IP** ou adicione manualmente em **Criar Regra:**

* **Adicionar meu endereço de IP:** Aqui, o portal traz automaticamente o seu endereço de IP atual. Com apenas um clique no botão, você pode cadastrar seu IP atual.
* **Criar Regra:** Ao selecionar esta opção, você preencherá o nome da regra e adicionará uma faixa de endereços IP de início e fim. Se desejar liberar apenas um único endereço IP, preencha ambos com o mesmo número de IP.

<figure><img src="../../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

Feito isso, o firewall está configurado para uso. Abaixo, seguem mais orientações para aproveitar ao máximo esse recurso.

Nesta mesma aba, é possível visualizar as regras cadastradas, lembrando que isso só funcionará se as etapas anteriores forem seguidas corretamente.&#x20;

<figure><img src="../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

Ao criar uma regra, um botão chamado ‘Ações’ é exibido no lado direito.&#x20;

Neste botão estão disponíveis algumas funcionalidades:

* **Edição:** Você pode modificar a regra, incluindo a alteração do nome e do endereço de IP associado.
* **Remover:** Remove a regra especificada. Ao excluir uma regra, lembre-se de que o usuário associado a ela perderá o acesso ao portal, a menos que possua a permissão específica de ‘Desconsiderar regras de firewall’, o que permitirá o acesso normal ao portal, tanto para usuários individuais quanto para grupos.
* **Auditoria de Entidade:** Aqui, você encontra informações sobre quem criou a regra e quando. Este menu permite visualizar as atividades dos usuários no portal de administração.

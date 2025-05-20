# Posso instalar o Power Embedded na minha infraestrutura?

Para clientes que possuem mais de 1.500 usuários ou por algum motivo, como LGPD, precisem que os recursos da aplicação fiquem sob a sua gestão, **existe um outro modelo de cobrança, no formato PaaS, que é uma assinatura mensal sem cobrança de usuários**.

Nesse formato, a equipe da Power Tuning instala o Power Embedded na assinatura Azure do cliente e realizará a cobrança da mensalidade de R$ 5.000,00 independente da quantidade de usuários, para mais ou para menos, e a gestão dos recursos fica por conta do cliente.

No modelo PaaS, além do custo do Fabric, o cliente que irá arcar com os custos de infraestrutura necessários para o Power Embedded funcionar (aproximadamente R$ 1.500,00), tendo total gestão sobre os recursos da aplicação e banco de dados, podendo escalar livremente conforme necessidade.



### Qual serviços o Power Embedded necessita?

Para conseguir instalar o Power Embedded na sua infraestrutura do Azure, você precisará dos seguintes recursos:

* 1 Azure App Service Plan Y1 com Windows (Azure Functions)
* 1 Azure App Service Plan P1V3 com Linux (Aplicação)
* 7 Azure App Service
* 1 Azure Azure Database for Postgres (2 vCores e 8 GB de RAM)
* 1 Azure Key Vault
* 1 Storage Account
* 1 Azure Cache for Redis Basic
* 1 Managed Identity
* 1 Azure OpenAI (Power Pilot - Opcional)
* 1 Azure Defender for Cloud (Opcional)



### Qual o custo dessa infraestrutura?

| Serviço                                                    | Estimativa de Custo (mensal) |
| ---------------------------------------------------------- | ---------------------------- |
| Azure App Service Plan Y1 com Windows (Azure Functions)    | USD 10,00                    |
| Azure App Service Plan P1V3 com Linux (Aplicação)          | USD 113,15                   |
| Azure Azure Database for Postgres (2 vCores e 8 GB de RAM) | USD 129,94                   |
| Disco P15 - 256 GB                                         | USD 29,44                    |
| Azure Key Vault                                            | USD 34,00                    |
| Storage Account                                            | USD 20,00                    |
| Azure Cache for Redis Basic                                | USD 16,00                    |
| Managed Identity                                           | USD 0,00                     |
| Azure OpenAI (Power Pilot - Opcional)                      | USD 10,00                    |
| Azure Defender for Cloud (Opcional)                        | USD 200,00                   |
| **TOTAL**                                                  | USD 362,63                   |

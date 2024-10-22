# Segurança interna do Power Embedded

A segurança interna do Power Embedded é extremamente robusta e o sistema utiliza uma arquitetura toda baseada em recursos SaaS auto-gerenciados no Azure, onde a gestão é feita pela Microsoft, backups automáticos e alta disponibilidade da aplicação e do banco de dados por zonas de disponibilidade com failover automático e com garantia de disponibilidade de 99,99%.

O sistema é submetido à diversos e complexos pentests de forma periódica, tanto automáticos feitos por ferramentas de pentest quanto validações e testes manuais, feitos por especialistas de segurança de empresas contratadas.

Todo o ambiente de nuvem é protegido pelo Microsoft Defender for Cloud, que faz a proteção, análise e recomendações de forma proativa e contínua.

O acesso aos recursos do Azure é bloqueado para internet e só acessível através de VPN.

A comunicação entre o sistema e o navegador é criptografa utilizando certificados SSL (HTTPS).

A chave de acesso ao Power BI é armazenada no banco de dados criptografada utilizando o algoritmo mais seguro do mercado (RSA-OEAP) e vários mecanismos de proteção para garantir que mesmo em um eventual acesso indevido ao banco de dados, essa chave não possa ser decodificada, uma vez que o acesso à chave de segurança para descriptografar (que é individual por cliente) fica em um Azure KeyVault onde somente a aplicação possui permissão e conectividade para acessar.

A chave da API pública é criptografada utilizando um algoritmo de HASH que não permite recuperação do valor gerado, assim como o secret de um KeyVault.



### Documentação técnica do Power Embedded

{% embed url="https://powerembedded.com.br/arquitetura" %}


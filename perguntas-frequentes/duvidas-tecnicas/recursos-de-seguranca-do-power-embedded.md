# Recursos de Segurança do Power Embedded

Um dos principais pilares do Power Embedded é em relação à Privacidade dos dados & Segurança. Por conta disso, incluímos diversos controles, auditorias e recursos para melhorar a governança e ajudar as empresas a evitarem vazamentos de dados.



Controles de Segurança do Power Embedded:

1️⃣ **Controle de acessos por usuários e grupos**: Defina quais relatórios cada pessoa ou grupo podem acessar e quais as permissões desses usuários.

2️⃣ **Segurança a nível de linha (RLS)**: Diferentes usuários irão visualizar diferentes informações do mesmo relatório, de acordo com as regras de RLS definidas no relatório.

3️⃣ **Segurança a nível de objeto (OLS)**: Controle de segurança a nível de medida, coluna ou tabela, onde só as pessoas com as devidas permissões vão conseguir visualizar os gráficos que utilizam os objetos protegidos.

4️⃣ **Segurança a nível de página (PLS)**: Controle quais páginas do relatório cada usuário ou grupo pode visualizar ao acessar.

5️⃣ **Controle de acessos por IP**: Defina faixas de IPs específicas, como a rede interna da empresa, e os usuários só poderão visualizar os relatórios caso estejam conectados nessas faixas de IP, podendo configurar cenários de exceção também.

6️⃣ **Controle de acessos por horário**: Defina os dias e horários que os usuários poderão acessar os relatórios e evite horas extras desnecessárias e não aprovadas.

7️⃣ **Marca d'água nos relatórios**: Quer evitar prints e fotos da tela para não ter vazamentos de dados? Nós criamos uma solução pra isso, inserindo várias marcas d'água no relatório ao ativar esse recurso no relatório, com email, data e hora do usuário que está acessando. Se vazar algum print, já sabe quem e quando vazou.

8️⃣ **Controle de exportação dos dados**: Controle quem pode exportar os dados dos visuais de cada relatório.

9️⃣ Controle granular de APIs: Crie chaves de integração com a API do sistema e selecione quais endpoints a chave criada poderá utilizar.

🔟 Controle de login: Selecione quais os métodos de autenticação (Integrada Microsoft, Google ou Email/senha com MFA) cada usuário poderá utilizar para logar no portal, que já tem proteção Google Recaptcha V3

1️⃣1️⃣ Controle de sessão: Defina quantos minutos o portal irá desconectar o usuário automaticamente após inatividade, exigindo um novo login.

1️⃣2️⃣ Controle de localização: Saiba de qual endereço IP, cidade e estado seus usuários estão e qual a operador de internet estão utilizando.



Além disso, também temos diversas auditorias para analisar a utilização do sistema pelos usuários:

* Quem está visualizando cada relatório, quem baixou o PBIX e quem exportou os dados para PDF ou PPTX
* Qual página do relatório ou visual/gráfico cada usuário está utilizando
* Quem logou ou tentou logar no portal
* Quem alterou algo no sistema (permissão, usuário, relatório, configuração, etc)
* Quais as permissões que cada usuário ou grupo possui nos relatórios, incluindo funções de RLS que ele tem acesso
* Quem está utilizando a IA Generativa, seja pelo portal ou por WhatsApp
* Quem solicitou acesso em relatórios e quem aprovou/recusou
* Quem está tentando acessar o portal utilizando IPs não autorizados

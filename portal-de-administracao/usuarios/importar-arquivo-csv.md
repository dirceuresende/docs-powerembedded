# Importar arquivo CSV

Esse método permite que você possa importar um arquivo texto, no formato CSV, contendo uma lista de emails para serem importados em massa para o Power Embedded.

<figure><img src="../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

\
A plataforma suporta os três tipos de layout abaixo:

* **2 colunas:** \[E-mail, Nome] (importação sem senha);
* **3 colunas:** \[E-mail ,Nome, Senha] (importação com senha);
* **7 colunas:** \[E-mail, Nome, Senha, Função, Grupo, Departamento, Empresa] (importação completa);



Observações sobre o arquivo CSV que será importado:

* O arquivo deve ter a extensão **“.csv”**;
* O arquivo deve ter um cabeçalho na primeira linha, seguindo um dos três layouts disponíveis:
* Se o campo senha estiver vazio, o usuário será criado sem senha e essa senha poderá ser definida usando o link de “Registrar” na tela de login;
* Caso você esteja utilizado a importação completa e os campos: função, grupo, departamento ou empresa estiverem vazios, será criado um usuário básico sem essas informações e você precisará adicionar manualmente no sistema;
* Caso você esteja utilizando a importação completa e os campos: Grupo e/ou Empresa informados no CSV não existirem no sistema, estes serão criados automaticamente;
* Caso o usuário já exista no sistema, ele será atualizado com as informações do arquivo CSV (exceto e-mail, que não é alterável);
* As senhas devem conter letras não alfanuméricas, maiúsculas e minúsculas com no mínimo 8 caracteres.

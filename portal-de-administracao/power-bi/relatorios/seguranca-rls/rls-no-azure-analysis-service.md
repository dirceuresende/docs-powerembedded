---
hidden: true
---

# RLS no Azure Analysis Service

1. **Adicione o Service Principal como administrador no Azure Analysis Services.**
2.  Após essa configuração, certifique-se de que a regra de RLS criada utilize a função `CustomData()`.

    > **Importante:** Em cenários de embed (incorporação), **somente** a função `CustomData()` é compatível.

    Exemplo de uso:

    ```dax
    daxCopiarEditar[Email] = CUSTOMDATA()
    ```
3. Com a regra definida, vincule o Service Principal à RLS utilizando o **SQL Server Management Studio (SSMS)**.
4. Agora, acesse o **portal de administração do Power Embedded**.\
   Vá até a seção **Conjuntos de Dados**, selecione o conjunto desejado e clique em **Ações > Segurança**.
5. Crie uma nova regra manual com **o mesmo nome da regra definida no Azure Analysis Services**.
6. No menu de **RLS Dinâmica**, marque a opção correspondente (checkbox) para ativar a aplicação automática da RLS com base no valor passado via `CustomData()`.

O primeiro passo para que a RLS (Row-Level Security) funcione corretamente no Azure Analysis Services com Power Embedded é adicionar o **Service Principal** como **administrador do recurso** no portal do Azure. Siga estes passos:

#### Configuração de RLS no Azure Analysis Services para uso com Power Embedded

\

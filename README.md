## SQL

- Linguagem de Consulta a Banco de dados. Voltada para manipulação de dados. 

Abaixo citaremos os principais subgrupos de comandos dentro do SQL.
- DDL: Data Definition Language - Comandos usados para criar, alterar ou excluir a `estrutura` de objetos no banco de dados. `CREATE` `ALTER` `DROP` `TRUNCATE`.
<br><br/>
- DML: Data Manipulation Language - Diferente do DDL, que manipula a estrutura o DML manipula o dado. Ou seja os comandos do DML é diretamente ligado aos dados. `INSERT` `UPDATE` `Delete`. (Dentro do CRUD, refere-se ao C, U e D)
<br><br/>
- DCL: Data Control Language - Comandos para gerenciar acessos ao banco de dados. Exemplo: Permitir que um usuário possa ler. `GRANT` (Garantir o acesso) e `REVOKE` Revoga o acesso.
<br><br/>
- DQL: Data Query Language - Comandos que buscam e recupera os dados de um banco de dados - `SELECT` Comando principal.
<br><br/>
<br>
---
<br>
<br>
<br>
<br>


<h1> Diagrama SQL
<br>
<br>

---

```mermaid
mindmap
  root(( Linguagem SQL ))
    DDL
      Definicao de Dados
      CREATE: Cria tabelas
      ALTER: Modifica estrutura
      DROP: Exclui objetos
      TRUNCATE: Esvazia tabela
    DQL
      Consulta de Dados
      SELECT: Busca registros
    DML
      Manipulacao de Dados
      Relacionado ao CRUD
      INSERT: Adiciona dados
      UPDATE: Atualiza dados
      DELETE: Apaga registros
    DCL
      Controle de Dados
      GRANT: Concede permissao
      REVOKE: Remove permissao

```
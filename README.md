# dojo-SQL
Este repositório contém o material para realização do **DOJO sobre SQL**. O objetivo deste Dojo é treinar o uso da linguagem de SQL. Ou seja, pretendemos exercitar a compreensão e escrita de *Queries SQL*.

Para o exercício foi escolhido um banco de dados contendo registros de locadora de DVD. As tabelas estão organizadas como dispostas no diagrama a seguir:

![Diagrama da base dados](dvd-rental-sample-database-diagram.png)

# Como rodar

Estão incluídos um Script `docker-compose` que inicializa 2 containers, um para rodar o servidor de banco de dados PostgreSQL e outro para rodar a aplicação PgAdmin, utilizada para acessar o BD e onde executaremos as consultas SQL.

1. Clone o código deste repositório `$ git clone https://github.com/economiagovbr/dojo-SQL.git`
2. Acesse o diretório do material `$ cd dojo-SQL`
3. Acesse o PgAdmin  [http://localhost:5555/](http://localhost:5555/) com o usuário e senha;

   3.1 - Abra o terminal conecte no postgres (sudo -u postgres psql) e verifique qual usuário está criado (\du)
   4.
   5.2 - Se não tiver usuário criado, crie: `create user teste`
   
   7.3 - Defina senha: `ALTER USER teste WITH PASSWORD 'senha'`;
   
   7.4 - Testar a coneção com o usuário: `psql -u teste -h localhost -W`
   
4. Crie um novo database: create database dvd;
5. Carregue o banco  dvdrental.tar;
   `pg_restore --host "localhost" --port "5432" --username "teste"  --dbname "dvd" --verbose "dvdrental.tar"`
 
6. MÃOS À MASSA!
7. Para iniciar, listamos no arquivo [desafios.md](desafios.md) algumas questões introdutórias sobre a base de dados de aluguel de DVDs.

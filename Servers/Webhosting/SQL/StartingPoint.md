<{[ SQL ]}>--------------------------------------
DataBase managment system (DBMS) = MySQL, MariaDB,
Relational DB MS (RDBMS) = database tables that links "Relates"to each other.
non-relational (NRDBS) = noSQL

### MANAGMENT
show databases;
use "database";

show tables;
describe "table"
select * from "table";

SELECT name FROM name WHERE variable>30 or variable="Philip";
SELECT * FROM name ORDER BY variable ASC;	+ DESC

### DB
create table "name" ( colum1 int, colum2 varchar(69420), colum3 varchar("max size") );

### Table
insert into "db_name" values ( 1, "hello" , "bye" );
ALTER TABLE name ADD COLUMN id int FIRST;	+ AFTER

UPDATE name SET value=1 WHERE row="value"; 
DELETE FROM "name" WHERE name="Philip";

### Users

**[ User ADD ]**
>CREATE USER 'sammy'@'localhost' IDENTIFIED BY 'password';

**[ List User ]**
>SELECT user FROM mysql.user

**[ User Permisions ]**
>GRANT PRIVILEGE ON database.table TO 'username'@'host';
>GRANT ALL PRIVILEGES ON \*.\* TO 'username'@'localhost'

NOT 127.0.0.1

**[ Alter User ]**
>ALTER USER 'user'@'localhost' IDENTIFIED BY 'NewPassword'


# Basic Java Swing Form
This repository contain a Java Swing Project that inplements a simple MySQL database connection, on this example we make a get and a post to the database.

Install and use the project
=================

1.- Download the full project
2.- Create a database called "db01" on any MySQL console or clien.
3.- Create the table "gender" with the the following atributes: 
```

gender_id (PK)
gender

```
4.- Create table "human" with the following atributes:
```

human_id (PK)
first_name
last_name
age
gender (FK of gender table)

```
5.-  Create a store procedure called "sp_getGender" with the next lines:
```

delimiter //
create procedure sp_getGender()
begin
declare x_var nvarchar(20);
set x_var = 'varaible';
	select gender_id, gender from gender;
end//
delimiter//

```
6.- Fill the gender table with the next lines:
```

insert into gender(gender) values ("Man");
insert into gender(gender) values ("Woman");
insert into gender(gender) values ("Undefined");

```
7.- Enjoy the software :D

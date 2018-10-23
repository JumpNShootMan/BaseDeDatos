Familiarizandonos con el lenguaje y la sintaxis... Creamos tablas y registros obligatorios, etc

use master
create database Prueba
use prueba

CREATE TABLE VIDEO(
VideoID char(03) not null,
Título varchar(50) not null,
Stock int not null,
primary key (VideoID),
check (Stock>0)
)

create table Empleado(
IDEmpleado int not null primary key,
Nombres varchar(50) not null,
Antiguedad int
)

ALTER TABLE Empleado
	ADD CONSTRAINT CHK_Antiguedad_Empleados 
	Cgeck (Antiguedad > 0 AND Antiguedad < 50)

insert into Empleado values(001, 'Mouse Mickey',20)

ALTER TABLE Empleado alter column Antiguedad int not NULL

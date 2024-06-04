# SQL---First-Skill-Test Code


/* Create a table called the Employee table */
create table Employee (
Employee_id INT,
First_name VARCHAR(50) NOT NULL, 
Last_name VARCHAR(50) NOT NULL,
Age INT,
Salary INT,
Job VARCHAR(50) NOT NULL
)

select * from employee
/* Insert data into table */

insert into employee (Employee_id, First_name, Last_name, Age, Salary, Job)
values 
(01, "Lateef", "Salau", 30, 120000, "Data Analyst"),
(02, "Kalu", "Lekwa", 31, 150000, "Computer Engineer"),
(03, "William", "Akpode", 28, 180000, "Writer"),
(04, "Ade", "Adepoju", 26, 190000, "Marketer"),
(05, "Emerald", "Effiong", 28, 190000, "Car Entuthiast"),
(06, "Anita", "Uche", 26, 140000, "Service Apartment"),
(07, "Amanda", "Ezinne", 27, 150000, "Fashion Designer"),
(08, "William", "Oyiwona", 28, 130000, "Farm producer"),
(09, "Umoh", "Etoro", 25, 160000, "Fashion Designer"),
(10, "Kayode", "Asemota", 28, 140000, "Product designer")

/* Use SELECT statment to view table*/
select * from Employee

/* Using the WHERE statement */
select * 
from Employee
where Age > 28

/* Adding a new column into an existing table */
alter table employee 
add column Gender VARCHAR (50) NOT NULL

/* Rearranging the columns */
alter table employee
modify Gender VARCHAR(50) after Last_name

/* Inserting data into the Gender column */
update employee
set Gender = "F"
where Employee_id = 9


/* Creating SQL views */
Create view Duet_employee As
Select * 
from employee
where salary >= 150000

select * from Duet_employee

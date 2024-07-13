create database guvi;
use guvi;
--------------------------

create table students(
studentid int primary key auto_increment,
studentname varchar(35) unique,
mail varchar(300) unique,
mobil varchar(30) not null
);
--------------------

create table course(
course_id int auto_increment primary key,
studentid int,
course_name varchar(35),
course_duration varchar(300),
course_fees varchar(35),

foreign key(studentid) references user(studentid)
);

--------------------

create table admission(
studentid int,
course_id int,
admission_fees varchar(25),
foreign key(studentidid) references user(studentidid),
foreign key(course_id) references course(course_id)
);

-------------------------

create table mentor(
studentid int,
course_id int not null,
mentor_name varchar(25) ,
foreign key(studentid) references user(studentid),
foreign key(course_id) references course(course_id)
);



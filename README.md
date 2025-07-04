# Task5 - JOINS ( INNER,LEFT,RIGHT,FULL)

CREATE TABLE employee1 ( emp_id INT PRIMARY KEY,
    emp_name VARCHAR(100) NOT NULL,
	gender VARCHAR(10),
    job_title VARCHAR(50),
    email VARCHAR(100) UNIQUE,
    phone_number VARCHAR(15));
CREATE TABLE employee2 ( emp_id INT PRIMARY KEY,
    emp_name VARCHAR(100) NOT NULL,
    gender VARCHAR(10),
    job_title VARCHAR(50),
    email VARCHAR(100) UNIQUE,
    phone_number VARCHAR(15));
Insert into employee1 (emp_id,emp_name,gender,job_title,email,phone_number) values
('1','Uday','Male','Developer','uday11@gmail.com','9554762315'),
('2','Alexa','Female','Programmer','Alexa12@gmail.com','7985645985'),
('3','Suhana','Female','Analyst','Suhana13@gmail.com','9751432563'),
('4','Steve','Male','Programmer','Steve10@gmail.com','8798641585'),
('5','Joe','Male','Programmer','Joe18@gmail.com','8945478495');
Insert into employee2 (emp_id,emp_name,gender,job_title,email,phone_number) values
('1','Sahu','Male','Developer','sahu11@gmail.com','9754762315'),
('6','Sweety','Female','Programmer','Sweety12@gmail.com','7885645985'),
('3','John','Male','Programmer','John18@gmail.com','8145478495'),
('4','Betu','Female','Analyst','Betu13@gmail.com','8951432563'),
('5','Smith','Male','Programmer','Smith10@gmail.com','8398641585');

---INNER JOIN---

Select * FROM employee1 INNER JOIN employee2 
ON employee1.emp_id=employee2.emp_id;

---LEFT JOIN---

Select * FROM employee1 LEFT JOIN employee2 
ON employee1.emp_id=employee2.emp_id;

---RIGHT JOIN---

Select * FROM employee1 RIGHT JOIN employee2 
ON employee1.emp_id=employee2.emp_id;

---FULL JOIN WITH HELP OF UNION---

Select * FROM employee1 LEFT JOIN employee2 
ON employee1.emp_id=employee2.emp_id
UNION
Select * FROM employee1 RIGHT JOIN employee2 
ON employee1.emp_id=employee2.emp_id;

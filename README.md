# Deploying Web App API and MySQL server on Kubernetes

### Code Repo URL:
https://github.com/shivank24/kubernetes_app


### Docker Hub URL for image:
https://hub.docker.com/r/skj03/python-mysql/tags

### SERVICE API URL:
http://{HOST}:5000/students

### RECORDING LINK:
`https://nagarro-my.sharepoint.com/:v:/p/shivank_jain/EZsWQv22P5FIuWHEst2nOdUBtmYFAGPyiwWiKAUj6BXcVA?e=XTeTdm`


## Initial Database data load
To save initial database records do below steps:

Step 1: Run below command to login to mysql instance
```
kubectl run -it --rm --image=mysql --restart=Never mysql-client -- mysql --host mysql --password={db_password}
```

Step 2: Run below commands to create database and create records
```
CREATE DATABASE school;
USE school;
CREATE TABLE students(student_id INT PRIMARY KEY AUTO_INCREMENT, name VARCHAR(255), roll_no INT);
insert into students(name, roll_no) values('rohan', 23);
insert into students(name, roll_no) values('karan', 12);
insert into students(name, roll_no) values('raj', 22);
insert into students(name, roll_no) values('nita', 05);
insert into students(name, roll_no) values('vicky', 45);
insert into students(name, roll_no) values('dev', 3);
insert into students(name, roll_no) values('Naina', 14);
```

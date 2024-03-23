# SQL-Query-20-


/*  Query no 1 for Storing Firstname as Employee_name */
select e_Firstname as EMPLOYEE_NAME from Employee;

/* Query no 2 for Getting all letter in captial        */
select upper(e_Firstname) from Employee ;

/* Query no 3 to select all different value in the table  */
select distinct department from Employee ;

/*  Query no 4 to get first 3 letters  */
select left(e_Firstname,3)  from Employee;

/*Query No 5 TO find any letter from  */
select position('a' in e_Firstname) from Employee;

/*Query no 6  to remove the white space from right side */
select rtrim(e_Firstname) from Employee;

/*Query no 7  to remove the white space from left side */    /*We can also use trim to remove all white space */
select ltrim(e_Firstname) from Employee;

/* Query no 8 to get the length of  character of department column(Data)  */
select distinct department ,length(department) from Employee;

/* Query no 9 it is use replace any character with other charater   */
select replace(e_Firstname,'a','A') from Employee  ;

/* Query no 10 it is use concat to columns    */
select concat( e_Firstname,'  ',e_lastname) as COMPLETE_NAME from Employee;

/* Query no 11 it is use  the columns details in ascending order  */
select * from Employee order by e_Firstname;

/* Query no 12 it is use  the columns details in ascending order  and Descending Order */
select * from Employee order by e_Firstname asc,department desc ;

/* Query no 13 it is use to print the details if Firstname is Vipul or Satish  */
select * from Employee where e_Firstname='Vipul' or e_Firstname='Satish';


/* Query no 14 it is use to print the details if Firstname is not  Vipul or Satish  */
select * from Employee where e_Firstname Not in  ('Vipul','Satish');


/*Query no 15  it is use to print details if department is Equal to Admin  */
select * from Employee Where department ='Admin';

/* Query no 16 it is use to print detail if Firstname contain a in it */
select * from Employee where e_Firstname like ('%a%') ;

/* Query no 17 it is use to print detail if Firstname ends with a in it */
select * from Employee where e_Firstname like ('%a') ;

/*Query no 18 it is use to print detail if firstname is = 6 and ends with h */
select * from Employee where length(e_Firstname)=6 and e_Firstname like('%h');

/* Query no 19 it is use to print details if its salary is between 100000 to 500000 */
select * from Employee where e_Salary>=100000 and e_Salary <=500000;

/* Query no 20 it is use to print detail of those who has joined on feb 2014  */
select * from Employee Where date_format(e_doj,'%y-%m')='2014-02';


# JDBC SQL injections 

This sample application creates a database and runs some commands in it. 
There is a SQL injection bug in the application's code. You have two tasks:

 - find an argument for deposit10 method which causes corruption in the database
 - fix the deposit10 method so that it works with all possible arguments 

The application uses an embedded H2 database (http://h2database.com). 
You don't need to install anything - just start the application and the database will automatically start inside your JVM. 

## Task 1: cause corruption in the database
Don't change the method deposit10 yet. 
Change the argument to deposit10 in the main method, so that one of the following happens:

 - money is deposited to ALL accounts instead of one
 - some new account is added
 - some accounts are deleted 
 
Only try out the "drop table" example if you can't get any of the above working!

## Task 2: fix the injection bug
Change the deposit10 method to use parameterized prepared statements. 
Make sure that the method works with the original argument "Märt".
Verify that the argument string you created in task1 no longer hacks anything.   

## Results to submit

 - attack argument from task1
 - fixed deposit10 method

## Read about SQL injection

 - http://bobby-tables.com/ (see the front page, "About" page and "Java" page)
 - http://codecurmudgeon.com/wp/sql-injection-hall-of-shame/ 
 - https://www.owasp.org/index.php/SQL_Injection_Prevention_Cheat_Sheet


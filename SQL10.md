# SQL Injection in Blood Bank Management System via Admin Login page 

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

\blood bank2\admin\admin_login.php(8) username parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

username parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.

## **Vulnerability recurrence**

### **POC**
1. Navigate to admin login page 
2. Once logged in, navigate to /blood%20bank2/admin/index.php path
   ![image](https://github.com/user-attachments/assets/705a94b8-af02-4c8b-b172-47034cde88d6)
3. Fill user name and passwrod and submit the request and intercept it in Burp Proxy tool
4. Inject simple SQL Injection payload (`) in the code paramter
5. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/a72fdf5e-15cf-40d5-8902-b3da7b29bf3e)
6. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
  ![image](https://github.com/user-attachments/assets/5392fb26-246e-49c7-ab8a-db57e5e34389)


### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/admin/index.php
```
![image](https://github.com/user-attachments/assets/8ff967d7-0c99-4b5f-8471-432fdcfa234c)


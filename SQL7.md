# SQL Injection in Blood Bank Management System via Code Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

\blood bank2\admin\add_city.php(10) code parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

code parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.


## **Vulnerability recurrence**

### **POC**
1. Login into the application as Admin privilege user
2. Once logged in, navigate to /blood%20bank2/admin/city.php path
3. Fill all the details and submit the request and intercept it in Burp Proxy tool
   ![image](https://github.com/user-attachments/assets/41ea4a04-8c48-447b-a5e3-6ec0e50e781a)
4. Inject simple SQL Injection payload (`) in the code paramter
5. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/1c0fb154-8d4b-4962-83d0-c42879be8500)
6. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
   ![image](https://github.com/user-attachments/assets/c3672769-4906-4104-a1c5-fabbd02457c4)

### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/admin/city.php
```
![image](https://github.com/user-attachments/assets/55f43c8c-11c5-47d6-afdf-db93103a5516)


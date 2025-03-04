# SQL Injection in Blood Bank Management System via state_id Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

\blood bank2\admin\edit_state.php(9) state_id parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

state_id parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.


## **Vulnerability recurrence**

### **POC**
1. Login into the application as Admin privilege user
2. Once logged in, navigate to /blood%20bank2/admin/edit_state.php?state_id= path
3. Inject simple SQL Injection payload (`)
4. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/e8cd1c81-cad9-43b8-8d6c-3e9911403983)
5. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
   ![image](https://github.com/user-attachments/assets/87bb907f-7f51-4d0b-86aa-751ba09fd39c)

### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/admin/edit_state.php?state_id=
```
![image](https://github.com/user-attachments/assets/157c481c-7062-43ad-80ad-21ff1627469b)


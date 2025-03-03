# SQL Injection in Blood Bank Management System via requester_id Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

\blood bank2\user_dashboard\delete_requester.php requester_id parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

requester_id parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.


## **Vulnerability recurrence**

### **POC**
1. Login into the application as low privilege user
2. Once logged in, navigate to /blood bank2/user_dashboard/delete_requester.php?requester_id= path
3. Inject simple SQL Injection payload (`)
4. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/e14095cc-66b0-4c64-a230-18e71fe2db79)
5. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
   ![image](https://github.com/user-attachments/assets/778b16c5-ed98-44bb-bb45-12faf202a9b6)

### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood bank2/user_dashboard/delete_requester.php?requester_id=
```
![image](https://github.com/user-attachments/assets/47d57f28-93d8-4059-a4f8-37e58f263253)


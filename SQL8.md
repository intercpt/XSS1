# SQL Injection in Blood Bank Management System via name Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

\blood bank2\user_dashboard\add_donor.php name parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

name parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.


## **Vulnerability recurrence**

### **POC**
1. Login into the application as Low privilege user
2. Once logged in, navigate to /blood%20bank2/user_dashboard/donor.php path
3. Click on `Donate Blood`
   ![image](https://github.com/user-attachments/assets/33d6e9de-aa65-4825-babf-e830d3499d2f)
4. Fill all the details and submit the request and intercept it in Burp Proxy tool
5. Inject simple SQL Injection payload (`) in the name paramter
7. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/1211ba47-3e8d-435e-b442-b2aca8707277)
8. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
   ![image](https://github.com/user-attachments/assets/879d266e-31f6-40e7-9e9c-3efdd6c4a5fb)

### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/user_dashboard/donor.php
```
![image](https://github.com/user-attachments/assets/a9dee6b6-89c1-4d7d-a7d8-1c7c3890d128)


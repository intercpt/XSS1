# SQL Injection in Blood Bank Management System via fullname Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

blood bank2\member_register.php fullname parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

fullname parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.

## **Vulnerability recurrence**

### **POC**
1. Navigate to registration page
2. Inject SQL injection payload in `Fullname` field
   ![image](https://github.com/user-attachments/assets/7642e051-ecd5-48e5-bb54-9ffa7dc1ae09)
3. Observe that noted endpoint is vulnerable to SQL Injection
   ![image](https://github.com/user-attachments/assets/705bf6b6-8ba1-430c-aba5-8848c2f626f6)
4. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable
  ![image](https://github.com/user-attachments/assets/f8f44b2b-c0b6-4fb8-98cf-9c4751c6c0b1)

### Result

fullname parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/register.php
```
![image](https://github.com/user-attachments/assets/62d60b3f-d1dd-4c60-9076-a157c9a6ce40)

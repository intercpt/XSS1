# SQL Injection in Blood Bank Management System via member_id Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

blood bank2\admin\delete_members.php member_id parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

member_id parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.


## **Vulnerability recurrence**

### **POC**
1. Login into the application as super admin privilege user
2. Once logged in, navigate to /blood%20bank2/admin/delete_members.php?member_id= path
3. Inject simple SQL Injection payload (`)
4. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/12c41e07-5314-47f0-9012-4ba10b49efaa)
5. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
   ![image](https://github.com/user-attachments/assets/825392a6-3d53-4c80-83c5-570f66d9d209)


### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/admin/delete_members.php?member_id=
```
![image](https://github.com/user-attachments/assets/dfc8f9ff-acd6-4c06-bc2f-95b9e3541d70)


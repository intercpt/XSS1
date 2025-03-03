# SQL Injection in Blood Bank Management System via blood_id Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

\blood bank2\admin\delete_bloodGroup.php(6) blood_id parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

blood_id parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.


## **Vulnerability recurrence**

### **POC**
1. Login into the application as Admin privilege user
2. Once logged in, navigate to /blood%20bank2/admin/delete_bloodGroup.php?blood_id= path
3. Inject simple SQL Injection payload (`)
4. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/24f5900e-20d6-42ca-999f-02e3d679f75f)
5. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
   ![image](https://github.com/user-attachments/assets/aa3246c1-0231-4b54-b39d-98f52096d004)


### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/admin/delete_bloodGroup.php?blood_id=
```
![image](https://github.com/user-attachments/assets/ec3000d9-6c03-4067-a545-124113eb8901)


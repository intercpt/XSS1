# SQL Injection in Blood Bank Management System via donor_id Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

\blood bank2\user_dashboard\view_donor.php donor_id parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

SQL Injection

## **Description of the vulnerability**

donor_id parameter in the Blood Bank Management System is vulnerable to SQL Injection. This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.


## **Vulnerability recurrence**

### **POC**
1. Login into the application as low privilege user
2. Once logged in, navigate to /blood%20bank2/user_dashboard/view_donor.php?donor_id= path
3. Inject simple SQL Injection payload (`)
4. Observe that application responds with SQL Error
   ![image](https://github.com/user-attachments/assets/b0f00a90-5c8f-4ff3-a743-134584de98b1)
5. Now use SQLMap or manual approach and observe that this vulnerable enpoint is completely exploitable.
   ![image](https://github.com/user-attachments/assets/c039190a-78de-4770-9feb-b86309822dbd)

### Result

This vulnerability allows attackers to inject malicious SQL queries to the backend database which could result compromise of Confidentiality, integrity and availability of the data and the system.
```
http://bloodbankmgmtsystem/blood%20bank2/user_dashboard/view_donor.php?donor_id=
```
![image](https://github.com/user-attachments/assets/9930c241-0249-4e5b-bd90-fcf6b4c41b19)


# Reflected Cross Site Scripting Vulnerability in Online Class and Exam Scheduling System via room Parameter

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

blood bank2/user_dashboard/donor.php name parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

Reflected Cross Site Scripting Vulnerability

## **Description of the vulnerability**

Room parameter in the Online Class and Exam Scheduling System is vulnerable to Reflected cross site scripting. This allows attackers to inject malicious javascript which gets executed on administratos session


## **Vulnerability recurrence**

### **POC**
1. Login into the application 
2. Navigate to /scheduling/pages/room.php?id=1&room="><img%20src=x%20onerror=confirm(1)%20/>
3. Observe that XSS is executed
   ![image](https://github.com/user-attachments/assets/3a6d0186-e4d2-4a50-88b2-3699c03865f1)


### Result

We can trigger the XSS vulnerability by loading the URL

```
http://bloodbankmgmtsystem/scheduling/pages/room.php?id=1&room=
```
![image](https://github.com/user-attachments/assets/bcad68e5-a8f7-4c5c-beef-e42a24c3a4fc)

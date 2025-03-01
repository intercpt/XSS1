# Stored Cross Site Scripting Vulnerability in Blood Bank Management System via name Parameter

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

Stored Cross Site Scripting Vulnerability

## **Description of the vulnerability**

Name parameter in the Blood Bank Management System is vulnerable to stored cross site scripting. This allows attackers to inject malicious javascript which gets executed on another users session or administratos session


## **Vulnerability recurrence**

### **POC**
1. Login into the application as low privilege user
2. Once logged in, navigate to blood%20bank2/user_dashboard/donor.php path
3. Click on `Donate Blood`
   ![image](https://github.com/user-attachments/assets/340dbe35-3ccb-4061-b8c5-e767b9409ce0)
4. Inject XSS payload in `Name` field
   ![image](https://github.com/user-attachments/assets/7dfc3a1b-f6a6-4e6a-8a64-14da50f18915)
5. Observe that XSS is executed
   ![image](https://github.com/user-attachments/assets/158b0866-3842-455d-9330-d817794a3737)

### Result

We can trigger the XSS vulnerability that was just inserted by accessing  donor.php. 

```
http://bloodbankmgmtsystem/donor.php
```
![image](https://github.com/user-attachments/assets/22871d6b-b930-469e-a85a-558b7244b646)

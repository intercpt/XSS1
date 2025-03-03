# Unauthenticated Directory listing in Blood Bank Management System

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Blood Bank Management System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/blood-bank-management-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

/blood bank2/upload/

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/09f1f26e-072d-4fec-bd3b-974076ee162c

# PROBLEM TYPE

## Vulnerability Type

Directory listing

## **Description of the vulnerability**

A directory listing vulnerability occurs when a web server allows the listing of files within a directory, rather than providing a proper access control mechanism for file access. In the context of uploaded patient images, this means that sensitive images, such as medical records or photos, are stored in directories on the server that can be accessed by anyone without requiring authentication or authorization.

## **Vulnerability recurrence**

### **POC**
1. Login into the application as low privilege user
2. Once logged in, navigate to `Request for blood` and  add entry and upload a patient image
   ![image](https://github.com/user-attachments/assets/fee6017f-de5b-40e7-a136-5c699278913f)
3. Once uploaded
4. In another browser navigate to `/blood%20bank2/upload/` and observe that all the uploaded files accessible without authentication
   ![image](https://github.com/user-attachments/assets/60021d6a-9857-4033-ac0f-1db3c24f00eb)


### Result

A directory listing vulnerability occurs when a web server allows the listing of files within a directory, rather than providing a proper access control mechanism for file access. In the context of uploaded patient images, this means that sensitive images, such as medical records or photos, are stored in directories on the server that can be accessed by anyone without requiring authentication or authorization.
```
http://bloodbankmgmtsystem/blood%20bank2/upload/
```
![image](https://github.com/user-attachments/assets/ddbff5d0-31dd-44c5-96ba-4092cd7e1956)

# Stored Cross Site Scripting Vulnerability in Online Ticket Reservation System via Full Name, Address, Contact, Booked By  Parameter (Unauthenticated to Admin)

[Blood Bank Management System In PHP With Source Code](https://code-projects.org/blood-bank-management-system-in-php-with-source-code/)

## NAME OF AFFECTED PRODUCT(S)

**Online Ticket Reservation System In PHP With Source Code**

## Vendor Homepage

https://code-projects.org/online-ticket-reservation-system-in-php-with-source-code/

##  **Manufacturers sites**

https://code-projects.org/

# AFFECTED  VERSION(S)

## Vulnerable File

ticket%20reservation/passenger.php name parameter.

## VERSION(S)

-  v1.0

## Software Link

https://download.code-projects.org/details/2759a6ff-3a12-4b75-b979-4d31a269ee15

# PROBLEM TYPE

## Vulnerability Type

Stored Cross Site Scripting Vulnerability

## **Description of the vulnerability**

Multiple parameters in the Online Ticket Reservation System is vulnerable to stored cross site scripting. This allows attackers to inject malicious javascript from unauthenticated forms which results in executing administratos session


## **Vulnerability recurrence**

### **POC**
1. From unauth page navigate to ticket%20reservation/ path and reserve the ticket
2. Select destination and date.
3. Inject XSS payloads in Full Name, Address, Contact, Booked fields at ticket%20reservation/passenger.php
   ![image](https://github.com/user-attachments/assets/16830ddd-9c8a-49b3-a3d4-24d50d3149b3)
5. Submit above form
6. Login as admin
7. Observe that XSS is executed from all the injected fields
   ![image](https://github.com/user-attachments/assets/2716b5ff-cc2d-44b1-a0a2-48c0a38a1176)


### Result

We can trigger the XSS vulnerability that was just inserted by accessing  admin/reservation.php from admin session. 

```
http://ticketreservationsystem/ticket%20reservation/admin/reservation.php
```
![image](https://github.com/user-attachments/assets/6f4435af-6efd-46dd-b668-f62d0bb86a01)

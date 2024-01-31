# i-pos
Inventory & POS 
SYSTEM DOCUMENTATION 
Kate Murray 
karynmurray09@gmail.com 

  
1. INTRODUCTION 
1.1. Purpose of the document 
The main purpose of this document is to provide a comprehensive guide and reference 
point for the development and implementation of the Inventory Management and Point
of-Sale(POS) system. It serves as a detailed resource for developers, stakeholders and 
future maintainers of the systems. This documentation outlines the goals, requirements, 
architecture and timelines of the system.  
Developers 
Kate Karyn Murray 
Karynmurray09@gmail.com 
Kate.Murray@tnm.co.mw  
0886394280 
Client 
Daniel Phiri 
Daniel.Phiri@tnm.com.za  
1.2. Scope of the system 
The scope of the Inventory management and POS system encompasses end to end 
management of products, sales and stock levels within the business. The system aims 
to streamline all processes to increase efficiency and provide accurate records. Key 
functionalities and features are: 
1.2.1. 
Functionalities  
 Product management 
 Sales management 
 Stock level management 
 Reports and analytics 
 User authentications and authorization 
1.3. System overview 
The inventory management and POS system will be implemented as a mobile app for 
portability sake. It will be developed using the Flutter framework for the frontend and 
Firebase for the backend.  
2. BUSINESS REQUIREMENTS 
The main goal of this systems is to meet the business goals which include: 
2.1. Business goals 
a. Efficient Inventory Management 
 Streamline the process of managing stock to minimize effort and errors 
b. Improved sales management 
 Enhance the efficiency of sales recording to reduce inaccuracy 
c. Real-time Data monitoring 
 Provide real-time visibility into stock levels, enabling timely decision
making on stock replenishment and order fulfillment. 
d. Data-driven decision making 
 Enable data-driven decision-making through the generation of reports 
and analytics on product sales, stock turnover, and order fulfillment. 
2.2. Stakeholders  
a. Business owner/ manager: Require all-access to real-time reports, and 
analytics 
b. Staff: use the system for day to day inventory management and sales 
recording 
2.3. Functional Requirements 
a. Product management: ability to add new products, modify the products, delete 
the products with details like name, quantity, price etc… 
b. Sales tracking: ability to record a sale 
c. Stock level monitoring: real time monitoring of stock levels and automatic alerts 
d. Reports and analytics: generating of reports on products sales 
e. Authorization & authentication: secure role-based authentication and 
authorization  
2.4. Non-functional requirements 
a. Performance: the system should provide a quick and responsive interface 
b. Security: Secure authentication and authorization to protect sensitive 
information, audit logs  
c. Scalability: the systems should be able to handle growth 
3. SYSTEM ARCHITECTURE 
3.1. Development technology  
a. Front end: flutter will be used for the development of user interface. 
b. Back end: the backend & authorization will be handled by Firebase. 
c. Database: data will be stored in NoSQL database provided by Firebase 
4. DATA MODELLING 
4.1. Entity Relationship Diagram 
1. Product 
 Product ID(pk) 
 Name 
 Price 
 Quantity  
 Metric  
2. Sales  
 Sale ID(pk) 
 User ID (fk) 
 Date  
 Total Amount (total price * metric) 
3. Sales Details 
 SalesDetails ID(pk) 
 Sales ID(fk) 
 Product ID(fk) 
 Quantity  
 Unit Price 
4. Transactions 
 Transaction ID (pk) 
 Date 
5. User  
 User ID(pk) 
 Name 
 Role  
6. Audit log 
 Log ID(pk) 
 User ID(fk) 
 Action  
 Timestamp 
 
 
  
5. USER INTERFACE DESIGNING 
The system will have the following screens 
a. LOGIN SCREEN 
 Allows login with phone number 
 Screen for user to enter an OTP 
b. HOME SCREEN/DASHBOARD 
 Quick access to features on the app 
 Overview of products and metrics 
c. PRODUCT MANAGEMENT SCREEN 
 List all products available 
 Allows users to add new products 
 Provides options to edit or delete existing products 
d. PRODUCT DETAILS SCREEN 
 Detailed products about a product 
 Allows users to edit product details. 
e. SALES REPORTING SCREEN 
 Presents graphical representation of sales data 
f. USER MANAGEMENT SCREEN 
 Lists all users with roles and permissions 
 Allows admins to add, remove and edit users 
g. AUDIT LOG SCREEN 
 Lists log entries with user, action and timestamp 
h. PROFILE SCREEN 
 Displays user information 
i. 
POINT OF SALE SCREEN 
 Allows user to select products 
 Allows user to remove products  
 Shows total amount 
 Generates receipt  
6. SECURITY 
Ensuring the security of the Inventory Management System is paramount to protect 
sensitive data and maintain the integrity of the application. The following security 
measures have been implemented: 
6.1. User authentication 
The system utilizes Firebase Authentication to ensure safe and secure authentication 
process. 
 Users will be required to enter a phone number for authentication. After entering 
a phone number, they will receive a one-time-pin(OTP) in order to complete the 
authentication process. 
 Access to different sections of the app with be controlled by roles. Admins will 
have all access. 
 Audit logging will also be implemented to ensure integrity. A dedicated screen will 
include details of actions recorded including who recorded.  

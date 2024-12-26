

# Terminologies:


## 1. SERVER : 
* Originated from word 'serve'.
* Listens to the requests made by clients and sends back response.
 
* Example: Browsing a Website
  * You type www.google.com into your browser.
  * Your browser (client) sends a request to Google’s server.
  * Google’s server processes your request and sends back the webpage.


 ### 1.1 Types of Servers:
1. **Web Server**: Serves web pages (e.g., Apache, NGINX).
2. **Application Server**: Runs applications (e.g., Flask, Django).
3. **Database Server**: Stores and retrieves data (e.g., MySQL, PostgreSQL).
4. **File Server**: Manages file storage and retrieval.
5. **Mail Server**: Handles emails (e.g., Microsoft Exchange).
6. **Proxy Server**: Acts as a gateway between you and the internet.
 

### 1.2 Analogy: Running a Pizza Delivery Service
* **Web Server**: The menu on your website — serves static pages and accepts orders.
* **Application Server**: The chefs preparing the pizzas (business logic).
* **Database Server**: The pantry storing ingredients (user data and inventory).



 ### 1.3 How This Works in Action:
Let’s say a user visits an e-commerce site and asks for details about a product. Here’s how it happens:

Client Request:

The user’s browser sends a request to the web server to get product details.
Web Server:

The web server receives the request and forwards it to the application server (since the web server handles only basic requests like serving static files, not business logic).
Application Server:

The application server queries the database server for the product details using SQL (e.g., “SELECT * FROM products WHERE id = 123”).
Once the application server gets the data from the database, it might:
Apply business rules, like calculating discounts or checking stock availability.
Format the data: For example, converting prices into the correct currency or applying discount percentages.
It then prepares a response with the formatted data.
Database Server:

The database server holds the actual data and performs read and write operations as requested by the application server.
In the example, it would run the SQL query and return the product details to the application server.
Sending Response Back:

The application server sends the final response (product details with any calculations applied) to the web server, which then delivers it to the user’s browser.





 ---------------------------------------------------------------------------------------------------------------------------------------

## 2. PHYSICAL SERVERS IN THE CLOUD : 
* At the core, cloud providers have massive data centers filled with *thousands of physical servers*. 
* These servers are super powerful and are maintained in a controlled environment:
  * They are kept cool to prevent overheating.
  * They are backed up with multiple power sources for reliability.
  * They have high-speed network connections to handle huge amounts of data.

### 2.1 Why do we need Physical servers?
 * **To "rent computing power"** :
   * Small businesses are essentially renting access to **physical servers (and sometimes virtual ones)**.
   * Owned and managed by cloud providers like AWS, Microsoft Azure, or Google Cloud.

### 2.2 Virtualization:
* Cloud providers use virtualization to divide one ***physical server*** into ***multiple virtual servers*** (called Virtual Machines or VMs). 
* Each VM acts as if it’s a separate machine, with its own *operating system* and resources.

### 2.3 What are physical servers in the cloud:
* At the core, cloud providers have massive **Data centers**. 
* Each Data center consist of thousands of *Physical servers*.

## Stack of Physical Server:
           
             Applications
           -------------------
            sever-softwares : web-servers (Nginx, Apache), Database-servers(Mysql, Postgresql,etc), Application sever: Django, Node.js
           -------------------
            Operating system
           -------------------
               Hardware    : CPU, RAM, STORAGE, NETWORKING-CARDS








-----------------------------------------------------------------------------


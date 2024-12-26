

# Terminologies:


## Stateless and stateful:
### Stateless HTTP:
* HTTP is stateless, meaning servers don’t retain information about previous requests. so every request is new request..


# For designing of : Real-Time Chat APP:

1. the choice of network protocols is important:


          HTTP
Client ----------> Server


---------------------------------------------------------------------------------------------------------------------------------------------------

# SERVER : 
* Originated from word 'serve'.
* Listens to the requests made by clients and sends back response.
 
* Example: Browsing a Website
  * You type www.google.com into your browser.
  * Your browser (client) sends a request to Google’s server.
  * Google’s server processes your request and sends back the webpage.


 # Types of Servers:
1. **Web Server**: Serves web pages (e.g., Apache, NGINX).
2. **Application Server**: Runs applications (e.g., Flask, Django).
3. **Database Server**: Stores and retrieves data (e.g., MySQL, PostgreSQL).
4. **File Server**: Manages file storage and retrieval.
5. **Mail Server**: Handles emails (e.g., Microsoft Exchange).
6. **Proxy Server**: Acts as a gateway between you and the internet.
 

## Analogy: Running a Pizza Delivery Service
* **Web Server**: The menu on your website — serves static pages and accepts orders.
* **Application Server**: The chefs preparing the pizzas (business logic).
* **Database Server**: The pantry storing ingredients (user data and inventory).



 







 ---------------------------------------------------------------------------------------------------------------------------------------

# PHYSICAL SERVERS IN THE CLOUD : 
* At the core, cloud providers have massive data centers filled with *thousands of physical servers*. 
* These servers are super powerful and are maintained in a controlled environment:
  * They are kept cool to prevent overheating.
  * They are backed up with multiple power sources for reliability.
  * They have high-speed network connections to handle huge amounts of data.


# Virtualization:
* Cloud providers use virtualization to divide one ***physical server*** into ***multiple virtual servers*** (called Virtual Machines or VMs). 
* Each VM acts as if it’s a separate machine, with its own *operating system* and resources.

# What are physical servers in the cloud:
* At the core, cloud providers have massive **Data centers**. 
* Each Data center consist of thousands of *Physical servers*.

## Physical Server is just like a computer:
Let's understand the stack of server:

           
             Applications
           -------------------
            sever-softwares : web-servers (Nginx, Apache), Database-servers(Mysql, Postgresql,etc), Application sever: Django, Node.js
           -------------------
            Operating system
           -------------------
               Hardware    : CPU, RAM, STORAGE, NETWORKING-CARDS








-----------------------------------------------------------------------------


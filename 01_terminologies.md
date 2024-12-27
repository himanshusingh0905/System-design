

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
 

### 1.2 Analogy:
#### Example : Real-World Example: A Pizza Ordering App
* **Web Server (Waiter):** Displays the menu and sends the user’s pizza order to the kitchen. [Request of particular web-page]
* **Application Server (Chef):**
    * Processes the order (checks inventory, applies discounts).
    * Contacts the database to fetch details like crust types and toppings.
    * Prepares the final response (e.g., a confirmation of the order).
* **Database (Pantry):** Stores the ingredients, orders, and user preferences.


 ### 1.3 How This Works in Action:
#### Example: Let’s say a user visits an e-commerce site and asks for details about a product.

**[Client-request] -> [Web-server] -> [Application-server] -> [Database-server] -> [send-response]**

1. **Client Request:** The user’s browser sends a request to the web server to get product details.

2. **Web Server:** The web server receives the request and forwards it to the application server (since the web server handles only basic requests like serving static files, not business logic).

3. **Application Server:**
   * The application server queries the database server for the product details using SQL (e.g., “SELECT * FROM products WHERE id = 123”).
   * Once the application server gets the data from the database, it might:
      * Apply business rules, like calculating discounts or checking stock availability.
      * Format the data: For example, converting prices into the correct currency or applying discount percentages.
      * It then prepares a response with the formatted data.

4. **Database Server:** 
* The database server holds the actual data and performs read and write operations as requested by the application server.
* In the example, it would run the SQL query and return the product details to the application server.

5. **Sending Response Back:** The application server sends the final response (product details with any calculations applied) to the web server, which then delivers it to the user’s browser.





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
* **ON-Premise servers** were costly as maintaining them was a tedious job.


### 2.2 Stack of Physical Server:
           -------------------
           |  Applications   |
           -------------------
           | sever-softwares | -> web-servers (Nginx, Apache), Database-servers(Mysql, Postgresql,etc), Application sever: Django, Node.js
           -------------------
           |        OS       |
           -------------------
           |     Hardware    | -> CPU, RAM, STORAGE, NETWORKING-CARDS
           -------------------

--
### 2.3 Virtualization:
* Cloud providers use virtualization to divide one ***physical server*** into ***multiple virtual servers*** (called Virtual Machines or VMs). 
* Each VM acts as if it’s a separate machine, with its own *operating system* and resources.

#### 2.3.1 The Role of the Hypervisor
***A hypervisor allows a single physical server to be virtualized.***
* The hypervisor acts as a middleman between the hardware and the operating systems.
* It divides the physical server's resources (CPU, RAM, storage) into multiple virtual environments.
* The hypervisor allocates resources like CPU, RAM, and disk space to each VM.
   * Each VM gets its own slice of the server’s resources.
   * Resources are isolated so one VM doesn’t interfere with another.
   * **Example:**A server with 16 CPUs and 64 GB of RAM can be partitioned into:
                1. VM1: 4 CPUs, 16 GB RAM.
                2. VM2: 8 CPUs, 32 GB RAM.
                3. VM3: 4 CPUs, 16 GB RAM.
* Each virtual environment runs its own operating system, behaving as if it were a separate physical server.

* ##### Two Types of Hypervisors:
  1. **Bare-Metal Hypervisor**:
     * Runs directly on the hardware.
     * Examples: VMware ESXi, Microsoft Hyper-V, KVM (Linux Kernel-based Virtual Machine).
     * Use Case: Data centers hosting large-scale cloud services.

  2. **Hosted Hypervisor**:
     * Runs on top of an existing operating system.
     * Examples: VirtualBox, VMware Workstation.
     * Use Case: Developers running multiple test environments on a personal machine.

#### 2.3.2 The Role of Virtual Machines (VMs)
*  **NOTE : Each VM created by the hypervisor acts like an independent server.**
* **VM = *Virtual Hardware* + Operating System + Software Stack.**
* Each VM can run:
    * Its own OS (Linux, Windows, etc.).
    * Any combination of server software (web servers, database servers, etc.).
    * Applications specific to a workload.


* **This enables a single physical server to host multiple independent server software stacks simultaneously.**
#### 2.3.3 How VMs Fit into the Stack:
Here’s how the stack looks when you include hypervisors and VMs:

         ----------------------------------
         | Hardware: or [Physical Server] |   -> Physical CPU, RAM, storage, and networking resources.
         ----------------------------------
                       |
         ----------------------------------
         |        Hypervisor:             |   ->  Divides the hardware resources and creates multiple VMs.
         ----------------------------------    
                       |
         ----------------------------------
         |     Virtual Machines (VMs):    |   ->  Each VM act as separate computer
         ---------------------------------- 
                       |
         Each VM includes : 
                 ------------------------
                 | Virtualized hardware |    ->  CPU, RAM, etc., allocated by the hypervisor.
                 ------------------------
                 | Operating System:    |    ->  A separate OS for each VM.
                 ------------------------
                 | Server Software:     |    ->  Web servers, database servers, application servers.
                 ------------------------
                 |   Applications       |    -> The actual programs serving requests.
                 ------------------------













-----------------------------------------------------------------------------

3
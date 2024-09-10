# Fifth Documentation 

- Set up four instances on my EC2 spinning up Ubuntu servers

![1](pic/1.png)

- Renamed the instances for easy identification

![1](pic/2.png)

- Inputing the required Consul service specific ports to function correctly. Selecting the **Consul** instance, clicking on **Security** and selecting the **Security Group**

![1](pic/3.png)

- Click on **Edit inbound rules**

![1](pic/4.png)

- Click on **Add rules**

![1](pic/5.png)

- Edit **Port range** to desired port number

![1](pic/6.png)

- Select **0.0.0.0/0.** Security measures have been intentionally relaxed by opening SSH, HTTP, HTTPS, and Consul ports to all traffic (0.0.0.0) for rapid development and testing.

![1](pic/7.png)

>[!NOTE]
This configuration is highly insecure and should never be used in production environments. 

- Click on **Add rule** again

![1](pic/8.png)

- Chooose **Custom UDP** 

![1](pic/9.png)

- Enter the Port range and choose the CIDR blocks.

![1](pic/10.png)

- Repeat the process for the remaining port configurations.

![1](pic/11.png)

- Once completed, click on **Save rules**

![1](pic/12.png)

- SSH into the Consul server and install **Consul**

![1](pic/13.png)

- Confirm Consul installation by checking its version

![1](pic/14.png)

- To configure the Consul server, start by backing up the default configuration file **consul.hcl** by renaming it to **consul.hcl.back**

![1](pic/15.png)

- Generate an **Encrypted key**

![1](pic/16.png)

- Creating a new file named **consul.hcl** in the **/etc/consul.d** directory and adding my **Encrypted Key**

![1](pic/17.png)

- Starting the Consul server in the background

![1](pic/18.png)

- Checking the status of the Consul server

![1](pic/19.png)

- Visiting 54.152.148.66:8500 in order to access the Consul dashboard.

![1](pic/20.png)

# Setting Up My Backends Servers

- SSH into the backend servers

![1](pic/21.png)

- Install **NginX**

![1](pic/22.png)

- Installing Consul as an agent on the servers.

![1](pic/23.png)

- Verifying that Consul is installed properly

![1](pic/24.png)

- Rename the default file and create a new one by inputing my **Encrypted Key** and my **Consul Server's IP Address**

![1](pic/25.png)

- Verify the configurations

![1](pic/26.png)

- Starting the Consul agent 

![1](pic/27.png)

- To verify if everything is working correctly, visiting my  Consul UI. Once the backend listed in the UI as depicted below, it indicates that the backend has successfully registered itself with Consul.

![1](pic/28.png)

![1](pic/29.png)

![1](pic/30.png)

# Setting up My Load Balancer

- SSH into my load balancer and Update the package information and install unzip

![1](pic/31.png)

- Install **NginX**

![1](pic/32.png)

- Download the consul-template binary

![1](pic/33.png)

- To verify the installation of consul-template, check its version

![1](pic/34.png)

- Creating a file named **consul-template.hcl** in the **/etc/nginx/conf.d/ directory.** This configuration file is used by consul-template to specify details about the Consul server IP and the destination path where the processed load-balancer.conf file will be saved.

![1](pic/35.png)

- Deleting the default server configuration to disable it by running the following command

![1](pic/36.png)

- Restarting Nginx to apply the changes

![1](pic/37.png)

- Starting the Consul Template agent 

![1](pic/38.png)

- Upon completion, a **load-balancer.conf** file will be created with backend server information populated from the Consul service registry.

![1](pic/39.png)

- Accessing the load balancer IP on my web browser, it will display the custom HTML content from one of the backend servers. Upon refreshing the page, the load balancer will route my request to the other backend server, displaying its custom HTML content.

![1](pic/40.png)

![1](pic/41.png)

# Service Discovery Test

- Now that everything is set up and running, I can test the configuration by observing what happens when I stop one of my backend servers.

- Stopping **Nginx server** on one of the backends servers

![1](pic/42.png)

- Stopping one of the backend servers. The Consul server will monitor the health of each registered service. Once a backend server is stopped, Consul will detect the server's unavailability and mark it as unhealthy. The health check for that server will fail, and it will be removed from the load balancer's active pool of servers.

![1](pic/43.png)

# End of PROJECT 5

- THANK YOU
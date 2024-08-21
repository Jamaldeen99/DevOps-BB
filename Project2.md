# Creating my second documentation

- Launching my instance using Ubuntu AMI.

![1](img/1.png)

![1](img/2.png)

- Click on create new key pairs for secure connection to my instance

![1](img/3.png)

- Giving my key pair a name and clicking on **Create Key Pair**

![1](img/4.png)

- Selecting the **SSH, HTTP and HTTPS** access options and **Click on Launch Instance**

![1](img/5.png)

- Successfully initiated launch of instance; Click on **View all instances**

![1](img/6.png)

![1](img/7.png)

- Click on the **Created Instance**

![1](img/8.png)

- Click on **Connect**

![1](img/9.png)

- Copy the command under the **SSH Client** example 

![1](img/10.png)

- A terminal was open in the directory where my **.pem** file was downloaded and I pasted the command

![1](img/11.png)

- Installing Nginx and hosting my website

![1](img/12.png)

![1](img/13.png)

![1](img/14.png)

- Starting the Nginx server by using the start command, enable it to start on boot using the enable command and confirming if it is running using the status command

![1](img/15.png)

- Visiting my  instances IP address in a web browser to view the default Nginx startup page.

![1](img/16.png)

- Download my preferred website template from my preferred website by navigating to the website, locating the template I want. Click on **Inspect** by right clicking beside the **Download** botton.

![1](img/17.png)

- Click on the **Network** tab and **Download** afterwards

![1](img/18.png)

- Right click on the selected template name. Hover the curson to **Copy** and click on **Copy URL** 

![1](img/19.png)

- Execute the command to download and unzip my website files

![1](img/20.png)

- Download the second website and follow the same procedures as the first

![1](img/21.png)

![1](img/22.png)

![1](img/23.png)

- To make my website accessible via my domain name rather than the IP address, I set up a DNS record. I did this by buying my domain from Namecheap and then moving hosting to AWS Route 53, where I set up an A record.

![1](img/33.png)

- Restart my nginx server by running the sudo systemctl restart nginx command. Afterwards, went to my domain name in a web browser to verify that my website is accessible.

![1](img/34.png)

![1](img/35.png)

![1](img/36.png)

- Installed certbot in order to generate a secure connection to my website.

![1](img/37.png)

![1](img/38.png)

![1](img/39.png)

![1](img/40.png)

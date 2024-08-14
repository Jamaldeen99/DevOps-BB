# My name is Jamaldeen

Creating my first documentation

- Launching my instance using Ubuntu AMI

![1](imgs/1.png)

![1](imgs/2.png)

- Click on create new key pairs for secure connection to my instance

![1](imgs/3.png)

- Giving my key pair a name and clicking on **Create Key Pair**

![1](imgs/4.png)

- Selecting the **SSH, HTTP and HTTPS** access options and **Click on Launch Instance**

![1](imgs/5.png)

- Click on **View all instances**

![1](imgs/6.png)

- Click on the **Created Instance**

![1](imgs/7.png)

- Click on **Connect**

![1](imgs/8.png)

- Copy the command under the **SSH Client** example 

![1](imgs/9.png)

- A terminal was open in the directory where my **.pem** file was downloaded and I pasted the command

![1](imgs/10.png)

- I return to my AWS console to create and assign an Elastic IP

![1](imgs/11.png)

![1](imgs/12.png)

- Click on **Allocate Elastic IP Address**

![1](imgs/13.png)

- Keep the settings unchancged and click on **Allocate**

![1](imgs/14.png)

- Proceed to **Associate this Elastic IP Address** with my running instance

![1](imgs/15.png)

- Process to select the instance to be associated with the Elastic IP Address and click on **Associate**

![1](imgs/16.png)

> [!NOTE]
The IP Address of my instance will have been updated to the Elastic IP associated with it. Copy the new command and paste it in my terminal.

![1](imgs/17.png)

- NginX was installed using commands on the terminal

- Nginx server was stared using three different commands

![1](imgs/18.png)

- A return to the EC2 Dashboard to copy the **Public IPv4 Address**

![1](imgs/19.png)

Paste my instace **Public IPv4 Address** on a web browser to view the default **Nginx Startup Page**

![1](imgs/20.png)

- A visit to **Tooplate** to obtain a website template

![1](imgs/21.png)

- After careful selection, I right click beside the the download button and click on **Inspect**

![1](imgs/22.png)

- Click on the **Network** tab

![1](imgs/23.png)

- Click on the **Download** button

![1](imgs/24.png)

- Hover the mouse to the file that has **.zip** right click and hover the **Copy** icon to show the **copy URL**

![1](imgs/25.png)

![1](imgs/26.png)

- run this command sudo curl -o /var/www/html/2136_kool_form_pack.zip https://www.tooplate.com/zip-templates/2136_kool_form_pack.zip

![1](imgs/27.png)

- To install the unzip file; run the following command sudo apt install unzip

- Navigate to the web server directory by running the following command: cd /var/www/html

![1](imgs/28.png)

- Unzip the contents of your website by running sudo unzip 2136_kool_form_pack.zip

![1](imgs/29.png)

- Update your nginx configuration by running the command sudo nano /etc/nginx/sites-available/default. Then, edit the root directive within your server block to point to the directory where your downloaded website content is stored.

![1](imgs/30.png)

- Restart Nginx to apply the changes by running: sudo systemctl restart nginx

- Open a web browser and go to your Public IPv4 address/Elastic IP address to confirm that your website is working as expected.

![1](imgs/31.png)

- Creating a Record!

- Go to namecheap list and select the icon bar

![1](imgs/32.png)

-Click on **Manage** icon

![1](imgs/33.png)

- Return to AWS Console and search for **Route53**

![1](imgs/34.png)

- Click on **Get Started**

![1](imgs/35.png)

- Select Create hosted zones and click on Get started.

![1](imgs/36.png)

- Enter the **Domain name**, choose **Public hosted zone** and then click on **Create hosted zone**.

![1](imgs/37.png)

![1](imgs/38.png)

n- Select the created hosted zone and copy the assigned Values.

![1](imgs/41.png)

- Go back to your domain registrar and select **Custom DNS** within the NAMESERVERS section. Paste the values you copied from **Route 53** into the appropriate fields, then click the **Checkmark Symbol** to save the changes.

![1](imgs/40.png)

- Head back to your AWS console and click on **Create record**

![1](imgs/41.png)

- Paste your **Elastic IP Address** and then click on **Create records**.

![1](imgs/42.png)

- My A record has been successfully created.

![1](imgs/43.png)

- Click on **Create record** again, to create the record for your sub domain. Input the **Record name(www)**, paste the **IP address**, and then click on **Create Records**.

![1](imgs/44.png)

- Restart the nginx server by running the **sudo systemctl restart nginx** command. Go to your domain name in a web browser to verify that your website is accessible.

![1](imgs/45.png)

- Installing certbot 

![1](imgs/46.png)

![1](imgs/47.png)

![1](imgs/48.png)

- Visit https://pantherapookie.xyz to view my amazing and secure website.

![1](imgs/49.png)

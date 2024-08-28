# Creating My Third Documentation

- Setting up three instances on my AWS account

![1](im/1.png)

![1](im/2.png)

![1](im/3.png)

![1](im/4.png)

![1](im/5.png)

![1](im/6.png)

![1](im/7.png)

![1](im/8.png)

![1](im/9.png)

![1](im/10.png)

![1](im/11.png)

![1](im/12.png)

![1](im/13.png)

![1](im/14.png)

![1](im/15.png)

- Installing NginX and setting up my website

![1](im/16.png)

![1](im/17.png)

![1](im/18.png)

![1](im/19.png)

![1](im/20.png)

![1](im/21.png)

![1](im/22.png)

![1](im/23.png)

- To set up my website's configuration by creating a new file in the Nginx sites-available directory to point to the directory where your downloaded website content is stored.. 

![1](im/24.png)

- Creating a symbolic link for both websites

![1](im/25.png)

- Running the **sudo nginx -t** command to check the syntax of the Nginx configuration file, and when successful run the **sudo systemctl restart nginx** command.

![1](im/26.png)

- Repeating the process for the second website

![1](im/27.png)

![1](im/28.png)

>[!NOTE]
On my first and second server, ran sudo rm /etc/nginx/sites-enabled/default. This will delete the default site-enabled folders and enable Nginx to serve content from my specified website directories.

![1](im/29.png)

- Checking both IP addresses to confirm my website is up and running.

![1](im/30.png)

![1](im/31.png)

- Configuring my Load Balancer

![1](im/32.png)

![1](im/33.png)

![1](im/34.png)

- Creating A Record

![1](im/49.png)

- Installing Certbot

![1](im/50.png)

- Checking my domain

![1](im/51.png)

![1](im/52.png)

- THANK YOU

**My Fourth Documention**

# **This Project involves setting up a WordPress websit using the LAMP Stack.**

1. Spinning up an Ubuntu server on the AWS Terminal.

![1](images/1.png)

- An inbound rule was set for MYSQL in my security group by Clicking on Security and selecting the Security group

![1](images/2.png)

- Click on **Edit inbound rule**

![1](images/3.png)

- Click on **Add rule**

![1](images/4.png)

- Click on **Custom TCP** and select **MySQL/Aurora**

![1](images/5.png)

- Inputing my **IP Address** and clicking on **save rules**

![1](images/6.png)

- Ran my **SSH** command on my terminal and installing my **Apache**

![1](images/7.png)

- Enabling **Apache** to start on boot and confirmining it **status**

![1](images/8.png)

- Checking if my server is running and accessible both locally and from the Internet using the **IP Address**

![1](images/9.png)

![1](images/10.png)

- Installing **MySQL** on my terminal

![1](images/11.png)

- Setting password for my root user

![1](images/12.png)

- Starting the interactive script setting my password validation policy level.

![1](images/13.png)

![1](images/14.png)

- Enabling **MySQL** to start on boot and confirming it status

![1](images/15.png)

- Installing **PHP** along with required extensions

![1](images/16.png)

![1](images/17.png)

- Confirming the downloaded PHP version by running php -v

![1](images/18.png)

- Creating a virtual host for my Website using Apache

![1](images/19.png)

- Creating and opening a new configuration file in Apache's sites-available directory

![1](images/20.png)

- Ran the ls command **sudo ls /etc/apache2/sites-available** to show the new file in the sites-available directory.

![1](images/21.png)

- Enabling the new virtual host using the a2ensite command

![1](images/22.png)

- Disabling Apache's default website

![1](images/23.png)

- Ensuring my configuration file doesn’t contain syntax errors, a **Syntax OK** message should pop up

![1](images/24.png)

- Reload Apache

>[!NOTE]
My new website is now active, but the web root /var/www/projectlamp is still empty. Let's create an index.html file in that location to test that the virtual host works as expected.

- Using the following command: sudo echo **'Hello LAMP from Panthera' > /var/www/projectlamp/index.html** inorder to create an index.html file with content.

![1](images/25.png)

- Visiting my IP Address on the web browser

![1](images/26.png)

- Removing the index.html file

![1](images/27.png)

- Enabling PHP on the website

![1](images/28.png)

- Reloading Apache for the changes to take effect. Now, Apache will prioritize index.php over index.html when both files exist in the same directory.

![1](images/29.png)

- Creating a new file named index.php inside your custom web root folder

![1](images/30.png)

- Reloading my web browser after saving

![1](images/31.png)

- Installing WordPress

![1](images/32.png)

- Extracting the files from the downloaded WordPress archive

![1](images/33.png)

- Running the command ls -l to confirm the existence of the wordpress directory in the current location

![1](images/34.png)

- Checking the user running your web server

![1](images/35.png)

- Granting ownership of the WordPress directory and its files to the web server user **(www-data)**

![1](images/36.png)

- Creating a Database For Wordpress: Login in with previously set password when prompted

![1](images/37.png)

- To create a separate database named wp_db for WordPress to manage

![1](images/38.png)

- To access the new database, I create a MySQL user account 

![1](images/39.png)

- Granting all priviledges and flushing priviledges 

![1](images/40.png)

- exit

![1](images/41.png)

- Granting executable permissions recursively (-R) to the wordpress folder

![1](images/42.png)

- Change into the **WordPress** directory

![1](images/43.png)

- Configuring Wordpress

![1](images/44.png)

![1](images/45.png)

![1](images/46.png)

![1](images/47.png)

- Visiting **http://98.81.97.211:80/wordpress/** on my web browser to access the WordPress setup wizard where I can finalize the installation process.

![1](images/48.png)

- Enter the required information and click on **Install WordPress**

![1](images/49.png)

- WordPress has been successfully installed. Login in to access WordPress

![1](images/50.png)

- Upon login in, WordPress dashboard page pops up

![1](images/51.png)

- A return to AWS Console inorder to make my website accessible via my domain name rather than the IP address

![1](images/52.png)

![1](images/53.png)

![1](images/54.png)

![1](images/55.png)

![1](images/56.png)

- Updating my Apache configuration file in the sites-available directory to point to my domain name

![1](images/57.png)

- Updating my wp-config.php file with DNS settings

![1](images/58.png)

- A return to my browser to load the page using my domain name

![1](images/59.png)

- Login in to my WordPress admin portal

![1](images/60.png)

![1](images/61.png)

- Installing certbot and Requesting For an SSL/TLS Certificate

![1](images/62.png)

![1](images/63.png)

![1](images/64.png)

![1](images/66.png)

![1](images/65.png)

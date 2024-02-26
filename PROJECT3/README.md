# LAMP STACK IMPLEMENTATION

A software stack is a set of layered tools, libraries, programming languages, and technologies used for building, managing, and running an application. 
The stack consists of software components that support the application in different ways, such as visual presentation, database, networking, and security.

A LAMP stack is a bundle of four different software technologies that developers use to build websites and web applications.
 LAMP stacks are used by developers to create, host, and manage both static and dynamic web content. Many of the websites you visit on a daily basis today are powered by this widely used solution.
 LAMP is an acronym for the operating system, Linux; the web server, Apache; the database server, MySQL; and the programming language, PHP.

Since all four of these technologies are open source, anyone can use them for free and they are maintained by the community. 
 When combined, they offer a proven software suite for delivering web applications with great performance. Each element provides the stack with necessary capabilities

- Linux (The operating system):Linux is a free and open source operating system (OS) that was developed in the mid-1990s. It currently has a large global user base that spans several industries. 
One reason Linux is so popular is that, compared to certain other operating systems, it provides greater flexibility and configuration options.
 
- Apache (The web server): The Apache web server processes requests and delivers web content using HTTP making the application available to anybody within the public domain via a straightforward web URL. A significant portion of the websites that are currently accessible on the internet are powered by Apache, a feature-rich, mature server that is developed and maintained by an open community. 

- MySQL (The database):  MySQL is an open source relational database management system for storing application data. The LAMP model uses MySQL for storing, managing, and querying information in relational databases. SQL is a great choice if you are dealing with a business domain that is well structured, and you want to translate that structure into the backend. For example, developers store application data, such as customer records, sales, and inventories. When a user searches for information, the web server queries the stored data in MySQL. Query refers to special instructions for manipulating data in a relational database with the SQL language.

- PHP (The programming language): The PHP, which stands for PHP: Hypertext Preprocessor, is an open source scripting language that works with Apache to help you create dynamic web pages. A dynamic process involves information in software that constantly changes. Dynamic processes like extracting data from a database cannot be done with HTML. You can add PHP code to any part of a page that you want to be dynamic in order to provide this kind of functionality.  

Web developers embed the PHP programming language in HTML to show real-time or updated information on websites. They use PHP to allow the web server, database, and operating system to cohesively process requests from browsers.

 PHP is designed to be efficient. Given that you can write new code, hit refresh, and see the changes right away without having to compile it, it makes programming simpler and even a little more enjoyable. 

LAMP has a classic layered architecture, with Linux at the lowest level. The next layer is Apache and MySQL, followed by PHP. Although PHP is nominally at the top or presentation layer, the PHP component sits inside Apache.

Web applications use a LAMP stack to respond to requests from web browsers. The Apache web server and MySQL database run on the Linux operating system and communicate using PHP

## WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS

A web stack is the collection of software used for web development that incorporates, at a minimum, an operating system (OS), a programming language, database software and a web server. 

A web stack, also known as a web application stack, is a type of solution stack. It's a collection of software applications that performs a particular task. In this case, the task or purpose is to enable web development, that is, the development of websites and web applications.

## Documentation on the implementation of LAMP (LINUX,APACHE,MYSQL,PHP) on AWS

A LAMP stack implementation in AWS is used to create, host, and manage both static and dynamic web contents.

### INSTALLING APACHE AND UPDATING THE FIREWALL

Before installation, I authenticate my laptop to enable access to my server by running an ubuntu operating sysytem on my AWS account. 

#### PRECONDITIONS:

1. Set up an AWS account.

2. Connect to your EC2 instance. launch a new Ec2 instance of t2.microfamily with Ubuntu Server 20.04 LTS.

3. Install and open your selected terminal. Windows terminal was used for this project.

4. Securely store the generated downloaded pem file format in your laptop (for example, downloads folder).

#### CONNECTING WINDOWS TO EC2

1. Run the command on windows terminal to change directory eg: Downloads folder.

```Bash
cd downloads
```

![alt text](<images/cd downloads.png>)


2. In this working directory enter the command:

```Bash
 ssh -i <private-key-name>.pem ubuntu@<Public-IP-address>

```

![alt text](<images/Instance connection to terminal.png>)


This will establish connection between the two computers using the copied the `ssh` protocol to establish connectivity between computers.

#### INSTALLING APACHE

Update a list of packages in package manager using the command:

```Bash
sudo apt update
```

![alt text](<sudo apt update.png>)


Use the command to install Apache2 package:

```Bash
sudo apt install apache2
```

![alt text](<install apache2.png>)

Verify that Apache2 is running as a Service in our operating System, use the command:

```Bash
sudo systemctl status apache2
```

Apache2 server is actively running

![alt text](<apache2 status.png>)

Open the TCP port 80 which is the default port on your instance to recieve traffic by our Web Server. 

![alt text](<Inbound edited rules.png>)

Check how to access the server locally on our Ubuntu shell by running the command:

```Bash
curl localhost
```

![alt text](<curl localhost.png>)

Test how Apache HTTP server responds to request from the internet. Open a web browser and access the url.

![alt text](<apache2 default.png>)

This means my web server is properly installed and accessible. 

### INSTALLING MySQL

The web server is up and running, there is need to install a Database Management System (DBMS) to store and manage data for your site in a relational database. 

Install MySQL on the ubuntu server using the command:

```Bash
sudo apt install mysql-server
```

![alt text](<mysql-server installation.png>)

Log in to the MySQL console using the command:

```Bash
sudo mysql
```

I am connected to the MySQL server as the administrative database user root, which is inferred by the use of sudo when running this command. 

![alt text](<sudo mysql.png>)

A security script that comes pre-installed with MySQL is recommended.  

This script removes some insecure default settings and lockdown access to the database system.

Set a password for the root user, using mysql_native_password as default authentication method. The password was defined as the command below:

```Bash
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
```
Exit the MySQL shell with:

```Bash
mysql> exit
```

![alt text](<default authetication method.png>)

Commence the interactive script by running the command:

```Bash
sudo mysql_secure_installation
```

![alt text](<validate sql password.png>)

![alt text](<validate sql password contd.png>)

### INSTALLING PHP

At this point, Apache has been installed to serve your content and MySQL installed to store and manage your data. 

PHP is the component of our setup that will process code to display dynamic content to the end user. 

Additionally, the `php` package, you will need `php-mysql`, a PHP module that permits communication of PHP with the MySQL-based databases. 

You will also need `libapache2-mod-php` to enable Apache to handle PHP files. Core PHP packages will automatically be installed as dependencies. 

Install these three packages at once, run the command:

```Bash
sudo apt install php libapache2-mod-php php-mysql
```

![alt text](<php installment.png>)

After installation, run the command to confirm the PHP version:

```Bash
php -v
```

![alt text](php-version.png)

The LAMP stack is fully installed and operational. 

### ENABLE PHP ON THE WEBSITE

Creating a Virtual Host for your Website using Apache.

Create the directory for `projectlamp` using `mkdir` command as follows:

```Bash
sudo mkdir /var/www/projectlamp
```

Assign ownership of the directory with the `$USER` environment varaible, which will reference your current system user using this command:

```Bash
sudo chown -R $USER:$USER /var/www/projectlamp
```

![alt text](<mkdir Projectlamp.png>)

Create and open a new configuration file in Apache's `site-available` directory using your preferred command-line editor. We will be using `vi` or `vim`. use the command 

```Bash
sudo vi /etc/apache2/sites-available/projectlamp.conf
```

![alt text](<apache2 (vi) sites-available.png>)

Use the `ls` command to show the new file in the sites-available directory.

```Bash
sudo ls /etc/apache2/sites-available
```

![alt text](<apache2 (vi) sites-available.png>)

Use a2ensite command to enable the new virtual host. Use the commmand:

```Bash
sudo a2ensite projectlamp
```

Disable the default website that comes installed with Apache. To disable Apache's default website use the dissite command:   

```Bash
sudo a2dissite 000-default
```

Reload Apache so that these changes take effect.

```Bash
sudo systemctl reload apache2
```

![alt text](<enable and disable server.png>)

The new website is active, but web root '/var/www/projectlamp' is still empty. Create an index.html file in that location to test the virtual host is working as expected. Use the command: 

```Bash
sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html
```
Run the command:

```Bash
sudo echo 'Hello LAMP from host' 'with public IP' $(hostname -i) > /var/www/projectlamp/index.html
```

![alt text](<Create index html.png>)

### CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE

The default 'DirectoryIndex' settings on Apache, a file named `index,html` will always precede over an `index.php` file. This is useful for setting up maintenance pages in PHP applications. 

To change this behaviour, use the command:

```Bash
sudo vim /etc/apache2/mods-enabled/dir.conf
```

Save and close the file, reload Apache to effect changes. Use the command:

```Bash
$ sudo systemctl reload apache2
```
Create a PHP script to test that PHP is installed correctly and configured to the server. 

Create a new file named `index.php` inside the custom web root folder. Run the command: 

```Bash
vim /var/www/projectlamp/index.php
```

This gives a blank file. Add the valid PHP code in a text inside the file. use the code below:

```Bash
<?php
phpinfo();
```
Save and close the file, refresh the web page for update.

![alt text](<php vim (enable php on website).png>)

 After checking for relevant information about your PHP server, it is best practice to remove the created file due to sensitive information about your PHP environment and Ubuntu server. 

Use the `rm` command:

```Bash
sudo rm /var/www/projectlamp/index.php
```
Refresh the page.

![alt text](<apache2 virtual host.png>)

The page is actively running.
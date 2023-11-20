# Apache and Remote on Ubuntu Server
This repository contains how to install apache and remote to a ubuntu server

# Things to be prepared
1. Ubuntu server that already installed SSH Open Server
2. Stable internet connection

# Setting up Apache on the Ubuntu server
1. Update the Ubuntu repository
   ```
   Sudo apt update
   ```
   
2. Install Apache
   ```
   Sudo apt install apache2
   ```
   
3. Activate the Apache using systemctl command
   ```
   Sudo systemctl start apache2
   ```
   
4. Make Apache run automatically at every boot
   ```
   Sudo systemctl enable apache2
   ```
   
5. Checking Apache status
   ```
   Sudo systemctl status apache2
   ```
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/fae630ab-88ed-483c-8567-96f87be18dd5)

6. Checking if the installation is successful on the web browser
   
   To ensure that Apache is running properly, attach the Ubuntu Server to a wifi hotspot or other network, then open a web browser on another device connected to that network and check the IP address of the Ubuntu Server
   (this can be done by using the hostname -I command)
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/51f05a8d-f107-48f1-9fbb-9d90d847409e)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/bfd41fa7-a84c-47dd-8ea5-91356eaed1bd)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/8d5b40e1-dddd-4f83-a582-3fda0767dd38)

# Remote Server on the Ubuntu Server
   Things that need to be prepared before installation:
1. Ubuntu server with SSH installed
2. A laptop running Windows with SSH and Putty installed
3. A smartphone that has installed Mobile SSH
4. A Linux desktop that has SSH installed
5. Every device listed above are connected to the same network with a stable internet connection.
6. Knowing the Ubuntu server's IP address (using the hostname -I command)
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/51f05a8d-f107-48f1-9fbb-9d90d847409e)

   Remote using CMD Windows:
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/7dafdfa0-50e0-435a-9896-8bb177cddeef)

   Remote using Putty:
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/578edc93-383d-4865-82b5-68e48844bee6)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/7295dfa9-5c55-409b-a9bb-d3d961b94750)

   Remote using Linux desktop (SSH):
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/98331d5b-f472-47ab-be5f-062f8020f151)

   Remote using Smartphone (Mobile SSH):
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/03e52529-e36c-4fdf-99d6-7a1fdddd67c8)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/d1d2bebc-5068-4fbb-a6bc-ed9978d2564d)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/63a165a9-32a0-468b-926c-d30cb10ee6ec)

# Wordpress Installation

# Things to be prepared
1. Ubuntu server that already installed Apache and Nano
2. Stable internet connection

# Setting up Wordpress on the Ubuntu server
1. Update the Ubuntu repository
   ```
   Sudo apt update
   ```

2. Install MySQL
   ```
   Sudo apt install mariadb-server mariadb-client
   ```

3. Install MySQL using secure instalation
   ```
   Sudo mysql_secure_installation
   ```
      
4. Install PHP
   ```
   Sudo apt install php php-mysql libapache2-mod-php
   ```

5. Check the PHP installation on a browser web

   Make a file "info.php" with the same coding as below
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/aedff3d6-fc2a-4cca-aabd-55b72c64489d)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/5c4a7425-0372-4e22-af13-c5528b762a3e)

   Then open a browser web on other device that connected to same network with the Ubuntu Server, type the IP address of Ubuntu Server and add "/info.php" at the end
   
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/a338158c-b2f9-4469-abb9-8fa10588d0cd)
   
   If the output from that web is similar as above, then the PHP installation is complete

7. Make a Wordress database, just follow all of the command one by one
   ```
   Mysql -u root -p
   ```
   ```
   CREATE DATABASE wordpress_db;
   ```
   ```
   CREATE USER 'wp_user'@'localhost' IDENTIFIED BY 'password';
   ```
   ```
   GRANT ALL ON wordpress_db.* TO 'wp_user'@'localhost' IDENTIFIED BY 'password';
   ```
   ```
   FLUSH PRIVILEGES;
   ```
   ```
   Exit;
   ```
8. Download and extract the latest version of Wordpress
   ```
   Sudo wget https://wordpress.org/latest.tar.gz
   ```
   ```
   Sudo tar -xvf latest.tar.gz
   ```

9. Change the Wordpress directory permission and add "uploads" directory inside
   ```
   Sudo chown -R www-data:www-data wordpress/
   ```
   ```
   Sudo chmod -R 755 wordpress/
   ```
   ```
   Sudo mkdir wordpress/wp-content/uploads
   ```
   ```
   Sudo chown -R www-data:www-data wordpress/wp-content/uploads/
   ```

10. Wordpress installation on a browser web
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/a6ee6315-aba9-42be-8969-db260254c8c4)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/36edf805-d8be-495d-b5e2-2cadc082da4f)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/01a70e1b-50c5-45e1-8a78-2e76f04cc95d)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/e9a392b6-78ce-48e2-8714-1708c233601e)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/4548f424-28fd-4c8b-95ac-bdbfff680148)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/37bffe3e-7c53-4964-8b7b-245688240e56)

# My Posts on Wordpress
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/dc98af8d-04d3-47a5-af9c-3b17d23888f2)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/6d7e9881-eeb4-49dc-8b76-1880045fd75a)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/26c5b5cd-1185-4d13-a289-d7b099964a3a)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/4c2c599b-f41e-4af5-afe1-89fe7abb2b39)
   ![image](https://github.com/AlanZanefate/Wordpress---Ubuntu-Server/assets/150001943/b86af4b3-0f88-4d36-a7c8-a2e4b0cf21b8)

  
 
 

      





   

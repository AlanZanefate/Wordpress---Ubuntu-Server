# Wordpress and Remote on Ubuntu Server
This repository contains how to make wordpress and how to remote to a ubuntu server

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



   

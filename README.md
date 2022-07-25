# Linux-VM
I'm following along on how to create a webserver using Virtual Box and Vagrant
https://www.tutorialworks.com/linux-vm-vagrant/


1. Download and installed Virtual Box and Vagrant
   - Virtual Box
    * Link: https://www.virtualbox.org/wiki/Downloads 
    I downloaded Windows hosts under VirtualBox platform packages
    I also downloaded the Oracle VM VirtualBox Extension Pack and had the VM install it
    
    - Vagrant
    * Link: https://www.vagrantup.com/downloads
    I downloaded the 686 version (just because)
 
 
 2. Setup my directory
    - Open terminal to create new directory and cd into it
    Terminal:
    mkdir myproject             // creates a new folder
    cd myproject                // to go into the new folder

    - I checked this site for the different boxes available - https://app.vagrantup.com/ubuntu 
    Terminal:
    vagrant init ubuntu/jammy64  // installs box
    vagrant up // after installation 
    
    Login to Virtual Machine (VM)
    Terminal:
    vagrant ssh


 3. Install the webserver
    - Installed Apache using Ubuntu's package manager
    Look at the list of packages installed
    Terminal:
    apt list --installed          // shows list of installation
    apt search apache             // lots of results but looking for Apache2 "Apache HTTP Server"
    apt update                    // to ensure everything is up to date (good practice)
    
    (To update or install packages, you need admin or root privileges) use sudo to access
    
    sudo apt update
    sudo apt install apache2      // It'll ask to confirm install, press y
    
    After install:
    dpkg -L apache2               // Shows all files installed onto system by apache2 package
    
  4.Check if Apache is running
    systemctl status apache2      // shows that it's running. use q to exit
    curl -v localhost:80          // test request. at the bottom is should say HTTP/1.1 200 OK. Apache is running
    
    
    
    
    
    
    
   

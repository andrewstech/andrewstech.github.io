---
title: HomeAssistant Advanced Install
date: '2021-08-09'
categories: []
tags:
  - HOMEASSISATNT
image_alt: lorem-ipsum
excerpt: lorem-ipsum
seo:
  title: ''
  description: ''
  robots: []
  extra: []
  type: stackbit_page_meta
layout: post
author: _data/team/person-8rvxgjy2b.json
---
# HomeAssistant Advanced Install&#xA;

Step 1 head to the [dietpi website](https://web.archive.org/web/20210123123637/https://dietpi.com/) and download the 64 bit Os for your device.

Step 2  flash dietpi to your SD card using the Raspberry pi imager

Step 3 (optional) edit the dietpi.txt file on SD Card.

Step 4 Connect to your router and identify the IP address of your raspberry Pi

Step 5 open a ssh connection to your Pi (on windows you can use Powershell or mac terminal). We are going to be using the root user so your command will look like ( ssh root@IP  ). The password is dietpi.

Step 6 Follow the on screen instructions till you reach a installation menu. Just select Install and yes. Once completed the Raspberry Pi will restart. If it doesn't then type reboot.

Step 7 Connect back to your RaspberryPi using the shh method then run the command (  sudo apt-get install python3 python3-dev python3-venv python3-pip libffi-dev libssl-dev libjpeg-dev zlib1g-dev autoconf build-essential libopenjp2-7 libtiff5 python ) If prompted press Y to continue.

Step 8  Run the command ( sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libsqlite3-dev libreadline-dev libffi-dev curl libbz2-dev ). Enter Y if prompted.

Step 9 Now we are about to compile Python3.8. Run the following commands. ( wget [https://www.python.org/ftp/python/3.8.2/Python-3.8.2.tar.xz](https://web.archive.org/web/20210123123637/https://www.python.org/ftp/python/3.8.2/Python-3.8.2.tar.xz) ) When the comand is complete we need to extract the tar file which the above command just downloaded to do so we must run the comand.  ( tar -xf Python-3.8.2.tar.xz ).  

Step 10 Navigate to the Python source directory and run the configure script we do this with the following commands ( cd Python-3.8.2 ) then ( ./configure --enable-optimizations ). This command may take a long time so its a good tea break.

Step 11 When the last command has completed then we must run another command. ( make -j 4 ) This will also take a long time.

Step 12 Now python3.8 has been compiled and can now be installed. simply run the following ( sudo make altinstall ) This can take around 2 minutes.

Step 13 Type ( cd ) to head to the root directory. We can now create our virtual environment for Homeassistant. Type the following ( python3.8 -m venv homeassistant ). Wait for the command to run then type ( cd homeassistant ). We are now in the folder which hosts the virtual environment. Run the command ( source bin/activate )

Step 14 Time to install Homeassistant run the comands ( python3 -m pip install wheel ) then ( python3 -m pip install homeassistant ).

Step 15 Homeassistant is now installed now to make it auto start. Close your ssh client then open it back up to start a new connection. Once connected type ( cd /etc/systemd/system/ )  You are now in the /system/ folder type ( wget [https://raw.githubusercontent.com/unofficial-skills/pi-scripts/master/home-assistant.service](https://web.archive.org/web/20210123123637/https://raw.githubusercontent.com/unofficial-skills/pi-scripts/master/home-assistant.service) ) This will download the Homeassistant auto start script. 

Step 16 Run the comand ( sudo systemctl --system daemon-reload ) this makes the system scan for startup scripts/services. Now run ( sudo systemctl enable home-assistant ). This will enable Homeassistant to auto boot. That's It you can now restart your pi and Homeassistant will start. Restart using the command ( reboot ). Homeassistant will take up-to 10 minuets to appear on the first boot. 

 

The config files are available at (  /root/.homeassistant/ ).

If you wish to find the status of Homeassistant then type in ssh ( sudo systemctl status home-assistant )

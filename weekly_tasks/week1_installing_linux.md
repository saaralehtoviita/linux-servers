# Week 1

This file consists of a report from the first weeks theme. The first part is a report about my process of installing Linux and the second part is a summary about the article What is Open Source Software and Why use OSS".

## Installing Linux

I am very new to Linux; recently I started my first job in the IT-field and I need Linux-skills there. I have managed to install Linux (DietPi) before on a Raspberry 5 computer. Now I am planning to install Debian on an old laptop and will try to report the steps below.

1. Download Debian

- Go to https://www.debian.org/download

2. Download Rufus

- Rufus is needed for making the usb-stick bootable
  1.  Go to rufus.ie/fi/ and select the version you want to download. I selected the first version.

  ![Downloading Rufus](../images_w1/rufus1.png) 2. Download Rufus on usb-stick

3. Flash Debian-image to usb-stick

![Flashing to a stick](../images_w1/rufus2.png)

![Flashing to a stick 2](../images_w1/rufus4.png)

4. Shut down laptop and insert usb-stick

5. Open laptop, and click on Esc

6. Choose the usb-stick from where installation should be done

![Choose correct usb-stick/device](../images_w1/usb.png)

7. Follow the installation process

- I pretty much chose the options that where suggested, probably this could have been done with more thought
- For example I don't know how partitioning should be done but since I knew that all on this computer could be deleted, I just chose the default options

![Partitioning 1](../images_w1/partition.png)
![Partitioning 2](../images_w1/partition1.png)

- I chose a minimal amount of software to be downloaded during the installation since my laptop is old and not very efficient
  - I had read that Xfce is a lighter Desktop enviroment than GNOME so I chose to use that

![Available software at installation](../images_w1/software_choosing.png)

8. Extra things after installation

- After the installation I was nervous and excited for if the installation process had gone throug but I could log in without problems and now have a working laptop with Linux! Here is how the desktop looks like:

![Sxfce Desktop](../images_w1/desktop.png)

- It took some time to find the screenshots that I took during the isntallation. Eventually I found them with some help from AI. All the folders under /home were empty and it turned out that I had to give my user sudo rights before I could even make a more advanced search for the screenshots.
- Checking the ip adress for the device: `hostname -I`
- Logging in from another computer using SSH: `saara@192.XXX.XXX.XX`
- Command for logging in as root: `su -`
- Giving sudo rights for my user: `usermod -aG sudo saara`
- Checking in what gropus my user is: `groups saara`
- Rebooting system after group update: `sudo reboot`
- AI suggested that I look for the screenshots like this: `sudo find /var/log/installer -type f | sort`
- Copy all the images from file: `sudo cp /var/log/installer/*.png ~/Pictures/`
- Change owner of file: `sudo chown saara:saara ~/Pictures/*.png`
- From the dcevice command center, for example Windows PowerShell, copy images from Linux-device to this device: `scp saara@192.168.100.14:/home/saara/Pictures/*.png "$env:USERPROFILE\Pictures\"`

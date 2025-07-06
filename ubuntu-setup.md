## HomeLab -- Linux install via VirtualBox --
**tools:** VirtualBox, Ubuntu 24.04, Windows Y40 machine

This repository documents the process of installing Ubuntu 24.04.2 LTS using VirtualBox onto my main Windows machine. The goal is to establish a clean and consistent Linux virtual environment for system administration practice and preparation for the LPI Linux Essentials certification.

--Purpose--
Set up a stable Ubuntu VM on both macOS (M1 MacBook Air) and Windows (Lenovo Y40) host machines.

Practice common Linux administration tasks in a homelab environment.

Reinforce concepts and hands-on experience aligned with the LPI Linux Essentials exam objectives.

--Prior Experience--
Ive previously used VirtualBox to run Kali Linux and earlier Ubuntu versions across macOS and Windows systems, using online tutorials and self-guided labs. This project documents that process as part of a structured homelab documentation.

#### Step 1: Download Required Software

Start by going to ubuntu.com and downloading the most recent Ubuntu Desktop ( in this case Ubuntu 24.04.2 ) LTS version for long term support via the downloads tab.

Youll need the VM to run the virtual disk, however I have already downloaded and installed VirtualBox from a previous lab.

In the event the program isnt already on the machine it can be downloaded from virtualbox.org. From the main page there will be a large download button which will take you to another screen that will allow you to pick the OS version your machine is running. Download, install, and run VirtualBox, follwing the installation instructions onscreen and accepting the defaults.

#### Step 2: Mount and Configure ISO

After the VM is installed run the VirtualBox program and in the top bar of the VirtualBox screen click 'New'

From there a 'Name and operating System' menu will appear with forms and drop-down menus. In the name form give it the name 'Ubuntu' followed by the version youll be using, in this case 'Ubuntu 24.04.2 LTS'.

Next select the amount of memory to give it. This will vary depending on the machine youre using, for instance I will be using around 4GB of memory but if you are unsure or are running a machine with less RAM it may be best to use the recommended defaults. 

Now the system is all built however nothing has been installed so if you were to try to run anything in this virtual computer you would get the OS with nothing inside. This is because you need the ISO disk that we downloaded, the ubuntu iso. To install it highlight the Ubuntu virtual computer and click the 'Storage' tab. 

A Settings menu will pop-up, click the storage tab and find the 'Devices' tab. Locate and select the small disk icon inside the 'Controller: IDE' tab, it will have 'Empty' next to the icon. After clicking the icon select the Ubuntu iso file we downloaded earlier from your Downloads folder.

#### Step 3: Update

Once that is all setup, within VirtualBox select the Start icon with the large green arrow next to it.

From there follow the install instructions in Ubuntu's GUI menus and run any updates required. If a terminal pops up from the initial start up select the 'Try/Install Ubuntu' option.

Follow setup instructions, selecting defaults/recommended settings, and update softwares as needed.

Select 'Restart Now' once updates are downloaded and installed.


#### Bonus: Software installation in the future

When maximizing the Ubuntu Window the program intially will not match the full screen size of your machine. This can be changed with a CLI command:

Select the 'Show Apps' in the bottom left corner.
Select 'Terminal' program

enter the following command verbatim:

sudo apt install linux-headers-$(uname -r) build-essential dkms

Type and enter Y for any requests asked and enter password as necessary

Select Device in the screen menu bar of the VirtualBox window and select Insert Guest Additions CD Image'. A disk icon will appear, select it and allow it to Run. Then Restart Virtualbox.

## NOTE: if issue persists click View in VirtualBox menu, click Virtual Screen, select 'Scale to.." and change percentage to match screen size


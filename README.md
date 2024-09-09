# Home Lab

This is my home lab project for monitoring and detection, as a way to increase my hands-on experience with different tools and OS.
My goal is to create a lab completely free with open-source resources so everyone can build their own without limitations, as showed below:

# Content:
- Hypervisor: VirtualBox
- Attack machine: Kali Linux
- Vulnerable machines: Windows 10

(this might be edited in the future)



## Host PC:
- Processor: Intel(R) Core(TM) i7-7700HQ CPU @ 2.80GHz   2.81 GHz
- Installed RAM: 16GB
- OS: Windows 10 Home 64-bits
- Graphics card: NVIDIA GeForce GTX 1050



## Downloading & Installing Oracle VM VirtualBox

For the purpose of this lab, I’ll be using Oracle VM VirtualBox as my hypervisor. It's an open-source software that you can download [here](https://www.virtualbox.org/)
It's a pretty straightforward installation process, but if you want step-by-step instructions follow this video: https://www.youtube.com/watch?v=kku0fVfksrk

*DISCLAIMER*: When creating the VMs for your home lab, please keep in mind your machine's resources when allocating space for each one. If you overdo it, there's a chance you'll ruin your host machine before having a chance to do anything with it.



## Installing and setting up Kali Linux

### Installation:
- Download the ISO file for Kali: https://www.kali.org/get-kali/#kali-installer-images
- Create a new VM in VirtualBox
- ![image](https://github.com/user-attachments/assets/9bb20ebc-70cf-4aaf-ba44-3803068480cc)
- After you name it and import the ISO image, go to Hardware and choose how much RAM you want (a good ratio is <= 25% of your system RAM)
- Choose Dynamically Allocated (if possible)
- ![image](https://github.com/user-attachments/assets/c8477aa4-bf87-46c3-8390-d2f4ca7b1bbe)
- Choose how much hard drive space you want (between 20-25 GB is good)
- ![image](https://github.com/user-attachments/assets/34294623-71fc-42ba-8602-14acab85dd8f)
- Click Create


### Configuration:

For this section of the process, I've used the book "Linux Basics for Hackers" by OccupyTheWeb. I won't share the PDF file due to ethical reasons but I'll do a summary of the steps:
- Choose Graphic install
- ![image](https://github.com/user-attachments/assets/c06f0c14-804e-43b8-9104-90dde19d6577)
- Choose your hostname for the system
- ![image](https://github.com/user-attachments/assets/369f67ac-959b-45b4-bb76-9fcb040737cb)
- Define your root credentials
- Choose your timezone and languages as you prefer
- Choose Guided - use entire disk
- Select All files in one partition
- Select Finish partitioning and write changes to disk and select Yes afterwards
- Network mirror isn't required so click No
- Select Yes to install GRUB boot loader
  - Enter device manually and select the drive
- Login as root and you're done!




## Installing and setting up Windows 10

### Installation:
- Start by downloading the Media Creation Tool (https://www.microsoft.com/en-ca/software-download/windows10)
- Select Yes and then Accept on the agreements page
- Choose the option Create installation media
- Customize the settings as your prefer
- Choose the option ISO file
- Create a Windows VM and import the downloaded ISO file
- (I chose the skip unattended installation)

This part of the proccess is dependend on your host machine's resources, please be mindful of that when following the steps

- Base Memory: 2048 MB
- 1 CPU
- Disk size: 50 GB
- Click Next and then Finish


### Configuration:
- Start the machine and click I don't have a product key
- Select Windows 10 Pro (or other OS you've downloaded)
- Accept license terms
- Custom installation (personal preference)
- Click Next and wait for it to complete installing



## Virtual Machines' Network Configuration

Disclaimer: the network configuration will change depending on what's your final goal for the homelab, testing tools and monitoring doesn't require the same specifications as malware analysis. Either way, take a screenshot of your different VM's before proceeding to have a secure baseline in case something breaks or gets infected.
As a personal preference, I've set up my VMs in an Internal Network without Internet access:

- Go to setting on the Windows machine and select Network
- Choose Internal Network and name it
- On the Kali machine, repeat the 1st step and choose the network you've named

- Start your Windows machine and righ-click on the globe icon
- Select Open Network and Internet settings
- Select Change adapter options
- Righ-click on Ethernet and choose Properties
- Click on IPv4 and choose Properties
- Assign a static IP of your choice

- Start your Kali machine amd righ-click on the network icon
- Select Edit Connections
- Click on wired connection and then Settings
- Choose IPv4 settings and change the method to Manual
- Assign a static IP of your choice (make sure it's withing the same network as the Windows machine)
- Ping the machines to ensure connectivity

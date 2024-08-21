# Home Lab

This is my home lab project for monitoring and detection, as a way to increase my hands-on experience with different tools and OS.
My goal is to create a lab completely free with open-source resources so everyone can build their own without limitations, as showed below:

# Content:
- Hypervisor: VirtualBox
- Attack machine: Kali Linux
- Vulnerable machines: Ubuntu and Windows 10
- Firewall: PfSense

(this will be edited during the process)



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
- 

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



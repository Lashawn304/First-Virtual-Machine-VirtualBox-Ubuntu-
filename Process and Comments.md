# #Project: Local Linux Workstation Setup via VirtualBox/Ubuntu ## 
📝 Overview

	The goal of this project  was to set up a secure isolated Linux environment using ubuntu for future projects.

🛠️ Environment & Tools

•	Host hardware & operating system
o	Lenovo IdeaPad 5
o	Windows 11Home
•	Hypervisor
o	Oracle VM VirtualBox (v7.x)
•	VM operating system
o	Ubuntu Server 24.04 LTS (64-bit)
•	Hardware Allocation
o	8 cpu cores
o	8GB
o	100GB virtual hard disk

🪜Steps

1.	Download and install Environment and Tools
a.	Download and install Oracle Virtualbox
b.	Download Ubuntu Server 24.04 LTS (64-bit) and store in 
i.	Preferably store the .ios file in a searchable folder 
2.	Virtual Machine Configuration
a.	Create a new VM in Virtualbox
b.	VM name and operating system
i.	Create VM name
ii.	Confirm folder location
iii.	Select Linux OS
iv.	Select Ubuntu distribution
v.	Select Ubuntu (64-bit)
vi.	(Optional) upload ISO image 
c.	VM hardware specification
i.	Base Memory (RAM) is set to 8GB
ii.	CPUs is set to 8
iii.	Set 100 GB of disk space (non-allocated)
d.	Select Finish and navigate to the new VM’s settings/storage devices
i.	Under controller, select the empty optical disk and attach it to the path of the Ubuntu .ios file and close
3.	Running the VM
a.	Run/Start the VM and wait for it load
b.	Select try install Ubuntu wait for it to install
c.	Configure Ubuntu settings to your liking 
4.	Explore your new VM

⚠️ Challenges, Troubleshooting

	VM failed to boot

	You have to navigate to the VirtualBox storage settings, selected the empty optical drive, and properly attached the Ubuntu Server .iso file to the controller.

	VM became unresponsive with a black screen during the installation

Investigate the logs, which confirmed “flatlining” and unresponsive due to hardware virtualization conflicts


Confirm that the VM is configured to Linux OS and Ubuntu Distribution

Close the VM and allocate more CPUs, base memory, and/or storage space

 Extreme lag and unresponsiveness when booting up or installing, indicated by the small turtle icon

Identify if Windows was running in a “Hyper-V” or fallback mode, which forced your VM into a slow emulation

Navigate to windows hyper platform by typing “Turn windows features on or off” in Windows home search

Navigate to Administrator Command Prompt by searching it in the Window’s home search and executing “bcdedit /set hypervisorlaunchtype off” to disable the Windows hypervisor layer. Then, resetting the laptop

Navigate to Windows security and toggled off Memory Integrity, which acts as a hidden hypervisor lock on Windows Home editions.

	Third-party Interference (Bitdefender)

Bitdefender's protection settings and manually added the VirtualBox installation directory (and its associated .exe processes) to the Exception List to prevent the antivirus from obstructing your hypervisor.

	Wait 15-1hour (10-15vminutes average) 

The host’s hardware is not as strong and will have to wait when installing Ubuntu.

👀Hindsight

•	Should’ve looked into other VMs such as VMware Workstation, Microsoft Hyper-V (only on windows 11 pro, enterprise, and education editions), and WSL 2 (primarily for command line projects)

•	Researching my hardware’s capabilities with VMs and specific ones I plan to use

•	Its good to watch YouTube installation tutorials beforehand

•	Having an AI chat bot to navigate common troubleshooting

⏭️ Next Steps

	I plan to use this setup as a sandbox for real-world situations, challenging myself to create things from scratch.

💬Comments

This last section is basically a log of just me sharing my thoughts at this time. Yes, this journey has been difficult, but it is a stepping stone to something bigger.

I know this won't be the first or last machine I use. I honestly prefer VMware Workstation, mainly because it is highly suitable for Windows. Nevertheless, I am working with a $0 budget, and I will keep that in mind for this project.
For anyone else looking to begin their self-learning journey in computer science, cybersecurity, networking, or computer engineering: if you want to get a job working with computers or want to work remotely, you have to create projects. You have to show that you are able to handle real-world situations.

I do not have a master's or a bachelor's degree in computer science; I actually have a biology degree. I had to take smaller jobs in order to eventually find a stable one that allows me the time and resources for this type of hobby and learning. My goal is to put my degree to work by integrating biology with computer science—or at least the logistics of it.
What should we tackle? Ideas? Problems? If you come from a different background, you can apply your unique perspective to computer science to innovate new ideas or tackle old problems to make things more efficient.

Also, do not be ashamed of using LLMs, but remember: they are tools to assist you. If you do not use them as tools or assistants, you are not going to actually learn, apply, or create what you want. More importantly, the work you publish won't really be your own. Your name might be on it, but the work itself could only be recreated by someone else's hands. Do not let your skills dull. These models are here as tools to enhance and sharpen us. They are here to used by our existing skills toward the specific outcomes we want to achieve.
 



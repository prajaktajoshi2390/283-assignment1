# 283-assignment1
As part of assignment, the steps executed are as follows:
- Download and Install VMware Workstation
- Download the 64 bit Ubuntu ISO file
- Create VM using the ISO downloaded, and allocate 200GB of disc space
- Enable nested virtualization settings (settings-Processors-Check the box next to Virtualize Intel VT-x/EPT or AMD-V/RVI.)
- Run the newly created VM
- Open the terminal
- command - cat /proc/cpuinfo | more
  Output of above command will have 'vmx' in flags, indicating that the CPU has been setup properly
- command - git clone https://github.com/prajaktajoshi2390/283-assignment1.git
- Add cmpe283-1.c and Makefile into the folder
- command - sudo apt install vim
- command - vi cmpe283-1.c
- Update the code for all the MSRs (Check cmpe283-1.c for the code)
- command - :wq!
- command - make (To compile the module)
- command - insmod cmpe283-1.ko
- command - dmesg (To print the output logs)
- Verify that the logs are displayed indicating the VMX capabilities for all the MSRs
- Commit and Push the changes to the Git Repo
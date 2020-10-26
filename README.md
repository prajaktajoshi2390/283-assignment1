# 283-assignment1
Q1: For each member in your team, provide 1 paragraph detailing what parts of the lab that member
implemented / researched.

- This assignment is implemented by 2 members:
  -- Prajakta Joshi
  -- Umashankar Kumar
- Activities By Prajakta Joshi
  -- Done the setup required for the assignment
  -- Implemented code to read from various MSRs
- Activities By Umashankar Kumar
  -- Done the research for setting up the VMvare Workstation
  -- Researched on the list of Intel's SDM VMX Controls
- Both the team members discussed and found out the way to implement the code and work on documentation.


Q2: Describe in detail the steps you used to complete the assignment.

As part of assignment, the steps executed are as follows:
- Download and Install VMware Workstation
- Download the 64 bit Ubuntu ISO file
- Create VM using the ISO downloaded, and allocate 200GB of disc space, 2 processors at the time of VM creation
- Enable nested virtualization settings (settings-Processors-Check the box next to Virtualize Intel VT-x/EPT or AMD-V/RVI)
- Run the newly created VM
- Open the terminal inside VM
- command - cat /proc/cpuinfo | more
  -- Output of above command will have 'vmx' in flags, indicating that the CPU has been setup properly
- command - git clone https://github.com/prajaktajoshi2390/283-assignment1.git
  -- Get the clone of git repository in which you would like to commit the code
- Add cmpe283-1.c and Makefile into the folder
  -- These files are provided as a startup for this assignment
- command - sudo apt install vim
  -- This will allow you to execute vim specific commands on terminal
- command - vi cmpe283-1.c
  -- Open the cmpe283-1.c file
- Update the code for all the MSRs (Check cmpe283-1.c for the code)
- command - :wq!
  -- Save the changes
- command - make
  -- It will compile the module
- command - insmod cmpe283-1.ko
  -- This will install the updated module
- command - dmesg
  -- Print the output logs
- Verify that the logs are displayed indicating the VMX capabilities for all the MSRs
- After making any consecutive code changes, you need execute the command - sudo rmmod cmpe-283-1
- The screenshot of output logs is added to the doc file "283-assignment-1-output-screenshots.docx"
- Commit and Push the changes to the Git Repo
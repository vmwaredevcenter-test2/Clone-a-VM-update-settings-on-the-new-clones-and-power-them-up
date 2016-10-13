
README file for the CloneAndChangeVM.java sample code

This sample code shows how to clone a VM (repeatedly, if needed), change some settings 
on all of the new VM created, and then power up all the new VMs.

This sample assumes you are running vSphere version 5.5 or later.

How To Run

In order to run this sample code you must provide 6 arguments:
[1] The server name or IP address
[2] The user name to log in as
[3] The password to use
[4] The name of the virtual machine to clone
[5] The number of clones to make
[6] The base name of each new clone

You can run this sample code by downloading the zip file below, unzipping it and running a command
similar to the following:
java -cp vim25.jar com.vmware.scia.workflows.CloneAndChangeVM <ip_or_name> <user> <password> <vm_ip>
java -cp vim25.jar com.vmware.scia.workflows.CloneAndChangeVM 10.20.30.40 JoeUser 10.20.30.41

Output

You will see the output similar to the following when you run the sample:
Cloning VM dbserver1
Cloning VM dbserver2
Cloning VM dbserver3
Updating new VM vm-27
Updating new VM vm-28
Updating new VM vm-29
Powering up new VM vm-27
Powering up new VM vm-28
Powering up new VM vm-29

If powering up your new VMs fails, it may be that there is a problem with the base VM
that you are cloning.  You might want to go to the kb.vmware.com web site, and search 
for the error message you get, to see how to configure your base VM.  

For example, if you get an "Invalid memory setting: memory reservation (sched.mem.min) 
should be equal to memsize(512)" error, you will find this knowledge base article:
http://kb.vmware.com/kb/2002779

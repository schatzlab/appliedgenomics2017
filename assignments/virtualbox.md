## Development Environment
The standard development environment for this course is Lubuntu 16.04 LTS, which is a fast and lightweight operating system based on Linux (a unix variant) and Ubuntu.  We have created a packaged version of this that you will need to import as an "appliance" through VirtualBox (instructions below). 
 
In order to install and use our environment follow these steps on your laptop:

1. Install VirtualBox, or upgrade your version if you already have it installed.  VirtualBox is software that allows you to create and work on virtual devices as separate instances within your machine. You can download it here: https://www.virtualbox.org/
 
2. Download the 64-bit Lubuntu 16.04 Xenial Xerus appliance. Do not install the Lubuntu 16.10 Yakkety Yak appliance -- it is not working! Make sure to download the 64 bit version! (large file, so expect it to take a while): 
http://www.osboxes.org/lubuntu/ (2.7 GB file, up to 8 GB required)

3. Follow the directions here to import the virtual box:
https://blogs.oracle.com/oswald/entry/importing_a_vdi_in_virtualbox

   The key steps are (1) Name your Virtual Machine and Select the Operating System as 64 bit Ubuntu
   ![Name](https://raw.githubusercontent.com/schatzlab/appliedgenomics/master/assignments/virtualbox/NameVirtualMachine.png)

   (2) Set the memory size to 4GB (or as much RAM as is available)
   ![Memory](https://raw.githubusercontent.com/schatzlab/appliedgenomics/master/assignments/virtualbox/MemorySize.png)

   (3) Select the Lubuntu image as your virtual hard disk
   ![HardDrive](https://raw.githubusercontent.com/schatzlab/appliedgenomics/master/assignments/virtualbox/Hard%20Disk.png)

4. When the install finishes, you will have a virtual machine called "Lubuntu 16.04 LTS" showing in the left menu of your VirtualBox device manager.  

5. Double-click on this virtual machine to start it up (or single-click and then hit the "start" icon).  If you get an error message, read the details and follow the instructions to update as necessary.  (For example, you might have to install the Oracle VM Extension Pack from https://www.virtualbox.org/wiki/Downloads to get the USB controller to work.)

6. Once your Lubuntu machine boots, you'll be prompted to login.  The default username is "osboxes" and the default password is "osboxes.org"; feel free to create a new username or change the password

7. Explore your new machine-in-a-machine to see what software is already there, by clicking the left bottom start button.  Keep in mind that the files in your virtual environment can only be accessed from within that virtual environment, not from your usual laptop software.  So Lubuntu has a web browser, office-like apps, accessories, etc. The terminal can be accessed using the LXTerminal application in the "System Tools" menu.

8. Note that updated versions of this appliance may be posted at a later date. Hence it's probably a Bad Idea (tm) if you keep source code you're working on only in your virtual machine instance. We highly recommend using a service such as Dropbox to maintain your files in. (Start->Internet->Dropbox to install.)  This also helps in case your laptop catches fire or some other mishap occurs.

### Essential Packages

After booting the virtual machine, there are a number of essential packages that will be needed. Install them with the following commands (just accept the defaults when prompted):

```
$ sudo apt-get update
$ sudo apt-get install build-essential
$ sudo apt-get install dkms
$ sudo agp-get install default-jre
```

#### Guest Additions
You will want to install guest additions to get cool features like access to shared folders and shared clipboard, native screen resolutions, etc. Please follow the linked documentation for how to install those extensions.  These tools will make it easier to switch back and forth between your virtual box machine and your native laptop.

From the VirtualBox Devices menu, click "Install Guest Additions CD Image..."

Then run this at the terminal:

```
$ sudo /media/osboxes/VBOXADDITIONS_5.1.14_112924/VBoxLinuxAdditions.run
$ /sbin/shutdown -r now
```

### Fixing the Display
In case you boot up the appliance and get some weird-looking graphics instead of a nice login screen: Hit "Host+F1" once, then "Host+F7" once and everything should be good. In VirtualBox the "Host" key is "Right Ctrl" (on Windows/Linux) or "Left Command" on OS X. (If you're using a Mac, you may also have to push some funky key called "fn" (bottom left corner of your keyboard) to get F1/F7 to behave as they should. And if you have a Mac without function keys, well, you should figure out for yourself where those keys are now...)
 


#### Powering Down
Always use the "power button" in the bottom right corner of your Lubuntu desktop to shut down your machine safely - do not simply exit the window or VirtualBox.  Running Lubuntu through VirtualBox can be a bit of a power drain on your laptop, so be prepared with a power cord.  
 

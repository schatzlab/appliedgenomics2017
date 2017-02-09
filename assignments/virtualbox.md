## Setting up VirtualBox 

I'd like to avoid platform-related problems, so I strongly recommend that you install a virtual Linux environment which will essentially be a computer within your laptop/desktop. By using one consistent environment for the entire course we can avoid most of the boring problems and concentrate on the meat of the course instead. These instructions are based on a guide originally written by Peter Froehlich, with contributions by Scott Smith, Adam Teichert, Ben Mitchell and Joanne Selinski.

### 1. Install Virtual Box (estimated time: 5 min)

First you'll need software that allows you to install Linux without erasing your existing operating system in the process. Although there are a variety of possible virtualization options, we highly recommend using VirtualBox. You can download it directly from https://www.virtualbox.org/ and follow the installation instructions provided there. Once VirtualBox is installed, you'll be able to set up the Linux environment for the course.

### 2. Download the Lubuntu Linux ISO File (estimated time: 5 - 10 min)

Now that you have a virtual machine, you need to download the operating system to install on it. We highly recommend that you download the most recent long-term-support 32-bit (x86) version of Lubuntu from http://lubuntu.net/ for this course, regardless of whether you have a 32-bit or a 64-bit laptop. You need the 32-bit (x86) to match your VirtualBox configuration. Lubuntu is a light-weight version of Ubuntu that works great even on older hardware and in virtual machines. Check with me as to which version to download if you're not sure.

### 3. Create a Virtual Machine for Lubuntu (estimated time: 2 min)

Start Virtual Box and hit the "New" button to start the "New Virtual Machine Wizard" which will guide you through the creation of your virtual machine. Pick a relevant name for your machine ("AppliedGenomics"). Select "Linux" as your operating system and "Ubuntu" as your version. Select at least "1024 MB" as your memory size (provided your actual machine has that much memory). Create a new virtual VDI harddisk with a size of at least "8 GB" (provided your actual machine has that much disk space left). After a few more prompts you should be done and your shiny new virtual machine should appear in the list on the left side of the Virtual Box window.

### 4. Install Lubuntu (estimated time: 30 min - 1 hour)

Select your named virtual machine and hit the "Settings" button. Select the "Storage" tab and then select the "Empty" CD-ROM icon. Far to the right there will be another CD-ROM icon with the popup help "Set up the virtual CD drive"; click that, then select "Choose a virtual CD disk file". A file dialog will pop up in which you should select the ".iso" file you downloaded earlier in step 2. You should also select the "General" tab, followed by the "Advanced" tab on the right. This will allow you to enable copy/paste; set "Shared Clipboard" to bidirectional (note that there will be another step required later to make this work fully). Once you're done, hit "Okay" in the "Settings" window. Make sure that your named virtual machine is still selected and hit the "Start" button to boot it.

After you start the virtual machine, a number of warning messages may pop up that can usually be ignored safely. You should see a menu in which you can select the language you want to use for Lubuntu. You can change the language using the cursor keys and you'll make your selection by hitting the "Return" key. In the following we'll assume that you picked "English" as your language. In the next menu you should select "Try Lubuntu without Installing" to make sure that you configured the virtual machine correctly. Once the boot process finishes, you should have an empty Lubuntu desktop with a single icon "Install Lubuntu" in front of you. You can now play around with Lubuntu if you want, just remember that anything you change will not survive the next boot of your virtual machine. So eventually you must double-click the "Install Lubuntu" icon. You might just want to do this first and skip the trying-out step.

Select your preferred language (we'll assume English again) and hit "Continue". The keyboard or mouse might behave a little funny during this part, but you can use the arrow keys, tab, and enter if necessary to navigate. On the next screen select "Download updates while installing" as well as "Install this third-party software" and hit "Continue". On the next screen select "Erase disk and install Lubuntu" and hit "Continue". On the next screen your virtual "VBOX HARDDISK" should already be selected; if that's not the case, select the "VBOX HARDDISK" before hitting "Install Now" to start the actual installation process.

While the installation formats your disk and copies files, a number of additional screens will need filling out. First select your location, probably "New York" since Baltimore is not an option. Then select your keyboard layout, probably "English (US)" but that depends on your actual keyboard more than anything else. Next fill in your name and the name for the virtual machine itself (the default is okay). We recommend that you pick the first part of your JHU email address as your user name, but once again this is really up to you. Pick a decent password that you won't forget! Since you will probably be the only person working on your virtual machine, select "Login automatically" but do NOT select "Encrypt my home folder" as that could be trouble later and hit "Continue" one last time. Now you can sit back and watch the installation progress. Once the installation finishes, hit "Restart Now". Once the message "Please remove the installation media..." pops up, simply hit "Return" and watch your virtual machine reset and then boot into your shiny new Lubuntu system. If the "Restart Now" doesn't finish properly, then simply close the Lubuntu window and then click the "Start" button in VirtualBox to restart your new virtual machine.

The first thing that will probably happen is that the "Update Manager" wants you to update your Lubuntu system to the latest version of various applications. Simply click the "Install Updates" button and authenticate with your password, then watch the updates fly by as they are installed. Most likely you will need to restart again after all the updates, simply hit "Restart Now" if that's the case. Once this last reboot finishes, you have a completely up-to-date Lubuntu system to play with. Enjoy!

### 5. Installing Additional Tools and Applications (estimated time: 5 min)

There are a few tools that you will want to add to Lubuntu right away. As the semester progresses, you'll start adding more and more tools and applications to Lubuntu, so we'll briefly explain the process for installing software here. The actual packages to install are listed below. If you find a cool package not yet listed, feel free to post a comment on the course's Piazza site to recommend it.

Most Unix systems, Lubuntu included, come with a package management system. This system handles installation, updating, and un-installation of software; you are likely familiar with the idea, since GooglePlay, the AppStore, and Steam are all modeled after Unix package management systems.

To install a new package click on the "Lubuntu" icon in the lower left corner of the screen, go to "System Tools" and start the "Synaptic Package Manager". You'll have to authenticate with your password again before you can continue. Click on the "Search" button at the top and enter the name of the package you want to install as your query. Once the search finishes look through the list of results to find the actual package. Once you have found the package, click on the box to the left of it and select "Mark for installation". At this point a window might pop up telling you what other packages need to be installed as well in order to install the package you want. Simply hit "Okay" to confirm. Then hit the "Apply" button at the top, which will pop up another confirmation dialog where you again hit "Apply" and then you can watch the packages get installed. Once the installation finishes, confirm again with the "Close" button. Then close the "Synaptic Package Manager" itself. Easy!

### 6. Packages to Install (estimated time: 5 min)

Here are some packages that will be useful regardless of the course/programming language you will be using. Check with your course instructor for language specific packages you will need to install.

virtualbox-guest-utils, virtualbox-guest-x11, virtualbox-guest-dkms - You should install these packages first thing, and then re-boot your virtual machine. These packages provide a better interface between your "host" operating system, and the "guest" linux operating system running on the virtual machine. They will allow you to resize your virtual desktop, and offer better cursor integration and more responsive input handling. Once installed, go to "Preferences -> Monitor Settings" within your virtual machine to change the desktop resolution. These packages will also let you copy/paste from non-virtual-machine programs, as long as you have your VirtualBox Settings configured to allow "bidirectional" copy/paste (under the "Advanced" tab of the "General" settings).

emacs - a very popular editor
vim - another very popular editor
vim-gtk - a GUI version of vim with a bunch of menus, easier to use, better integration with other GUI windows
git - version control program you may be using

There is also a command-line interface to the package management system, called apt-get. To install a package using it, open a terminal and type sudo apt-get install packagename (substituting the actual name of the package you want to install). It can be useful for installing multiple packages at once; for instance, to install all the recommended packages above, simply type or copy/paste the following into a terminal (though unfortunately, copy/paste won't work until you install the virtualbox-guest packages and enable it in your virtualbox settings):

```
$ sudo apt-get install virtualbox-guest-utils virtualbox-guest-x11 virtualbox-guest-dkms vim vim-gtk emacs git
```

### 7. Install VirtualBox Extension Pack (estimated time: 5 min)

You can only install the Extension pack after the operating system is install, but this will improve the performance of your virtual machine and make it easier to do things like resize the display. Download the extension pack from here: https://www.virtualbox.org/wiki/Downloads

### Using Lubuntu after installing

When you restart your virtual box, you will need to reopen a terminal session to use your Lubuntu installation. In the lower left corner of the virtual box open the main menu -> SystemTools -> LXTerminal (or Accessories on older versions). Now you're back in your linux environment and can code away. You can also access a nice version of emacs through Accessories or the Programming menu options. It's good to work with several open windows - one for editting, one for compiling and running.

### Keeping Lubuntu Current

Lubuntu's Update Manager will pop up from time to time when new versions of various installed packages are available. Unless you are working on something really really important you should go ahead and install the updates to keep your system current. However, there is always a risk that an update will break things. That has never happened to me, but there's no guarantee that it won't happen in the future. So don't update things the day before an assignment is due, unless of course you cannot finish your assignment without the update. The sole exception to this is an entirely new Lubuntu release: Do not not NOT switch to a new release, stay with your current package updates for the entire course.

### Shutting Down Properly

It's a really bad idea to quit your virtual Lubuntu machine by just closing the window or selecting "Quit" in the Virtual Box menu: That essentially means ripping the virtual power cord out of the virtual power plug, and hopefully you wouldn't do that to a real computer either. First type "exit" to close your terminal window. Then always use the "power button" in the lower right corner of the Lubuntu desktop to properly shutdown, otherwise you risk losing files or destroying your virtual machine entirely.


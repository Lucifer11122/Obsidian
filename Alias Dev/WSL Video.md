wsl --install
Wsl --list --online
Wsl --install -d ubuntu/kali-linux
Wsl --list --verbose(wsl -l -v)
Setup username and password(restart terminal)
Wsl --terminate distro-name
Start a particuar distro (wsl -d Kali-linux)
Install gimp, firefox,git,vim,neofetch,wget
Tell about python3
Configure vs code

***Ubuntu GUI***
1. Sudo apt install xfce4 xfce4-goodies -y(desktop environment)
2. sudo apt install xrdp -y
3. sudo systemctl enable xrdp
4. sudo adduser $(whoami) ssl-cert
5. echo "**startxfce4**" > ~/.xsession
6. Remote desktop (mstsc)
7. Localhost 3389
***Kali***
sudo cat /etc/apt/source.list
deb http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware

# Script
***Intro***
Welcome to my channel Alias dev. If  you ever wanted to try using Linux but do not want to give up using windows then you only  have a few options you can either setup a virtual machine or dual boot windows and Linux. Now as you may know setting up a virtual machine or dual booting are really difficult and  time consuming. what if i tell you you can run a real Linux kernel from inside windows using the terminal and installing it takes about 5 minutes of your time  literally using 1 command and you can seamlessly access Linux files from windows and windows files from Linux, takes 1-2 seconds to boot and you can do mostly everything you will want to do in Linux while also being in the comfort of windows, well that's the topic of today's video windows subsystem for Linux or wsl for short. In this video i will show you how to setup a very popular Linux distro ubuntu using wsl and configure it for your basic development needs and i will also show you how you can get a full desktop environment of ubuntu.
***WSL Setup***
Before we hop into our terminals and install our first Linux distribution we have to make sure that we have the windows subsystem for Linux feature enabled in our system Now to do that open your windows search and look for "Turn windows feature on or off" open it and then scroll down at the very bottom. Here you can see a feature called windows subsystem for Linux we want to enable this feature so click the check box beside wsl and click ok. Now you will be prompted to restart your pc. After you have restarted your pc open up your windows terminal, i am using powershell but you can also use command prompt. Now that we have opened our terminal you will probably want to know what distros we can download using wsl in order to check all the distros that can be downloaded through wsl we will use the command wsl --list --online. As you can see these are  all the distros that we can install . In order to install any distro we will use the command wsl --install <distro-name> for this video we will install ubuntu so lets do it. As you can see ubuntu has started to download. it is going to take some time so lets comeback after its done. Now as you can see ubuntu is successfully downloaded and installed in our pc and we can launch ubuntu with the command wsl -d ubuntu, Here you can see we are prompted to enter our unix username this is the default username that the ubuntu will use for us. This is not linked to the windows user account by any means, but as you can see this has taken my windows user name by default. This is  in order to just streamline the experience you can keep it anything you like as you can see i will change it too. Next is the password for the user you will be needing to use this password whenever you will be doing some admin/ root level tasks with sudo. After we have successfully setup the username and password we have successfully setup ubuntu and we can start working on it,  however i recommend you restart your terminal at this point to refresh the terminal. After you have restarted your terminal if you go here to open a new shell tab you can see the ubuntu shell listed among PowerShell command prompt git bash you can launch ubuntu directly from here or with the command so lets open it. First thing we will want to do after opening ubuntu is updating the system with the command sudo apt update -y && sudo apt upgrade -y and then enter your password and it will update all the system packages files this process is also going to take some time depending on your internet speeds. Nice the updating is done  and we can get started on working on it. The first package we can install is neofetch. It is a command line system information tool that displays a summary of the system we are running  we are installing this to see that we are actually running  ubuntu on our windows terminal. Now when you heard running linux on windows terminal you might expected it will be limited to command line stuff like writing bash commands install some cli tools and maybe run python scripts but with wsl 2, thanks to a feature called wsl g we can run gui applications like you are on a native linux desktop what wslg does is that it provides a display server behind the scenes.  Lets install a gui application like a  browser for example. Our choice here is firefox but you have installed any other brower.  As you can see firefox is downloaded and installed lets open it.
Now let is configure vs code to run to run from here, if you have vs code installed in windows. In order to do that first we will have to open vs code in windows, now go to the extensions page and search for Remote development. This extension pack here will install everything you will need to open vs code from inside of the ubuntu terminal and access the windows files from the ubuntu. Now lets get back to your terminal and we can open vs code from here with the command code . and well as you can see vs code is now opened. Now this is running the windows native vs code but this is running on the ubuntu environment so it will use the linux file paths linux tools and linux compilers and settings. Yes you will have to install the compilers you will use in this environment even if you have them installed in windows as this is a separate environment from your windows so lets do it in order to install the gcc and g++ compilers for c and c++ you will need to use the command sudo apt install build-essential -y this command will install gcc g++ make and some other necessary tools and with that you have the gcc and g++ compilers downloaded on this environment lets quickly check if the installation was successful gcc --version g++ --version so this is code lets try to run a simple cpp code to see if everything is working as intended on this note let me tell you python3 is preinstalled so if we do python3 --version we can see python version is installed by default but pip is not installed so lets install pip sudo apt install python3-pip -y lets also verify the installation pip3 --version and yes pip version is successfully installed you can also write a simple python code to check if everything is working properly. You can like this install everything else you will need one by one
Now as i said in the beginning of the video i will also show you how to create a desktop environment for out ubuntu installatin  lets get right into it at first we will have to install 2 packages 
1. Sudo apt install xfce4 xfce4-goodies -y (xfce is for the core desktop and xfce4 goodies will download Extra utilities (like terminal, task manager, etc.))
2. sudo apt install xrdp -y
3. sudo systemctl enable xrdp
4. sudo adduser $(whoami) ssl-cert
5. echo "startxfce4" > ~/.xsession
6. Remote desktop (mstsc)
7. Localhost 3389
8. in case localhost 3389 is not running in your remote desktop window us this command hostname -I to get the ip assigned to the distro and put that in the remote desktop window
9. then when prompted enter the username and password for your ubutu and we have a desktop environment for our ubuntu running


***into***


Welcome to my channel, AliasDev! If you’ve ever wanted to try using Linux but didn’t want to give up Windows, you have a few options: setting up a virtual machine or dual-booting. However, both can be difficult and time-consuming.

What if I told you that you can run a real Linux kernel from inside Windows using the terminal? Installing it takes only 5 minutes with **one command**. You can seamlessly access Linux files from Windows and vice versa, and it boots in 1-2 seconds. Plus, you can do almost everything you’d want to do in Linux while still being in the comfort of Windows.

That’s the topic of today’s video: **Windows Subsystem for Linux (WSL)**. I’ll show you how to set up the popular Linux distro **Ubuntu** using WSL, configure it for basic development needs, and even get a full desktop environment running.

---

### **WSL Setup**

Before we dive into installing a Linux distribution, we first need to ensure the **Windows Subsystem for Linux** feature is enabled on your system.

1. Open **Windows Search** and look for **"Turn Windows feature on or off"**.
    
2. Open it and scroll down to the bottom.
    
3. Find the option called **"Windows Subsystem for Linux"**. Check the box beside it and click **OK**.
    
4. You will be prompted to restart your PC.
    

After restarting, open your **Windows Terminal** (I’m using PowerShell, but you can also use Command Prompt).

Now that we’ve got the terminal open, let's check what distributions are available for WSL:

bash

CopyEdit

`wsl --list --online`

This command will show all the distros available for installation. To install any of these distros, use the following command:

bash

CopyEdit

`wsl --install <distro-name>`

For this tutorial, we’ll install **Ubuntu**. So, let’s go ahead and do that.

bash

CopyEdit

`wsl --install ubuntu`

Ubuntu will start downloading. This might take some time, so let’s come back when it’s done.

---

Once Ubuntu is downloaded and installed, you can launch it using the command:

bash

CopyEdit

`wsl -d ubuntu`

You’ll be prompted to enter a **Unix username**. This is separate from your Windows user account, but by default, it’ll suggest your Windows username. You can choose whatever username you like. After setting the username, you’ll need to set a password for **sudo** (administrator/root tasks).

After completing the setup, restart your terminal to refresh it.

---

### **System Update**

After restarting your terminal, you should see **Ubuntu** listed alongside PowerShell, Command Prompt, and Git Bash. Open Ubuntu from here, and the first thing we’ll do is update the system:

bash

CopyEdit

`sudo apt update -y && sudo apt upgrade -y`

Enter your password, and the system will update all packages. This will take some time depending on your internet speed.

---

### **Installing Tools**

Now that the system is updated, let’s install **Neofetch**, a system information tool that gives us a quick overview of the system we’re running.

bash

CopyEdit

`sudo apt install neofetch -y neofetch`

Running **neofetch** will show details about your Ubuntu system in the terminal.

---

### **Running GUI Applications**

With **WSL 2** and a feature called **WSLg**, you can now run **GUI applications** inside your terminal—just like you would on a native Linux desktop!

For example, let’s install **Firefox**:

bash

CopyEdit

`sudo apt install firefox -y`

Once it’s done, open it:

bash

CopyEdit

`firefox`

---

### **Configuring VS Code**

Next, let’s configure **Visual Studio Code** to run from within Ubuntu while accessing your Windows files.

1. First, open **VS Code** in Windows.
    
2. Go to the **Extensions** tab and search for **Remote Development**. Install this extension pack, which will allow VS Code to work inside Ubuntu.
    

Now, back in your Ubuntu terminal, you can launch VS Code with:

bash

CopyEdit

`code .`

This will open **VS Code** in Ubuntu, but it’s still the Windows version of VS Code. However, it will use **Linux file paths**, **Linux tools**, and **Linux compilers**.

---

### **Installing Compilers**

If you want to work with **C** and **C++** in your Ubuntu environment, you’ll need to install the compilers:

bash

CopyEdit

`sudo apt install build-essential -y`

This installs **GCC**, **G++**, **Make**, and other essential tools. To check if the installation was successful:

bash

CopyEdit

`gcc --version g++ --version`

For Python, **Python 3** comes preinstalled with Ubuntu in WSL, but **pip** (Python’s package manager) is not. To install **pip**:

bash

CopyEdit

`sudo apt install python3-pip -y`

Verify the installation with:

bash

CopyEdit

`pip3 --version`

You can now install Python packages and run Python code in your Ubuntu environment!

---

### **Creating a Desktop Environment**

As promised, let’s set up a **full desktop environment** for Ubuntu inside Windows. Here’s how:

1. Install the required packages:
    

bash

CopyEdit

`sudo apt install xfce4 xfce4-goodies -y sudo apt install xrdp -y`

2. Enable **xrdp**:
    

bash

CopyEdit

`sudo systemctl enable xrdp`

3. Add yourself to the **ssl-cert** group:
    

bash

CopyEdit

`sudo adduser $(whoami) ssl-cert`

4. Set up **Xfce** to start when you connect remotely:
    

bash

CopyEdit

`echo "startxfce4" > ~/.xsession`

5. Open **Remote Desktop Connection** (search for **mstsc** in Windows).
    
6. In the **Remote Desktop** window, enter `localhost:3389` and connect. If it doesn’t work, use the IP address assigned to the Ubuntu distro (run `hostname -I` in the Ubuntu terminal to find it).
    

You’ll be prompted to log in with the username and password you set for Ubuntu.

And that’s it! You now have a **full desktop environment** for your Ubuntu installation running inside Windows.

---

### **Conclusion**

And there you have it! With WSL and a bit of setup, you can enjoy all the power of Linux while staying within the Windows environment. Whether you need a command-line tool or a full desktop environment, WSL has you covered.
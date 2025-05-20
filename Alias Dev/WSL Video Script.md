# Important Bash Commands

```bash
sudo apt update -y && sudo apt upgrade -y # To update the system right after installation
sudo apt install neofetch -y
neofetch # to install and run neofetch
sudo apt install firefox -y
firefox # to install and fun firefox
# Ubuntu Desktop Environment :
sudo apt install xfce4 xfce4-goodies -y
sudo apt install xrdp -y
sudo systemctl enable xrdp
sudo adduser $(whoami) ssl-cert
echo "startxfce4" > ~/.xsession
hostname -I
sudo apt install build-essential -y # to install gcc and g++ compilers
python3 --version
sudo apt install python3-pip -y #installing pip
pip3 --version 
sudo apt install default-jdk -y # install java
java -version
# compile and run c code
gcc hello.c -o hello_c
./hello_c
# compile and run cpp code
g++ hello.cpp -o hello_cpp
./hello_cpp
# compile and run java code
javac HelloWorld.java
java hello world
# configure git
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global core.editor "code --wait"
git config --global init.defaultBranch main
ssh-keygen -t ed25519 -C "you@example.com"
cat ~/.ssh/id_ed25519.pub
ssh -T git@github.com
```
```c++
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, C++ World!" << endl;
    return 0;
}
```
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Java World!");
    }
}
```

# Script

***Intro***
Hello Everyone, Welcome to Alias Dev
If you are thinking that you want to use Linux and windows on the same computer like me and you google it the top answers are always the same, they either recommend dual-booting or using traditional virtual machines like vmware or virtual-box, but lets be real, both are kind of a hassle they are time consuming takes too much effort and not beginner friendly. But what if i tell you you also have a third option. That's what we are going to discuss in today's video about Windows Subsystem for Linux. 
Now Windows Subsystem for Linux or WSL is a feature of Windows that allows us to run a real Linux kernel inside windows using the windows kernel and a light weight vm called hyper-v and the best part is it is very resource friendly, takes one command to setup and less than 5 minutes to setup totally and no need to reboot to a different operating system as it is running in the windows terminal.
We can access Linux and windows files interchangeably, boot into Linux within seconds, run all sorts of GUI applications and code with the windows native vs code all within the comfort of the windows desktop.
In this video i will walk you through how to install ubuntu a very popular Linux distro on WSL, set it up for development purposes, and then show you how you can run a full ubuntu desktop environment on windows.
So lets jump in.
***WSL Setup***
Before we can go to out terminal and install ubuntu we will first have to make sure that WSL is enabled in windows
To enable WSL in windows 
1. Open the windows search bar
2. Look for "Turn windows Features on or off" and open it
3. Scroll down to the very bottom of this page 
4. Here check the checkbox beside windows subsystem for Linux and click ok
5. after clicking ok you will be prompted to restart your system 
After you have restarted your system open your terminal, i am using Power-shell but using command prompt is totally fine. Once you are inside the terminal you at first will probably want to know which Linux distributions you can install on WSL, in order to see the list of available distros you can use the command 
```bash
wsl --list --online
```
and here you are listed all the possible distros that you can possible install. For this video i will be installing ubuntu but you can install any distro listed here and all works really fine.
To install a distro we use the command 
``` terminal
wsl --install <distro-name>
```
it is going to take a few minutes to download and install.
Ok now that ubuntu is successfully downloaded and installed and we can launch it using the command 
```bash
wsl -d ubuntu
```
Now ubuntu has launched and we can see it is asking for a unix username this might have taken my windows username by default but this is totally different from your windows user account you can go ahead and choose a different username as i will too.
Next we are required to enter a password lets type it out. As you can probably see i have typed my password but the cursor hasn't moved this is for security purposes so don't worry you have typed password lets retype our password you will be using this password for doing admin/root level tasks with sudo. After successfully setting up the unix user account as you can see we are inside the ubuntu terminal and we can start working on it already but at this point i recommend we exit from here and restart the terminal to refresh it.
After restarting the terminal if you come here and open the list of your installed shells as you can see ubuntu is listed alongside my other installed terminals like power-shell ,command prompt, git-bash and since i have kali linux installed beforehand kali is also listed. You can also launch your installed WSL distro from here so lets click on ubuntu and it is opened in a different tab along side powershell. Now id you open powershell and type the command,
```bash
wsl --list --verbose
```
it will list all the installed distros in your system their status that is running or stopped and which WSL version they are using.
Coming back to the ubuntu terminal the first thing we will do is update the system with the command
```bash
sudo apt update -y && sudo apt upgrade -y
```
next we are prompted to enter the sudo password and enter and the system will update all the packages this may also take some time depending on your internet speed.
Now that the system is updated we are ready to install packages and the very first package i will install is neofetch. Neofetch is a command line system information tool that displays the summary of the system we are running. We are installing this tool to check that we are actually running ubuntu on windows terminal. Now when you heard running Linux on terminal you might have expected that it will be limited to command line stuff like writing bash commands install some cli tools and maybe run python scripts but with WSL 2, thanks to a feature called WSLG we can run GUI applications like you are on a native Linux desktop what WSLG does is that it provides a display server behind the scenes. So let us install a few GUI applications and what better than installing a browser first. So we are installing Firefox. Let me demonstrate a few other GUI applications like gimp which is a opensource photo editing tool vlc which is a media player and gedit which is a simple text editor like notepad
***Setting It Up for Development***
For development the first thing we will need is a lightweight customizable code editor with a wide range of extensions and support for various languages and tools. Yes i am talking about vs code lets configure the vs code that you have installed on windows to run in this ubuntu environment.
In order to do that we will first have to open vs code on windows and we need to install a extension pack called remote development this extension pack will install everything we need to setup vs code to run from the Linux environment. Once the extension pack is installed close vs code here and get back to the ubuntu terminal here we will use the command code . to open vs code. For the first time it will setup everything automatically and launch vs code. As you can see we are running the windows version of the vs code but from the Linux environment and it will use the Linux file paths Linux tools and Linux compilers. Yes you will have to install the necessary compilers for ubuntu separately from the windows installations as this is an isolated development environment separate from windows. On that note python is preinstalled so we will not have to install python we can check the version of python. Let us also install the gcc and g++ compilers for c and c++ we can do that using the command. With this we have Our gcc and g++ compilers installed and we can now try running a c and a c++ code so lets do it
``` Bash
nano hello_c.c
```
``` c
#include <stdio.h>

int main() {
    printf("Hello, C World!\n");
    return 0;
}
```
``` bash
gcc hello.c -o hello_c
./hello_c
```
similarly we you try running a simple c++ and python code to check if everything is working fine
If you want to you can also install jdk with the command.

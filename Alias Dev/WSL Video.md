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
Sudo vim /etc/apt/source.list
deb http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware

# Script
***WSL Setup***
Before we hop into our terminals and install our first Linux distribution we have to make sure that we have the windows subsystem for Linux feature enabled in our system 
Now to do that open your windows search and look for "Turn windows feature on or off" open it and then scroll down at the very bottom. Here you can see a feature called windows subsystem for Linux we want to enable this feature so click the check box beside wsl and click ok. Now you will be prompted to restart your pc. After you have restarted we can get to downloading linux on windows, so open your terminal i am using powershell but you ca use any terminal like cmd or something else. Now that we have opened our terminal we first need to know what distros we can download in order to check all the distros that can be downloaded through wsl we will use the command wsl --list --online. As you can see all the distros that we can install are listed. In order to install any distro we will use the command wsl --install <distro-name> for this video we will install 2 distros ubuntu and kali-linux and i will also show you how to setup both distros and install gui desktop enviroments for both of these distros but first we need to install out first distro ubuntu so lets do it. As you can see ubuntu has started to download 
 
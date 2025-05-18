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

Before we hop into our terminals and install our first linux distribution we have to make sure that we have the windows subsystem for linux feature enabled in our system
 
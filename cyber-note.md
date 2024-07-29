*introduction to linux

operating system is software part of the computer that helps to work on . 
it contains - kernel
         - softwares
         - desktop environment 
         - file extensions 
         - window manager
linux by it self is only kernel . linux with GNU is operating system. 

In linux there are three type of desktop environment 
1.mate 
2.genome (have beautiful feature)
3.KDE plasma (similar to window )
4.XFCE

which desktop environment is best 
-speed depend on 
-  animation 
- high graphics 
- quality 
-*window manager*
-i3-window-manager - to perform many things once 
- it can be installed using `sudo apt install i3

*why linux *

- for speed 
- most used (by many websites , servers , systems).
- it has most hacking tools.
- most secured.
- it is open source there is no any organization that controls linux.

***linux distribution*(distro)**

- Distro- are modified linux in kernels, type of operating systems with different 
     - linux kernel
     - packages(GNU)
     - package manager(file manager)
     - Desktop UI(desktop environment)
 - there are many linux distros 
     - Debian 
         - kalin linux
         - ubuntu
         - parrot
    - Arch
         - Black arch
         - Garuda
    - Fedora
    - Red Hat
    - Gentoo
    - Android
- ubuntu is for specifix purpose 

*what is best for hackers?*
        - kali linux
        - parrot os
        - Garuda 
        - Black Arch
      for begineer kali linux and parrot os are best 
    
    
   1. *kali linux 
-  is debian based  or debian derived linux distribution for digital forensic and penetration testing. it is maintained and funded by offensive security.
- desktop envronment = XFCE
- package managers = APT
- shell = ZSH
   2. *parrot 
- is based on debian with a focus on security, privacy and development.
- desktop env= MATE
- package manager =APT
- shell = BASH
3. *Garuda 
- based on arch linux
- desktop env = KDE PLASMA
- package manager= packman
- shell = fish
*do windows have distros?*
- no because window is not an open source so people won't use / edit it.

how can we use it(linux)?
a. main os/main boot 
     -  using only linux by discarding window os.
b. dualBoot / 2 in 1 
    - when we boot our pc it asks as to choose an os we have to shut down to change the os
c. Live boot 
 - by using flash - when we plug the flash in the operating system will be linux 
 - the flash can be above 8GB
D. Cloud terminal 
https://www.terminal.org
E. virtual machine 
- medium processor pc
- using vm software 
- it is like on one computer we can use two or more computers .
- we need to enable *virtualization*
- virtualization help us to use window and linux together.
- this is a method how it allocates out using memory to the virtual machines. 
- softwares that gives us this ability 
      - HyperV
      - ZEMY
      - virtual Box - oracle
      - VMware(common)

F. WSL V2
- for low performance computers
- it helps us to use linux shell on window cmd
- window subsystem for linux 
G. Termux - Android 
- to use linux for android phones 
- for running simple codes 

Day 3 kali linux 
= 
 
*over view of kali linux* 
kali linux was known as Backtrack. 
 - can use  genome and kde plasma
1. Informaton gathering
 - tools for gathering information 
 - e.g nmap
2. vulnerablity Analysis
    - vulnerability means - weakness of a system. 
    - tools for finding vulnerablity anaysis 
    - nikto , nmap
3. web application Analysis 
- tools for finding vulnerablity and exploitation on website - burpsuite 
4. Database Assessment
- tools for finding vulnerablities and exploits on databases - sqlmap
5. password Attacks 
- tools for exploiting passwords for login, websites , application , windows - johnthe ripper , hashcat 
6. wireless Attacks 
-  tools for exploting wireless systems like wifi , bluetooth - aircrack, reaver 
7. reverse Engineering 
- tools for exploiting softwares ,  mobile applications and any binary files - apk tool , NASM shell
8. Exploitation tools 
- tools for metasploit , search exploit 
9. sniffing and spoofing 
- tools for listening or hijacking networks (manefnef)
- weakness yemnfelgibachew tooloch 
- e.g wireshark
10. post exploitation
- tools for maintaining access .used after exploiting a system.
- access kagenyen behuala yemnkoybet 
- backdoor
- powersploit 
11. Forensics 
- Tools for doing researches and investigate a cyber attack
- cyber attack menorun ena detailun investigate yemnaregbet. 
- e.g autopsy , binwalk , foremost , galleta...
12. Reporting tools 
- tools for report preparation . after some forensic you will get data and you will write report and these tools will help you. 
13. social engineering tools 
- sewochn bematalel attack mareg 
- the tools used for social engineering attacks. 
14. system services 
- buttons used to start some services. 
- beef start and beef stop to start and stop services with out the permission of them.  
15. usually used applications
- softwares for some basic or specific purposes. 


File managers in kali linux 
 1. dolphin - looks like window 
 2. thunar - mostly it is found on ubuntu and genome 
 3. nautilus - genome or ubuntu 
to use different file manager in window we have to pay .

some Linux Commands 
= 
the terminal have 5 parts 
`(render@HunterMachine)-[~]`
   - username - rexder 
   - Hostname = HunterMachine
   - current directory = PATH
   - priviledge = $-(user), #-(root)
   - command place = __
   -Home directory is ~
   -Local directory with .
   -All directory *
   
- linux commands hve their own options and arguments 
- what is command 
   - are small programs that do one task well
	   - format - `command --option argument
	`
- Ls = list directory 
- ls -l  - lists with additional information like date....
- ls -a  - all files including hidden file 
- ls filename 
- ls -R =>recursively list files in all folder

- Cd to change directory
- pwd = tells the current working directory 
- echo = to write text and content of files with creating the file . 
- to write `echo "hello" > hi.txt`- the greater than sign means save.
- to append a text on existing file `echo "hello" >> hi.txt`
- cat/head/tail/less = to display the content of a file . 
- touch = to create a file with out writing any thing 
- touch = to create multiple files together `touch abebe kebede`
- mkdir= to create a directory. 
- clear = to clear the terminal (or by ctrl+l)

- rm = to remove files or folders 
- rm -r = recursively remove from folder to file 
- rm -i = delete with promt(ask)
- rm -f = force delete 
	- or we can use them in combination rm -rf  filename or directory.
- cp = copy
- mv = move 

 
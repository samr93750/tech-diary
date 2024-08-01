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
- greg= used to  search a word in a file 
- e.g `grep "abdisa" abdisa.txt`
- grep -i =search file in case sensitive manner
- grep -c = search file - count number
- grep -l = search - displays file name
- grep -R = search foldername -search text in folders recursively  eyegeba
- grep -v = term file name to display with out name
- grep -n "term " file - to display the term find number

- wc = word count 
- wc 

Day 4 linux
= 
 *More on linux*
 Linux file Hierarchy 
 VIM 
 NANO
 LINUX USER MANAGEMENT

      1.LINUX FILE HIERARCHY
 - linux have a special file system than windows.
 - file system is a directory structure that the os uses.
 system files 
  - osachin yemitekemew filoch 
  -   in window it is located in local disk c 
  - in linux it is located in root directory 
  - 
  **1./(root) = is root directory in linux** 
 every single file and directory starts from the root directory.
 $= normal user
 #=root user
 the only root user has the right to access root directory 
 - /root is the root user's home directory , which is not the same as /
 - / is a root directory for user 
 - /root is a root directory for root user
 2 . **bin =  Binary executables** 
     - essential command binaries that need to be available in singleuser mode : for all user 
     - computerachn lay run yemnadergew neger e.g cat,ls , cp ...
3 . **/boot - Boot loader files**
     - kernel initrd , vmlinux , grub files locted under /boot 
     - files that contain that used to boot our computer 
4  /dev = essential device files
     - include terminal devices , usb ,or any device attached to the system.
5 . /etc = et cetera 
- files that contain configuration files required by all programs. 
6 . /home = home directory 
- linux lay create yemnaregachew useroch yemikemetubet bota new .
- - ~ = /home/username(samrawit)
7 . /lib = libraries essential for the binaries in /bin & /sbin
8 . /media = mount points for removable media such as cd-roms 
 - temporary mount directory for removable devices. 
 - /media/cdrom for CDROM
 - /media/floppy for floppy drives.
10 . /mnt = temporarily mounted file
- temporarily mount yemihonu filoch . lemsale flash sekten file keftan then flashun binineklew filun anagenyewm . 
11 . /opt = optional application software package.
 - contains add -on applications from individual vendors.
 - add-on applications should be installed under either /opt or /opt sub-directory.
 12 . /sbin =essential system binaries 
 - it also contain binary executables. but it is used by system administrator(sudo) :- e.g  - adduser = hulum sudo yemil kal eyetetekemn new yemiseruln.
12 .tmp = temporary filoch 
13 . /usr user utilies
- useroch yetinyawn file metekem endemichilu yeminiwesenibetn new 
- create laregnachew metekem yemichilutn filoch yeminaskemitibet

**TEXT EDITOR**
- programs that used for text processing 
- linux command line text editors 
     - VIM 
     - NANO
     - EMACS
- linux Graphical Text editors 
     - sublime
     - vscode
     - gedit
     - pluma

**VIM** 
- it is very power full 
- but at the same time it is cryptic 
- it is hard to learn specially for windows users 
- it has mainly two modes  
    - command mode - where you can do commands 
    - input mode - where you can write .
    by default it is opened as command mode
inside command mode we can 
- save
- save and quit 
- force quit and save
- undo 
- execute bash commands 

-save
   `:w + enter
-to quit
   `:q +enter 
-force quit
    `:wq! + enter`
-undo 
    `:undo + enter` or `:u` 
-extra command 
    `:%!command` e.g :%!grep fun 
    there is no space between them between :%!command
    
**NANO** 
- simple text editor 
- user friendly 
- NANO file name
- ctrl +s = save
- alt +u = undo
- alt + e = redo
- ctrl +shift +c = copy 
- ctrl +shift +x = cut 
- ctrl +shift +v = paste
- ctrl+x =exit 
- ctrl +r = read

LINUX USER MANAGEMENT 

- every user has group 
- users have their own files and applications 
- to know our name on linux = who am i 
- those users have power / privilege
- on linux there are 2 kinds of users 
     - root id =o 
     - normal user (id start with 1-999)
 - the root user have the power to do every thing on linux . 
 - but if users want to have  root access they add sudo infront of command
 - sudo (command)
 - sudo = superuser do = used to pass permission denied.
 - on linux to create users 
     - useradd = simple 
     - adduser = detailed
     -useradd command 
          - `sudo useradd username`
    -adduser command 
     - `sudo adduser username`
     - user files are stored inside /etc/passwd
     - user password are store in /etc/shadow
     - when we create a user it creates a group with that name.
     - 
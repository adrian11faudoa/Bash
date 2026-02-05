# Bash Commands
## Info
All commands are Case Sensitive <br>
apt : Advanced Package Tool <br>
sudo : superuser do <br>
 ~ : /home/username <br>

<br>

## Admin
Check for Linux Distro 
    
    lsb_release -a

Update System 
    
    sudo apt update

? delete user 
    
    sudo deluser --remove-home username

? stop user activity 
    
    sudo kill -9 $(pgrep -u oldname)

? search for users 
    
    cut -d: -f1 /etc/passwd

? human user 
    
    awk -F: '$3 >= 1000 && $1 != "nobody" {print $1}' /etc/passwd

<br>

## System Analysis
Shows the time, since when the system have been up, and amount of users 
 
    uptime

Display amoun of free and used memory in the system 

    free

display Linux processes 

    top

Show processes goin on 

    ps

Report disk space usage 

    df 

Report disk space usage, but in a human format 

    df -h

Use to manipulate disk partition 

    sudo fdisk -l

List block devices 

    lsblk



? Install htop (better top) 

    sudo apt install htop 

<br>

## Network
Configure a network interface (install ifconfig)
    
    sudo apt install net-tools 

    show routing, network, interfaces 

        ip a

<br>

## Manage Packages
Check for updates in the packages 
    
    sudo apt update

Upgrade a package 

    sudo apt upgrade  

Search for a package 

    sudo apt search <ex: zip, app> 

install a package 
    
    sudo apt install <zip>

Remove a package 

    sudo apt remove <zip>

<br>

## Navegation and General Use
Print text to the terminal 

    echo <Text, $VAR, ~>

Print to a file 

    echo <text> >> <file name>

Print Working Directory , show directory 

    pwd 

List , show whats in the folder

    ls

List the contents with a "long list format"

    ls -l

List all the content, even hidden (-a /or/ --all)

    ls -a

Join together -l and -a

    ls -la

-h to make it human readeable

    ls -lah

List whats in the root file system

    ls /

Change directory

    cd <folder_name>

Go back a folder

    cd ..

Go back 2 folders, each set of dots represent a folder

    cd ../..

Go to the root file

    cd /

<br>
Info about a file
    
    file <file with extension> 

Print the content of a file or 
    
    cat <file>

Concatenate files together
    
    cat <file> <file2> > <all file> 

Shows first lines in a file
    
    head <file> 

Shows last lines in a file
    
    tail <file> 

To see what's in a file
    
    more <filename> 

<br>
Word count: showed you how many lines were in the file, how many words, and how many bytes
    
    wc <file.txt>

Diff is a command to view the difference between two files
    
    diff <file_1> <file_2> 

<br>

### SSH Keys
Create SSH Key (press Enter for defaults) 

    ssh-keygen -t ed25519 -C "afa1823@gmail.com"

Start SSH Agent 
    
    eval "$(ssh-agent -s)"

Add Key 
    
    ssh-add ~/.ssh/id_ed25519

Copy Public Key 

    cat ~/.ssh/id_ed25519.pub

Add Key To GitHub 
    
    GitHub → Settings → SSH and GPG Keys → New SSH Key
    Paste key → Save.

<br>


clean the terminal
    
    clear 

Help Flag, to use with other commands
   
    --help

manual of the command
    
    man <command>

make a new folder
    
    mkdir <folder name>

create a new folder in other directory
    
    mkdir <folder path>/<new folder name>

to make directories inside other
    
    mkdir -p <folder>/<child folder>/<child child folder>

create a file
    
    touch <file name> /or/ <directory>


copy a file to a folder
    
    cp <file> <destination>

copy a folder to a new folder
    
    cp -r <folder> <destination>

copy a file to a new file
    
    cp <filename> <new_name>

rename or move something
    
    mv <file name> <new file name> /or/ <destination> /+ or/ <new name>


to view a file tree, shows doc in the directory and inside of each
    
    find

to view the tree from a different folder
    
    find <folder>

search for a file directory or folder
    
    find -name <file name> /or/ <folder name>


remove directory
    
    rmdir <folder name>

remove directory with everything inside
    
    rmdir -r <folder name>

    
    rmdir -p <folder>/<child folder>/<>

remove a file
    
    rm <file name>

to delete a directory
    
    rm -rf <folder>

exit the terminal
    
    exit


pause execution for a num of sec
    
    sleep <sec>
    
redirect an output to a file, create or overwrite a file

    <echo hello test> > <filename.txt> 

redirect an output to a file, append
    
    <echo hello test> >> <filename.txt>



This will take the stdout from command_1 and use it as the stdin for command_2
    
    <command_1> | <command_2>

grep is a command for searching for patterns in text
    
    grep --color -n '<pattern>' <filename>


diff is a command to view the difference between two files

    diff <file_1> <file_2>


print the content of a file
    
    cat <file>





sed 's/<pattern_1>/<replacement_1>/; s/<pattern_2>/<replacement_2>/'


<command> < <filename_for_stdin>

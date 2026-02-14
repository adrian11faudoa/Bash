# Bash Commands

## Info
>All commands are Case Sensitive <br>
>sudo : superuser do <br>
> ~ : /home/username <br>

>dpkg : Debian Package = low-level tool that installs/removes local .deb files. <br>
>apt : Advanced Package Tool = high-level tool that downloads + installs + manages dependencies + repositories, and internally uses dpkg <br>

<br>


## Admin Management
### Check for Linux Distro 
    
    lsb_release -a

? delete user 
    
    sudo deluser --remove-home username

? stop user activity 
    
    sudo kill -9 $(pgrep -u oldname)

? search for users 
    
    cut -d: -f1 /etc/passwd

? human user 
    
    awk -F: '$3 >= 1000 && $1 != "nobody" {print $1}' /etc/passwd

<br>


## Manage Packages
### Refresh the list of available software packages from your configured repositories
    
    sudo apt update

### Install the newest versions of software that are already installed on your system

    sudo apt upgrade  

### Search for a package 

    sudo apt search <ex: zip, app> 

### Install a package 
    
    sudo apt install <zip>

### Remove a package 

    sudo apt remove <zip>

<br>


## System Analysis
### Display Linux processes 

    top

### Display amoun of free and used memory in the system 

    free

### Report disk space usage 

    df 

### Report disk space usage, but in a human format 

    df -h

### Use to manipulate disk partition 

    sudo fdisk -l

### Shows the time, since when the system have been up, and amount of users 
 
    uptime

### Show processes goin on 

    ps

### List block devices 

    lsblk

? Install htop (better top) 

    sudo apt install htop 

<br>


## Network
? Configure a network interface (install ifconfig)
    
    sudo apt install net-tools 

    show routing, network, interfaces 

        ip a

<br>

## Navegation and General Use
### Print Working Directory, show directory 

    pwd 

### List, show whats in the folder

    ls

### List the contents with a "long list format"

    ls -l

### List all the content, even hidden (-a /or/ --all)

    ls -a

### Join together -l and -a

    ls -la

### -h to make it human readeable

    ls -lah

### List whats in the root file system

    ls /

### Change directory

    cd <folder_name>

### Go back a folder

    cd ..

### Go back 2 folders, each set of dots represent a folder

    cd ../..

### Go to the root file

    cd /

<br>


## Files Management
### Print text to the terminal 

    echo < text, $Var, ~ >

### Print to a file 

    echo <text> >> <file name>

### Show info about a file
    
    file <file with extension> 

### Print the content of a file in terminal
    
    cat <file>

### Concatenate files together
    
    cat <file> <file2> > <all file> 

### Shows first lines in a file
    
    head <file> 

### Shows last lines in a file
    
    tail <file> 

### See what's in a file
    
    more <filename> 

### Word count: showed you how many lines, words, bytes were in the file
    
    wc <file.txt>

### See difference between two files
    
    diff <file_1> <file_2> 

<br>


## SSH Keys
### Check for SSH Key

    ls ~/.ssh

### Create new SSH Key (press Enter for defaults, no passphrase) 

    ssh-keygen -t ed25519 -C "afa1823@gmail.com"

### Start SSH Agent (and run it in shell)
    
    eval "$(ssh-agent -s)"

### Add Key to SSH Agent (Save)
    
    ssh-add ~/.ssh/id_ed25519

### Show Public Key in Terminal

    cat ~/.ssh/id_ed25519.pub

### Add Key To GitHub 
    
>GitHub → Settings → SSH and GPG Keys → New SSH Key → Paste key → Save

<br>


## General Use
### Clean the terminal
    
    clear 

### Help Flag, to use with other commands
   
    --help

### Manual of the command
    
    man <command>

### Exit the terminal
    
    exit

<br>


## Create  
### Make a new folder
    
    mkdir <folder name>

### Create a new folder in other directory
    
    mkdir <folder path>/<new folder name>

### Make directories inside other
    
    mkdir -p <folder>/<child folder>/<child child folder>

### Create a file
    
    touch <file name> /or/ <directory>

<br>


## Copy 
### Copy a file to a folder
    
    cp <file> <destination>

### Copy a folder to a new folder
    
    cp -r <folder> <destination>

### Copy a file to a new file
    
    cp <filename> <new_name>

<br>


## Rename
### Rename a file

    mv <file name> <new file name> 

### Move and rename a file

    mv <file name> <destination> <new file name>

<br>


## Search
### View a file tree, shows doc in the directory and inside of each
    
    find

### View the tree from a different folder
    
    find <folder>

### Search for a file directory or folder
    
    find -name <file name> /or/ <folder name>

<br>


## Delete
### Remove directory
    
    rmdir <folder name>

### Remove directory with everything inside
    
    rmdir -r <folder name>

    
    rmdir -p <folder>/<child folder>/<>

### Remove a file
    
    rm <file name>

### Delete a directory
    
    rm -rf <folder>

<br>






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

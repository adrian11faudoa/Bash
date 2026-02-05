# Bash Commands

    - Info:
        All commands are Case Sensitive
        apt : Advanced Package Tool
        sudo : superuser do
        ~ : /home/adr11an


### Admin
    - Check for Linux Distro
        lsb_release -a
    - Update System
        sudo apt update

    ? delete user
        sudo deluser --remove-home username
    ? stop user activity
        sudo kill -9 $(pgrep -u oldname)
    ? search for users
        cut -d: -f1 /etc/passwd
    ? human user
        awk -F: '$3 >= 1000 && $1 != "nobody" {print $1}' /etc/passwd


### System Analysis
    - shows the time of the system have been up, amount of users
        uptime
    - display amoun of free and used memory in the system
        free
    - show processes goin on
        ps
    - report disk space usage
        df 
    - report disk space usage, but in a human format
        df -h
    - to manipulate disk partition
        sudo fdisk -l
    - list block devices
        lsblk
    - display Linux processes
        top
    - install htop (better top)
        sudo apt install htop 


### Network
    - configure a network interface
        sudo apt install net-tools (install ifconfig)
    - show routing, network, interfaces
        ip a


### Manage Packages
    - check for updates in the packages
        sudo apt update
    - upgrade a package
        sudo apt upgrade 
    - search for a package
        sudo apt search <ex: zip, app> 
    - install a package
        sudo apt install <zip>
    - remove a package
        sudo apt remove <zip>


### Navegation and General Use
    - Print text to the terminal
        echo <Text, $VAR, ~>
    - Print to a file
        echo <text> >> <file name>
    - Print Working Directory , show directory
        pwd 

ls : list , show whats in the folder
ls -l : list the contents with a "long list format"
ls -a /or/ --all: list all the content, even hidden
ls -la : join together -l and -a
ls -lah : -h to make it human readeable
ls / :list whats in the root file system

cd <folder_name> : change directory
cd .. : go back a folder
cd ../.. :go back 2 folders, each set of dots represent a folder
cd / : go to the root file

file <file with extension> : info about a file 
cat <file> : print the content of a file or 
cat <file> <file2> > <all file> : concatenate files together
head <file> : shows first lines in a file
tail <file> : shows last lines in a file
more <filename> : to see what's in a file
wc <file.txt> <<word count: showed you how many lines were in the file, how many words, and how many bytes
<<diff is a command to view the difference between two files
diff <file_1> <file_2> 


### SSH Keys
    - Create SSH Key (press Enter for defaults)
        ssh-keygen -t ed25519 -C "afa1823@gmail.com"

    - Start SSH Agent
        eval "$(ssh-agent -s)"

    - Add Key
        ssh-add ~/.ssh/id_ed25519

    - Copy Public Key
        cat ~/.ssh/id_ed25519.pub

    - Add Key To GitHub
        GitHub → Settings → SSH and GPG Keys → New SSH Key
        Paste key → Save.



    echo <Message in the terminal> : print to the terminal
    echo <text> >> <file name> : print to a file 
    pwd : print working directory , show directory 

    ls : list , show whats in the folder
    ls -l : list the contents with a "long list format"
    ls -a /or/ --all: list all the content, even hidden
    ls / :list whats in the root file system

    cd <folder_name> : change directory
    cd .. : go back a folder
    cd ../.. :go back 2 folders, each set of dots represent a folder

    more <filename> : to see what's in a file
    clear : clean the terminal
    --help : Help Flag, to use with other commands
    man <command> :manual of the command

    mkdir <folder name> : make a new folder
    mkdir <folder path>/<new folder name> : create a new folder in other directory
    touch <file name> /or/ <directory>: create a file

    cp <file> <destination> : copy a file to a folder
    cp -r <folder> <destination> : copy a folder to a new folder
    cp <filename> <new_name> : copy a file to a new file
    mv <file name> <new file name> /or/ <destination> : rename or move something

    find : to view a file tree, shows doc in the directory and inside of each
    find <folder> : to view the tree from a different folder
    find -name <file name> /or/ <folder name> : search for a file directory or folder

    rm <file name> : remove a file
    rmdir <folder name> : remove directory
    rmdir -r <folder name> : remove directory with everything inside
    exit : exit the terminal

    sleep <sec>: pause execution for a num of sec
     
    <echo hello test> > <filename.txt> <<redirect an output to a file, create or overwrite a file
    <echo hello test> >> <filename.txt> <<redirect an output to a file, append

    <command> < <filename_for_stdin>

    <command_1> | <command_2> <<This will take the stdout from command_1 and use it as the stdin for command_2

    wc <file.txt> <<word count: showed you how many lines were in the file, how many words, and how many bytes

    <<grep is a command for searching for patterns in text
    grep --color -n '<pattern>' <filename>

    sed 's/<pattern_1>/<replacement_1>/; s/<pattern_2>/<replacement_2>/'

    <<diff is a command to view the difference between two files
    diff <file_1> <file_2>

    - print the content of a file
cat <file>














clear : clean the terminal
--help : Help Flag, to use with other commands
man <command> :manual of the command

mkdir <folder name> : make a new folder
mkdir <folder path>/<new folder name> : create a new folder in other directory
mkdir -p <folder>/<child folder>/<child child folder> : to make directories inside other
touch <file name> /or/ <directory>: create a file

cp <file> <destination> : copy a file to a folder
cp -r <folder> <destination> : copy a folder to a new folder
cp <filename> <new_name> : copy a file to a new file
mv <file name> <new file name> /or/ <destination> /+ or/ <new name>: rename or move something

find : to view a file tree, shows doc in the directory and inside of each
find <folder> : to view the tree from a different folder
find -name <file name> /or/ <folder name> : search for a file directory or folder

rmdir <folder name> : remove directory
rmdir -r <folder name> : remove directory with everything inside
rmdir -p <folder>/<child folder>/<>
rm <file name> : remove a file
rm -rf <folder> : to delete a directory
exit : exit the terminal



sleep <sec>: pause execution for a num of sec
    
<echo hello test> > <filename.txt> <<redirect an output to a file, create or overwrite a file
<echo hello test> >> <filename.txt> <<redirect an output to a file, append

<command> < <filename_for_stdin>

<command_1> | <command_2> <<This will take the stdout from command_1 and use it as the stdin for command_2

<<grep is a command for searching for patterns in text
grep --color -n '<pattern>' <filename>

sed 's/<pattern_1>/<replacement_1>/; s/<pattern_2>/<replacement_2>/'


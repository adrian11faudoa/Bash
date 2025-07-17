Subject:

Bash CMD (case sensitive)

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



<<Student DB

<<print the content of a file
cat <file>
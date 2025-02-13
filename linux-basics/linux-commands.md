## ls
- This command is used when listing all the files that are inside a container.
- It has several combinations such as -al which returns more detailed information about the files inside a particular folder.
## cd 
- The change directory command makes it possible for you to move inside a specified path/folder.
- by using cd .. ,you move to the previous directory/parent folder.
## pwd
- This command is used to know which directory you are in, by running it ,it will print the current folder path
## mkdir
- This command is used to create folders
- YOu can create multiple folders with one command: mkdir dogs people
- You can also create multiple nested folders by adding the -p option: mkdir -p fruits/apples
## rmdir 
- Used to delete a folder or multiple folders at once ( The folder must be empty)
- To delete folders with files in them (rm -rf fruits people)
## mv
- Used to move a file by specifying the file's current path and its new path
- (mv pear new_pear) - Renaming files and folders
- If the last parameter is a folder, the file located at the first parameter is going to be moved into the folder
- (mv pear apple fruits) - pear and apple moved to the fruits folder
## cp 
- Used to copy a file
- To copy folders, you need to add the -r to recursively copy the whole folder contents (cp -r fruits people)
## touch 
- Used to create an empty file eg touch apple
## open
- Used to open a directory 
- (open .) - opens the current directory
- Can also be used to open an application
## find
- The find command can be used to find files or folders matching a particular search pattern. It searches recursively
- (find . -name '*.js') - Find all files under the current tree that have the .js extension and print the relative path of each file that matches
- (find . -type d name src) - Find directories under the current tree matching the name 'src'
- (find folder 1 folder 2 -name filename.txt) - Searching under multiple root trees
- (find . -type d -name node_modules -or -name public) - Find directories under the current tree matching the name 'node_modules' or 'public'
- (find . -type d -name '*.md' -not -path 'node_modules/*') - excluding a path
- (find . -type f -size +100c) - Searching files that have more than 100 characters(bytes) in them
- (find . -type f -size +100k -size -1M) - Searching files bigger tha 100KB but smaller than 1MB
- (find . -type f -mtime +3) - Searching files edited more that 3 days ago
- (find . -type f -mtime -1) - Searching files edited in the last 24 hrs
## ln
- Used to create links(Pointer to another file)
- There are two types of links(hard links and soft links
- Hard links are rarely used. You cant link to directories and external filesystems
- (ln recipes.txt newrecipes.txt) - Creating a hard link
- Soft links are different. They are more powerful as you can link to other filesystems and to directories but when the original is removed, the link will be broken
- (ln -s recipes.txt newrecipes.txt) - Creating a soft link
## gzip
- Used for compressing a file
- (gzip filename) - This will compress the file and append the .gz extension to it and the original file is deleted. To prevent this, use the -c option and use the output redirection to write the output to the filename.gz file. ( gzip -c filename > filename.gz)
- (gzip -d filename.gz) - Decompressing the file
## gunzip
- Basically the equivalent of gzip only that when decompressing, no need for adding the -d
## tar
- Used to create an archive, grouping multiple files in a single file
- (tar -cf archive.tar file1 file2) - Creates an archive named archive.tar with the content of file1 file2
- (tar -xf archive.tar) - Extract files from an archive in the current folder
## alias 
- This is like creating a new command to mimic an existing command so that you dont use the existing command according to your preferences
- (alias ll = 'ls -al') - Creating a new command 'll' that is an alias to 'ls -al'
- (alias) - will list all the aliases defined
- The alias will work until the terminal sessions is closed
- To make it permanent, add it to the shell configuration
## tail
- Opens the file at the end and watches for file changes
- Great for watching log files ( tail -f /var/log/system.log )
## grep
- Used to search in lines or can be combined with pipes to filter the output of another command
- (grep "error" logfile.txt) - Finds and prints all lines in logfile.txt containing the word "error"
- (grep "hello" file1.txt file2.txt) - Searches for "hello" in both files
- You can use -i to ignore case sensitivity
- (grep -i "error" logfile.txt) - Finds "Error", "error" ,etc
- Can also be used in searching in the output of another command as shown in the next line
- ps aux | grep "firefox"
- (grep -v "error" logfile.txt) - Inverting the search ie exclude all lines that contain the pattern
- (grep -n "command" logfile.txt) - Shows the line numbers where "command" has appeared
- (grep -c "error" logfile.txt) - counts the number of lines containing "error"
- (grep "^hello" file.txt) - search for lines that start with "hello"
- (grep "done$" file.txt) - search for files that end with "done"
## sort
- Used in sorting elements in a file
- (sort -r filename.txt) - Reverses the order of sorting
- Can work with pipes,i.e you can use it on the output of another command ls | sort
## echo
- echo "Hello world" - prints a simple messsage
- name="John", echo "Hello $name" - This will print the value of variable
- echo "Hello, file" > output.txt - This will direct the output to a file but will override the contents of that file
- echo "Hello file" >> output.txt - This will append or add another line at the end of output.txt
- echo "Today is $(date) - Using echo with other commands
## chown
- Every file/directory in linux has an owner
- This command is used to change the owner of the file or directory
- The owner of a directory/ file or the root user are eligible to use this command
- sudo chown astro test.txt - Transferring the file ownership to astro
- chown -R <owner> <file> - Changing the ownership of a directory and all other files in it.
- chown <owner>:<group> <file> - Through this command,I can simulataneousy change the owner and the group of the file
- chgrp <group> <file> - Directly changing the group of the file
## chmod
- Used to change the permissions of a file
- Every file has 3 permissions (read, write and execute)
- For example if a go into a directory and run ls -al, the following is displayed
- drwxrwxr-x  4 astro astro 4096 Feb  9 11:33 .  
drwxr-x--- 31 astro astro 4096 Feb 12 14:50 ..  
drwxrwxr-x  8 astro astro 4096 Feb 13 12:32 .git  
drwxrwxr-x  2 astro astro 4096 Feb 13 12:39 linux-basics  
-rw-rw-r--  1 astro astro  163 Feb  9 11:32 README.md
- The letters and hyphens you see at the start of every file/folder are the permissions given of the file/folder
- (-) means its a normal file
- (d) means its a directory
- (l) means its a link
- After that, the first 3 values eg rwx represents the permissions of the owner of the file/directory
- The next 3 values eg r-x  represents the permissions of the group of the file
- The last 3 values eg --- represents the permissions of the other members or everyone else that comes across the file
- rwx means that person has read, write and execute permissions of the file/directory
- If either of the rwx values is swapped with - ,that means that person lacks the swapped permission eg :
- r-x means the person has read and execute permission but lacks the write permission
- You can change the permissions using the chmod command 

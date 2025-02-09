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


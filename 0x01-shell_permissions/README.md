This time we are handling the Permissions in shell.
0. Change user to betty => su-betty \n 
1. Prints the effective username of the current user  => whoami \n
2. prints all the groups the current user is part of => id -Gn root \n
3. changes the owner of the file hello to the user betty => chown betty hello \n
4. Create an empty file called hello => touch hello \n
5. A script that adds execute permission to the owner of the file hello => chmod +100 hello \n
6. Adds execute permission to the owner and the group owner, and read permission to other users, to the file hello => chmod +114 hello \n
7.A script that adds execution permission to the owner, the group owner and the other users, to the file hello => chmod +111 hello \n
8. Owner and groups no permissions but others all permissions
9.-rwxr-x-wx => chmod 753 hello \n
10. Sets the mode of the file hello the same as olleh’s mode. => chmod --reference=hello olleh
11. Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed. =>chmod +111 $(find * -type d) \n
12. Create a script that creates a directory called my_dir with permissions 751 in the working directory. => mkdir -m 751 my_dir
13. Write a script that changes the group owner to school for the file hello =>chgrp school hello \n
## Task 1
### Create a simple file and do `ls -ltr` to see the details of the files and change user permissions of the file

- Use Command - `touch sampleFile.txt`
- To see details of files, `ls sampleFile.txt -ltr`

Output  -

    -rw-rw-r-- 1 ubuntu ubuntu 0 Jan 7 18:45 sampleFile.txt

- The first blank denotes that it is a file, and not a directory. The next 3 characters 'rw-' represent that the owner has read and write permissions, the next 3 characters 'rw-' represents that the belonging group has read and write permissions, and the last 3 represent any other users who have only read permissions.
- So to change the permissions, type command `chmod 770 sampleFile.txt`

Output  -

    -rwxrwxr-- 1 ubuntu ubuntu 0 Jan 7 18:45 sampleFile.txt
		
- Now the file permissions have been changed. The owner of the file, and the group that it belongs has the permission to read, write and execute as well.

## Task 2
### Write an article about File Permissions

- When a file is created in Linux, it comes with certain permissions about who can access and do what with the file. We can have a look at the permissions of a file or directory using `ls -ltr` command. 
- As from the above example, we can notice that when sampleFile.txt was created, the owner and the group that the file belong to had the permission to read and write. Any other user had only read permission by default. So we can modify the file permission with the help of `chmod` change mode command. 
- Here are some common Linux file permissions commands:
	+ `chmod` : Change the permissions of a file or directory. You can use this command to add or remove permissions for different user groups.
	+ `chown` : Change the ownership of a file or directory. You can use this command to change the user and group ownership of a file or directory.
	+ `umask` : Set the default permissions for newly created files and directories.
	+ `chgrp` : Change the group ownership of a file or directory. You can use this command to change the group that owns a file or directory.

### ACL -Access Control List
- Access control list (ACL) provides an additional, more flexible permission mechanism for file systems. It is designed to assist with UNIX file permissions. ACL allows you to give permissions for any user or group to any disc resource.
- ACLs allow us to apply a more specific set of permissions to a file or directory without (necessarily) changing the base ownership and permissions. They let us "tack on" access for other users or groups. 

Use Command - `getfacl sampleFile.txt`

Output  -

    # file : sampleFile.txt
		# owner: ubuntu
		# group: ubuntu
		user::rwx
		group::rwx
		other::---
		
Use Command - `setfacl -m o:rw sampleFile.txt` Setting acl file permission for other user to read and write

Output  -

    # file : sampleFile.txt
		# owner: ubuntu
		# group: ubuntu
		user::rwx
		group::rwx
		other::rw-
		

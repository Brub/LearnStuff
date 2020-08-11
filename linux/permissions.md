# Permissions
Although there are already a lot of good security features built into Linux-based systems, one very important potential vulnerability can come from file permission-based issues resulting from a user not assigning the correct permissions to files and directories.

## check permissions

As you may have noticed, we have used the known **ls** command using a new flag, **-la**. Basically, the -la flag allows us to see some basic data related to the files or folders, like the permissions of the files/folders, their creation date/time, etc

```
ls -la
```

this result will be something like
```
-rw-r--r-- 1 user user 2257 Aug  7 14:41 move_bb8_square.py
```

For now, let's just focus on the first part, which is rw-r--r--. These are the PERMISSIONS of the file.

Each file or directory has 3 permissions types:

* **read**: The Read permission refers to a user's ability to read the contents of the file. It is stated with the character r.

* **write**: The Write permission refers to a user's ability to write or modify a file or directory. It is stated with the character w.

* **execute**: The Execute permission affects a user's ability to execute a file or view the contents of a directory. It is stated with the character x.

On the other hand, each file or directory has three user-based permission groups:

* **owner**: The Owner permissions apply only to the owner of the file or directory, and will not impact the actions of other users. They are represented in the first 3 characters.

* **group**: The Group permissions apply only to the group that has been assigned to the file or directory, and will not affect the actions of other users. They are represented in the middle 3 characters.

* **all users**: The All Users permissions apply to all other users on the system, and this is the permission group that you want to watch the most. They are represented in the last 3 characters.

## chmod
In Linux, the chmod command is used to modify the permissions of a given file or directory (or many of them). There are a couple of ways to use this command, though, so let's go by parts.

The structure of the chmod command goes as follows:

```chmod  <groups to assign the permissions><permissions to assign/remove> <file/folder names>```

### add/remove a permission to all users

**add**  

```bash
chmod +x move_bb8_square.py   
# result
-rwxr-xr-x 1 user user 2257 Aug  7 14:41 move_bb8_square.py  
```
**remove**

```
bash
chmod -x move_bb8_square.py   
# result
-rw-r--r-- 1 user user 2257 Aug  7 14:41 move_bb8_square.py
```

### permissions for a specific group
We already know the 2 last parameters. As for the groups, you can specify them using the following flags:

* **u**: Owner  
* **g**: Group  
* **o**: Others  
* **a**: All users. For all users, you can also leave it blank, as we did in the example command you executed before.

```
chmod g+w move_bb8_square.py
```

### permissions by Binary References
It's quite simple actually. Basically, the whole string stating the permissions (rwxrwxrwx) is substituted by 3 numbers. The first number represents the Owner permission; the second represents the Group permissions; and the last number represents the permissions for all other users. And how do these numbers work?

Basically, each permission has a number assigned:

* r = 4
* w = 2
* x = 1

Then, you add the numbers to get the integer/number representing the permissions you wish to set. You will need to include the binary permissions for each of the three permission groups.

For instance, let's say that we want to give the owner full permissions (rwx). Then, we would add 4 + 2 + 1 = 7. Now, for the Group, we just want to give read permissions (r--). Then, that would just be a 4. Finally, for all the other users, we don't want to give them any permission. Then, that would be a 0. So, at the end, we would have 740. So, the final command would be like this:

```
chmod 740 move_bb8_square.py
```
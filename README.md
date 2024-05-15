# ADS Labo 6

Authors : Felix Breval, Anthony David, Timothée Van Hove

Group : Lab_3_C

Date: 2024-04-29

# Task 0: Examine the setup of your own account

> - Examine your account by using the command `id` and by looking into the files
>   `/etc/passwd` and `/etc/group` . What is its principal group? What other groups is
>   the account a member of? What is the UID of the account and the GID of the
>   principal group?

**Output :** 

```bash
$ id
uid=1000(anthony) gid=1000(anthony) groups=1000(anthony),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),114(lpadmin),125(libvirt),988(sambashare)
```

**Answers to questions:**

1. **Principal group**: The principal group is `anthony`.
2. **Other groups**: The account belongs to the groups `adm`, `cdrom`, `sudo`, `dip`, `plugdev`, `lpadmin`, `libvirt`, and `sambashare`.
3. **UID of the account**: The UID of the account is `1000`.
4. **GID of the principal group**: The GID of the principal group is `1000`.

> - Which skeleton files have been copied?

**Output :**

```bash
$ ls -a /etc/skel

.  ..  .bash_logout  .bashrc  .face  .face.icon  .profile

```

**Answer to question :**

The skeleton files that have been copied from `/etc/skel` are:

- `.bash_logout`
- `.bashrc`
- `.face`
- `.face.icon`
- `.profile`

# Task 1: Create user accounts

> In this task you will use command-line tools to manage user accounts.
> Perform the following steps and give in the lab report the commands you used. Use the
> tools useradd and groupadd .
>
> 1. Create the groups `jedi` and `rebels` . Before creating them verify that they do not yet exist.



> 2. Create the following user accounts with default home directories and login shell (for example account luke should have home directory `/home/luke` and a `bash` shell).
>    Note: For fear of overwriting something the `useradd` tool is very cautious about creating the home directory for an account.
>
>    - What option do you need to specify to have `useradd` create a home directory?
>    - What is the default login shell for users created with `useradd` ? What
>      command should we use to change the default login shell from `/bin/sh` to `/bin/bash` ?
>
>    Before creating them verify that they do not yet exist.
>
>    - Account `luke` , assigned to groups `jedi` (principal) and `rebels`.
>    - Account `vader` , assigned to group `jedi` (principal).
>    - Account `solo` , assigned to group `rebels` (principal).



> 3. Set a password for the account `luke`.



> 4. Test the account `luke` . Verify that the user can log in and create files. 
>
>    Verify that the user cannot access sensitive system information such as the file `/etc/shadow`.



> 5. Use `su` to change your account to that of `vader`. Test if the user vader has access to the files in the home directory of user `luke` .



# Task 2: Change groupe membership

## 

> 1. Create the Account `leia` Without Assigning It a Principal Group:After it was created, which principal group did it get assigned?



> 2. Make `leia` a Member of the Group `rebels` (as a Secondary Group).



> 3. Make `leia` Leave the Group `rebels` and Join the Group `jedi` Instead:



> 4. Make `leia` Leave Any Secondary Group:



# Task 3: Give a user sudo rights

> To give a user access to `sudo` one must normally manually edit the file `/etc/sudoers` by using the `visudo` command and list all the users there. In many Linux distributions (among them Ubuntu) though touching the file is not necessary. Out of the box the file `/etc/sudoers` is configured to give sudo access to all users that are members of the group named `sudo` . Instead of modifying the `/etc/sudoers` file, one can simply make users members of the `sudo` group.
> Questions:
> a) Which line in `/etc/sudoers`gives the members of the group sudo the right to execute any command?



> b) How would you have to modify this line so that users can use sudo without typing a password (this is in general not recommended, but can be handy sometimes).



> Perform the following steps and give in the lab report the commands you used.
>
> 1. Give the account `luke` sudo rights.



> 2. Test the new rights. Verify that `luke` can read the file /etc/shadow using `sudo`.



> 3. Remove sudo rights from the account `luke`.





# Task 4 : Remove a user account

> Perform the following steps and give in the lab report the commands you used. Use the
> tool `userdel`.
>
> 1. Remove the account `leia`, but do not delete the home directory yet.



> 2. Inspect the home directory (look at the file metadata). What has changed?



> 3. Suppose the user `leia` has created other files on the system, but you do not
>    know where they are. How would you systematically scan the whole system to find
>    them?



> 4. Remove the home directory manually.




**Lesson: Creating and Managing Users, Groups, and Permissions**

**Objective:**
By the end of this lesson, students will be able to create and manage users, groups, and permissions in a Linux environment.

**Introduction:**
User and group management, along with permissions settings, are fundamental aspects of Linux system administration. In this lesson, we will cover how to create and manage users and groups, as well as how to set permissions for files and directories.

**Main Content:**

1. **User Management:**
    - **Creating Users:** Use the `useradd` command to create new users.
        - Example: `sudo useradd username`
    - **Setting Passwords:** Use the `passwd` command to set or change a user's password.
        - Example: `sudo passwd username`
    - **Modifying User Attributes:** Use the `usermod` command to modify user attributes such as the username, home directory, or shell.
        - Example: `sudo usermod -d /new/home/directory username`
    - **Deleting Users:** Use the `userdel` command to delete users.
        - Example: `sudo userdel username`

2. **Group Management:**
    - **Creating Groups:** Use the `groupadd` command to create new groups.
        - Example: `sudo groupadd groupname`
    - **Adding Users to Groups:** Use the `usermod` command to add users to groups.
        - Example: `sudo usermod -aG groupname username`
    - **Deleting Groups:** Use the `groupdel` command to delete groups.
        - Example: `sudo groupdel groupname`

3. **Permissions Management:**
    - **File Permissions:** Files and directories in Linux have three types of permissions: read, write, and execute, assigned to three categories of users: owner, group, and others.
    - **Changing Permissions:** Use the `chmod` command to change file permissions.
        - Example: `chmod u+rwx file` (Adds read, write, and execute permissions for the owner).
    - **Changing Ownership:** Use the `chown` command to change the owner and group of files and directories.
        - Example: `sudo chown username:groupname file` (Changes the owner and group of the file).

**Examples:**

- **User Management:**
    - Create a new user named "john": `sudo useradd john`
    - Set a password for the user "john": `sudo passwd john`
    - Change the home directory of the user "john": `sudo usermod -d /new/home/directory john`
    - Delete the user "john": `sudo userdel john`

- **Group Management:**
    - Create a new group named "developers": `sudo groupadd developers`
    - Add the user "john" to the "developers" group: `sudo usermod -aG developers john`
    - Delete the group "developers": `sudo groupdel developers`

- **Permissions Management:**
    - Change file permissions to allow read, write, and execute for the owner: `chmod u+rwx file`
    - Change the owner of a file to "john" and the group to "developers": `sudo chown john:developers file`

**Conclusion:**
Managing users, groups, and permissions is essential for maintaining security and access control on Linux systems. Practice these commands regularly to become proficient in managing users, groups, and permissions effectively.

**Homework Assignment:**
Create multiple users and groups, assign appropriate permissions to files and directories, and experiment with changing ownership and permissions settings. Observe the impact of these changes on user access and file operations.

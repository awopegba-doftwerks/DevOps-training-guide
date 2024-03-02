**Week 3: Advanced File Management and Process Control**

**Objective:**
In Week 3, students will dive deeper into advanced file management techniques and learn how to control processes effectively in a Linux environment.

**Lesson Plan:**

**Day 1: Advanced File Management**
- **Objective:** Explore advanced file management commands and techniques.
- **Topics Covered:**
    - Working with symbolic links (`ln` command).
    - Archiving and compressing files and directories (`tar` and `gzip` commands).
    - Searching for files and text within files (`find` and `grep` commands).
- **Practical Examples:**
    - Creating a symbolic link to a file: `ln -s /path/to/original /path/to/link`
    - Creating a tar archive of a directory: `tar -cvf archive.tar /path/to/directory`
      The command `tar -cvf archive.tar /path/to/directory` is used to create a new tar archive file named `archive.tar` containing the contents of the specified directory located at `/path/to/directory`. Here's a breakdown of each component of the command:
      - **`tar`**: This is the command-line utility for manipulating tar archives. "Tar" stands for "tape archive," originally used for archiving files to tape drives but now commonly used for creating archive files on disk.
        - **`-cvf`**:
          - `-c`: This flag tells `tar` to create a new archive.
          - `-v`: This flag stands for "verbose" mode, which instructs `tar` to display the progress of archiving and list the files being processed.
          - `-f`: This flag indicates that the next argument (`archive.tar` in this case) specifies the name of the archive file.

        - **`archive.tar`**: This is the name of the tar archive file that will be created. In this example, the archive file will be named `archive.tar`.

        - **`/path/to/directory`**: This is the path to the directory whose contents will be archived. In the command, `/path/to/directory` should be replaced with the actual path of the directory you want to archive. When you run this command, `tar` will create a new tar archive file named `archive.tar` containing all the files and directories within the specified directory (`/path/to/directory`). The `-v` flag provides verbose output, showing the progress of the archiving process and listing the files as they are added to the archive.

    - Compressing a file with gzip: `gzip file.txt`
    - Searching for files modified within the last 7 days: `find /path/to/directory -type f -mtime -7`. The command `find /path/to/directory -type f -mtime -7` is used to search for files within a specific directory (`/path/to/directory`) that have been modified in the last 7 days. Here's an explanation of each component of the command:

- **`find`**: This is the command-line utility for searching files and directories based on various criteria.

- **`/path/to/directory`**: This specifies the directory in which the search will be conducted. Replace `/path/to/directory` with the actual path to the directory you want to search within.

- **`-type f`**: This option tells `find` to only consider regular files in the search. It excludes directories, symbolic links, and other types of files.

- **`-mtime -7`**: This option specifies the criteria for the modification time of files to be considered.
  - `-mtime` stands for "modification time".
  - `-7` indicates files modified within the last 7 days. The minus sign (`-`) before `7` means "less than 7 days". So `-mtime -7` matches files that were modified within the past 7 days. 
  When you run this command, `find` will search within the specified directory (`/path/to/directory`) and its subdirectories for regular files that have been modified within the last 7 days. It will then list the paths of those files.
    - Searching for a specific string in files: `grep "search_string" /path/to/files*`. The command `grep "search_string" /path/to/files*` is used to search for a specific string, indicated by "search_string", within multiple files whose filenames match a specific pattern. Here's a breakdown of each component of the command:
      - **`grep`**: This is the command-line utility for searching text patterns in files.

        - **`"search_string"`**: This is the string you want to search for within the files. Replace `"search_string"` with the actual text you want to search for.

        - **`/path/to/files*`**: This specifies the path to the files you want to search within. The asterisk `*` is a wildcard character that matches any character or sequence of characters in filenames. So `/path/to/files*` would match all files in the directory `/path/to/` whose filenames start with `files`. When you run this command, `grep` will search for the specified string `"search_string"` within all files whose filenames match the pattern `/path/to/files*`. If any matches are found, `grep` will display the lines containing the search string along with the filename(s) where the string was found.

**Day 2: Advanced Permissions and Ownership**
- **Objective:** Understand advanced concepts of file permissions and ownership.
- **Topics Covered:**
    - Access control lists (ACLs) for fine-grained permissions (`setfacl` command).
    - Special permissions: Setuid, Setgid, and Sticky bit.
- **Practical Examples:**
    - Setting an ACL to grant read and write permissions to a specific user: `setfacl -m u:user:rw file.txt`
    - Setting the Setgid permission on a directory: `chmod g+s directory`
    - Setting the Sticky bit on a directory to prevent deletion by non-owners: `chmod +t directory`

**Day 3: Process Management**
- **Objective:** Learn how to manage processes effectively.
- **Topics Covered:**
    - Viewing running processes (`ps` command).
    - Managing processes: Killing, pausing, and resuming processes (`kill`, `killall`, `pkill`, `pgrep`, `top` commands).
    - Running commands in the background (`&` operator, `bg` and `fg` commands).
- **Practical Examples:**
    - Viewing running processes and their details: `ps aux | less`
    - Killing a process by PID: `kill PID`
    - Killing all processes with a specific name: `pkill process_name`
    - Running a command in the background: `command &`
    - Bringing a background process to the foreground: `fg`

**Day 4: Process Prioritization and Resource Control**
- **Objective:** Understand how to prioritize processes and control system resources.
- **Topics Covered:**
    - Process priority and scheduling (`nice` and `renice` commands).
    - Controlling resource limits with `ulimit` and `/etc/security/limits.conf`.
- **Practical Examples:**
    - Running a process with lower priority using `nice`: `nice -n 10 command`
    - Adjusting the priority of a running process with `renice`: `renice +5 PID`
    - Setting the maximum number of open files for a user: `ulimit -n 1000`
    - Configuring CPU time limits for a user in `/etc/security/limits.conf`.

**Day 5: Review and Practice**
- **Objective:** Review the concepts covered during the week and practice applying them in various scenarios.
- **Activities:**
    - Hands-on exercises covering advanced file management, process control, and resource management.
    - Q&A session to clarify any doubts or questions.
    - Assignments to reinforce learning, such as scripting exercises or troubleshooting scenarios.

**Homework Assignment:**
Practice the concepts covered during the week by working on additional exercises and challenges.
Experiment with different file management techniques, process control commands, and resource management strategies.
Document your findings and observations for discussion in the next class.

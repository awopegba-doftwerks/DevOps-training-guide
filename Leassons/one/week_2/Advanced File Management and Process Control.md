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
    - Compressing a file with gzip: `gzip file.txt`
    - Searching for files modified within the last 7 days: `find /path/to/directory -type f -mtime -7`
    - Searching for a specific string in files: `grep "search_string" /path/to/files*`

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

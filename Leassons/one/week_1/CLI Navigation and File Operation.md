**Lesson: Basic Command-Line Interface (CLI) Navigation and File Operations**

**Objective:**
By the end of this lesson, students will be able to navigate the command-line interface (CLI) of a Linux system and perform basic file operations.

**Introduction:**
The command-line interface (CLI) is a text-based interface used to interact with the operating system. Understanding CLI navigation and file operations is essential for efficiently managing files and directories in a Linux environment.

**Main Content:**

1. **CLI Navigation:**
   - **`pwd` (Print Working Directory):** Displays the current directory path.
     - Example: `pwd`
   - **`cd` (Change Directory):** Moves to a specified directory.
     - Example: `cd /path/to/directory`
   - **`ls` (List):** Lists files and directories in the current directory.
     - Example: `ls`
   - **`.` (Current Directory) and `..` (Parent Directory):** Represent the current directory and its parent directory, respectively.
     - Example: `cd .` (Stays in the current directory), `cd ..` (Moves to the parent directory).

2. **File Operations:**
   - **Creating Directories:** Use the `mkdir` command to create directories.
     - Example: `mkdir directory_name`
   - **Creating Files:** Use the `touch` command to create empty files.
     - Example: `touch file_name`
   - **Copying Files and Directories:** Use the `cp` command to copy files or directories.
     - Example: `cp source_file destination_file`, `cp -r source_directory destination_directory` (for directories).
   - **Moving or Renaming Files and Directories:** Use the `mv` command to move or rename files and directories.
     - Example: `mv old_file new_file`, `mv source_directory destination_directory`.
   - **Deleting Files and Directories:** Use the `rm` command to remove files and directories.
     - Example: `rm file_name`, `rm -r directory_name` (for directories).

**Examples:**

- **Navigating the File System:**
  - Navigate to the home directory: `cd ~`
  - List files and directories in the current directory: `ls`
  - Move to the Documents directory: `cd Documents`
  - List files in the Documents directory: `ls`

- **File Operations:**
  - Create a new directory named "Projects": `mkdir Projects`
  - Create a new file named "notes.txt": `touch notes.txt`
  - Copy the file "notes.txt" to the "Projects" directory: `cp notes.txt Projects/`
  - Rename the file "notes.txt" to "important_notes.txt": `mv notes.txt important_notes.txt`
  - Delete the file "important_notes.txt": `rm important_notes.txt`

**Conclusion:**
Mastering basic CLI navigation and file operations is essential for effective Linux system administration and development tasks. Practice these commands regularly to become proficient in working with files and directories in a command-line environment.

**Homework Assignment:**
Practice navigating the file system and performing basic file operations using the command-line interface. Create, copy, move, rename, and delete files and directories to reinforce your understanding of these concepts.

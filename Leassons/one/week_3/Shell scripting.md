# Shell Scripting
Shell scripting is a powerful tool for automating tasks on Unix-like operating systems such as Linux and macOS. It allows you to write scripts that execute a series of commands, making it easier to perform repetitive tasks efficiently. Here's a brief introduction to shell scripting:

1. **Choose a Shell**: The shell is the command-line interface that interprets your commands. Common shells include Bash (Bourne Again Shell), Zsh (Z Shell), and others. Bash is the most widely used and is the default on many systems.

2. **Create a Script File**: Start by creating a new file with a `.sh` extension, which indicates that it's a shell script. You can use any text editor to create this file.

3. **Shebang Line**: Begin your script with a shebang line, which tells the system which shell to use to execute the script. For Bash, the shebang line is `#!/bin/bash`.

4. **Write Your Script**: In the script file, write the commands you want to execute. These can be any commands you'd normally run in the terminal.

5. **Set Execution Permissions**: Before you can run the script, you need to give it execute permissions. You can do this with the `chmod` command: `chmod +x script.sh`.

6. **Execute the Script**: Run the script by typing its name preceded by `./`, like `./script.sh`, in the terminal.

Here's a simple example of a shell script that prints "Hello, World!":

```bash
#!/bin/bash

echo "Hello, World!"
```

Save this script in a file named `hello.sh`, set the execute permissions, and then run it. You should see "Hello, World!" printed to the terminal.

As you become more familiar with shell scripting, you can explore variables, control structures like loops and conditionals, functions, and more advanced features to build robust automation scripts tailored to your specific needs.


## Examples of shell scripting using relatable scenarios:

1. **Automating File Backup**:
   Imagine you have important documents on your computer that you want to back up regularly. You can create a shell script to automate this task. Here's a simplified version:

   ```bash
   #!/bin/bash

   # Define source and destination directories
   source_dir="/path/to/important/documents"
   backup_dir="/path/to/backup/location"

   # Create a timestamp for the backup folder
   timestamp=$(date +%Y%m%d%H%M%S)

   # Create the backup folder
   backup_folder="$backup_dir/backup_$timestamp"
   mkdir -p "$backup_folder"

   # Copy files from source to backup folder
   cp -r "$source_dir"/* "$backup_folder"
   
   echo "Backup completed successfully!"
   ```

   In this example, the script backs up documents from a specified directory to a backup location, creating a timestamped folder for each backup to keep track of versions.

2. **Batch Image Resizing**:
   Suppose you have a folder full of images that you need to resize for a website. Instead of resizing each image manually, you can automate the process with a shell script. Here's how it might look:

   ```bash
   #!/bin/bash

   # Define source and destination directories
   source_dir="/path/to/images"
   destination_dir="/path/to/resized/images"

   # Set the desired width and height for resized images
   width=800
   height=600

   # Loop through each image file and resize it
   for img_file in "$source_dir"/*.jpg; do
       filename=$(basename "$img_file")
       convert "$img_file" -resize "${width}x${height}" "$destination_dir/$filename"
   done
   
   echo "Image resizing completed successfully!"
   ```

   This script uses the `convert` command from the ImageMagick package to resize each JPEG image in a specified directory to the desired dimensions.

3. **Website Monitoring Script**: Suppose you run a small business website and want to monitor its uptime. You can write a shell script to periodically check if the website is accessible. Here's a simplified version:

```bash
#!/bin/bash

# Define website URL
website="http://example.com"

# Check if website is reachable
if curl --output /dev/null --silent --head --fail "$website"; then
    echo "Website $website is reachable."
else
    echo "Website $website is down!"
    # Send an email notification to the administrator
    mail -s "Website Down Alert" admin@example.com <<< "The website $website is down!"
fi
```

This script uses the `curl` command to check if the website is reachable. If it's down, it sends an email notification to the administrator.

4. **File Cleanup Script**: Imagine your downloads folder is cluttered with old files that you no longer need. You can write a shell script to clean up this folder by moving old files to an archive directory. Here's an example:

```bash
#!/bin/bash

# Define directories
downloads_dir="/path/to/downloads"
archive_dir="/path/to/archive"

# Move files older than 30 days to the archive directory
find $downloads_dir -type f -mtime +30 -exec mv {} $archive_dir \;
```

This script uses the `find` command to locate files older than 30 days in the downloads directory and moves them to the archive directory.

These examples demonstrate how shell scripting can be used to automate everyday tasks, making your life easier and more efficient.


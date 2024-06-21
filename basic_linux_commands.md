`sudo su` - Switching to root user.

`sudo <command-to-run>` - Runs any command with root privileges.

`mkdir <dir-name>` - Creates a new directory in current path.

`touch <file-name>` - Creates a new file in current path.

`vi <file-name>` - Enter into edit mode for a file.

`nano <file-name>` - Enter into edit mode for a file.

`cat <file-name>` - See the output of the file in read-only mode.

`rm -f <file-name>` - Deletes the file forcefully.

`rm -rf <dir-name>` - Deletes the folder and its subfolder forcefully.

`cp <old-path/file-name> <new-path/file-name>` - Copies the file from one path to other path. The same command is used to copy a directory as well.

`mv <old-path/file-name> <new-path/file-name>` - Moves the file from one path to other path. The same command is used to move a directory as well.

`cd ..` - Changes directory and goes one step back.

`cd /<particular-path>` - Goes to any particular path from current path.

`pwd` - To know present directory path.

`ls` - List out contents of the directory.

`ls -la` - List out all the contents including hidden files in the directory.

`clear` or `ctrl+l` - Clears the terminal screen.

`man <sub-command>` - To display the manual page for a specific command. It provides detailed information about the command, including its syntax, options, and examples. e.g. `man ls`

`uname` - Displays information about the system’s kernel, including the kernel name, hostname, kernel release, kernel version, and machine hardware name.

      Note: Some important flags you can use with the uname command.

                Use `uname -s` to display the kernel name.
                Use `uname -n` to display the hostname.
                Use `uname -r` to display the kernel release.
                Use `uname -v` to display the kernel version.
                Use `uname -m` to display the machine hardware name.

`whoami` - Displays the current user’s username.

`tar -cvf <archive name> <file-1 file-2 file-3>` - Used to create and extract archived files.

`tar -xvf <archive name>` - To extract an archive.

`zip <archive name> <file-1 file-2 file-3>` - Used to create and extract archived files.

`unzip <archive name>` - To extract an archive.

`<Any command with output> | grep "<string to find>"` - It searches for specific patterns or strings in one or more files and filter the output of other commands. e.g. `cat <file-name> | grep "<string-to-search>"` or `ls | grep "<file or dir to search>"`

`head <file-name>` - Displays first 10 lines of a file. Optionally, use `-n` flag followed by number of lines, you want to display. e.g. `head <file-name> -n 25`

`tail <file name>` - Displays last 10 lines of a file. Optionally, use `-n` flag followed by number of lines, you want to display. e.g. `tail <file-name> -n 25`

`ps -ef` - Displays a list of running processes.

`ps -p PID` - Display a list of all processes for a specific process ID.

`kill <process ID>` - Kills the process of the given process ID.

`df -h` - To display the amount of disk space used and available on the file systems.

`mount` - It is used to mount a file system or device to a specific directory. e.g. `mount /dev/cdrom /mnt` - In this case, `/dev/cdrom` is the device that needs to be mounted and `mnt` is the destination folder to which to mount the device

`chmod a+x <file-name>` - Adds executable permission to the existing permissions.

`chown user:user <file-name>` - This command changes the ownership of that file.

`ifconfig` - This command will give you the list of all the network interfaces along with the IP addresses, MAC addresses and other information about the interface.

`traceroute <destination address>` - This command is used to trace the route of network packets and determine the path they take to reach a specific destination.When working with `traceroute`, you can simply specify the IP address, hostname, or domain name of the endpoint.

`wget <link to file>` - Command to download any file from internet. When you specify the link for download, it has to directly be a link to the file. If the file cannot be accessed by the `wget` command, it will simply download the webpage in HTML format instead of the actual file that you wanted.

`wget -c <link to file>` - To resume an interrupted download.

`date` - Displays the date and time as per system format.

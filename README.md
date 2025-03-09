# Linux Commands Cheatsheet

This repository contains a comprehensive cheatsheet for Linux commands, organized by categories for easy reference. Whether you're a beginner or an experienced user, this cheatsheet will help you quickly find the commands you need for various tasks.
## Table of Contents | Categories

- **[File System Navigation](#file-system-navigation)**: Commands for navigating the file system, such as `pwd`, `ls`, and `cd`.
- **[File Operations](#file-operations)**: Commands for creating, copying, moving, and deleting files and directories, such as `touch`, `mkdir`, `cp`, `mv`, and `rm`.
- **[File Content](#file-content)**: Commands for viewing and searching file content, such as `cat`, `less`, `head`, `tail`, `grep`, `wc`, and `diff`.
- **[File Permissions](#file-permissions)**: Commands for managing file permissions and ownership, such as `chmod` and `chown`.
- **[Process Management](#process-management)**: Commands for managing processes, such as `ps`, `top`, `kill`, `bg`, `fg`, and `nohup`.
- **[System Information](#system-information)**: Commands for retrieving system information, such as `uname`, `hostname`, `df`, `du`, `free`, and `uptime`.
- **[Package Management](#package-management)**: Commands for managing packages on Debian/Ubuntu, Red Hat/Fedora, and Arch Linux systems.
- **[Network Commands](#network-commands)**: Commands for network configuration and troubleshooting, such as `ping`, `ifconfig`, `netstat`, `wget`, `curl`, `ssh`, and `scp`.
- **[Text Processing](#text-processing)**: Commands for processing text files, such as `echo`, `cut`, `sort`, `uniq`, `tr`, `sed`, and `awk`.
- **[Compression and Archiving](#compression-and-archiving)**: Commands for compressing and archiving files, such as `tar`, `gzip`, `gunzip`, `zip`, and `unzip`.
- **[User Management](#user-management)**: Commands for managing user accounts, such as `useradd`, `usermod`, `userdel`, `passwd`, `sudo`, and `su`.
- **[Special Operators](#special-operators)**: Operators for redirecting output, running commands in the background, and combining commands.
- **[System Control](#system-control)**: Commands for controlling the system, such as `shutdown`, `reboot`, `systemctl`, `journalctl`, `crontab`, `at`, `mount`, and `umount`.
- **[Shell Scripting Basics](#shell-scripting-basics)**: Basic syntax and commands for writing shell scripts, such as `#!/bin/bash`, `if`, `for`, `while`, `$variable`, `$()`, and `$(( ))`.

## File System Navigation

| Command  | Description                       | Example                                                        |
| -------- | --------------------------------- | -------------------------------------------------------------- |
| `pwd`    | Print working directory           | `pwd` → `/home/user`                                           |
| `ls`     | List directory contents           | `ls` → Lists files in current directory                        |
| `ls -l`  | List in long format               | `ls -l` → Shows detailed file information                      |
| `ls -a`  | List all files (including hidden) | `ls -a` → Shows hidden files starting with dot                 |
| `ls -lh` | List with human-readable sizes    | `ls -lh` → Shows sizes as KB, MB, etc.                         |
| `cd`     | Change directory                  | `cd Documents` → Move to Documents folder                      |
| `cd ..`  | Move up one directory             | `cd ..` → Move to parent directory                             |
| `cd ~`   | Change to home directory          | `cd ~` → Go to your home directory                             |
| `cd /`   | Change to root directory          | `cd /` → Go to system root                                     |
| `find`   | Find files/directories            | `find . -name "file.txt"` → Find file.txt in current directory |

## File Operations

| Command    | Description                    | Example                                                      |
| ---------- | ------------------------------ | ------------------------------------------------------------ |
| `touch`    | Create empty file              | `touch newfile.txt` → Creates empty newfile.txt              |
| `mkdir`    | Create directory               | `mkdir new_folder` → Creates new_folder directory            |
| `mkdir -p` | Create nested directories      | `mkdir -p dir1/dir2/dir3` → Creates directory tree           |
| `cp`       | Copy files/directories         | `cp file.txt backup/` → Copy file.txt to backup directory    |
| `cp -r`    | Copy directories recursively   | `cp -r folder backup/` → Copy folder and contents to backup  |
| `mv`       | Move/rename files              | `mv file.txt newname.txt` → Rename file.txt to newname.txt   |
| `mv`       | Move files to directory        | `mv file.txt Documents/` → Move file.txt to Documents folder |
| `rm`       | Remove files                   | `rm file.txt` → Delete file.txt                              |
| `rm -r`    | Remove directories recursively | `rm -r folder` → Delete folder and its contents              |
| `rm -f`    | Force remove files             | `rm -f file.txt` → Delete file without confirmation          |
| `rmdir`    | Remove empty directories       | `rmdir empty_folder` → Delete empty_folder if empty          |

## File Content

| Command   | Description               | Example                                                           |
| --------- | ------------------------- | ----------------------------------------------------------------- |
| `cat`     | Display file content      | `cat file.txt` → Shows content of file.txt                        |
| `less`    | View file with pagination | `less large_file.txt` → Browse through large_file.txt             |
| `head`    | Show first part of file   | `head -n 10 file.txt` → Display first 10 lines                    |
| `tail`    | Show last part of file    | `tail -n 20 file.txt` → Display last 20 lines                     |
| `tail -f` | Monitor file changes      | `tail -f /var/log/syslog` → Show and follow log updates           |
| `grep`    | Search text in files      | `grep "search term" file.txt` → Find "search term" in file.txt    |
| `grep -r` | Recursive search          | `grep -r "term" /home/user` → Search in all files under directory |
| `wc`      | Count lines, words, chars | `wc -l file.txt` → Count lines in file.txt                        |
| `diff`    | Compare files             | `diff file1.txt file2.txt` → Show differences between files       |

## File Permissions

| Command    | Description                    | Example                                                                |
| ---------- | ------------------------------ | ---------------------------------------------------------------------- |
| `chmod`    | Change file permissions        | `chmod 755 script.sh` → Set rwx-rx-rx permissions                      |
| `chmod +x` | Make file executable           | `chmod +x script.sh` → Add execute permission                          |
| `chmod -R` | Change permissions recursively | `chmod -R 755 directory/` → Set permissions for all files in directory |
| `chown`    | Change file owner              | `chown user:group file.txt` → Change owner and group                   |
| `chown -R` | Change owner recursively       | `chown -R user directory/` → Change owner for directory and contents   |

## Process Management

| Command   | Description                   | Example                                                     |
| --------- | ----------------------------- | ----------------------------------------------------------- |
| `ps`      | Show running processes        | `ps` → List your processes                                  |
| `ps aux`  | Show all processes            | `ps aux` → List all processes with details                  |
| `top`     | Interactive process viewer    | `top` → Show real-time process activity                     |
| `htop`    | Enhanced process viewer       | `htop` → Interactive process viewer (may need installation) |
| `kill`    | Terminate process             | `kill 1234` → Terminate process with PID 1234               |
| `kill -9` | Force terminate process       | `kill -9 1234` → Forcefully kill process                    |
| `killall` | Kill processes by name        | `killall firefox` → Kill all Firefox processes              |
| `bg`      | Send process to background    | `bg` → Resume suspended job in background                   |
| `fg`      | Bring process to foreground   | `fg` → Bring last background job to foreground              |
| `jobs`    | List background jobs          | `jobs` → Show background processes                          |
| `nohup`   | Run command immune to hangups | `nohup command &` → Run in background, persist after logout |

## System Information

| Command       | Description                | Example                                                |
| ------------- | -------------------------- | ------------------------------------------------------ |
| `uname`       | Show system information    | `uname -a` → Display all system info                   |
| `uname -r`    | Show kernel version        | `uname -r` → Display kernel release                    |
| `lsb_release` | Show distribution info     | `lsb_release -a` → Display Linux distribution details  |
| `hostname`    | Show system hostname       | `hostname` → Display computer name                     |
| `whoami`      | Show current username      | `whoami` → Display your username                       |
| `id`          | Show user identity         | `id` → Display user and group IDs                      |
| `df`          | Show disk usage            | `df -h` → Show disk space in human-readable format     |
| `du`          | Show directory space usage | `du -h directory/` → Show directory size               |
| `free`        | Show memory usage          | `free -h` → Display RAM usage in human-readable format |
| `uptime`      | Show system uptime         | `uptime` → Show how long system has been running       |

## Package Management

### Debian/Ubuntu (APT)

| Command       | Description          | Example                                                        |
| ------------- | -------------------- | -------------------------------------------------------------- |
| `apt update`  | Update package lists | `sudo apt update` → Refresh available package info             |
| `apt upgrade` | Upgrade packages     | `sudo apt upgrade` → Upgrade all installed packages            |
| `apt install` | Install packages     | `sudo apt install package_name` → Install new package          |
| `apt remove`  | Remove packages      | `sudo apt remove package_name` → Uninstall package             |
| `apt search`  | Search packages      | `apt search keyword` → Find packages matching keyword          |
| `apt list`    | List packages        | `apt list --installed` → Show installed packages               |
| `dpkg -i`     | Install .deb file    | `sudo dpkg -i package.deb` → Install from downloaded .deb file |

### Red Hat/Fedora (DNF/YUM)

| Command            | Description       | Example                                                       |
| ------------------ | ----------------- | ------------------------------------------------------------- |
| `dnf check-update` | Check for updates | `sudo dnf check-update` → Check for package updates           |
| `dnf upgrade`      | Upgrade packages  | `sudo dnf upgrade` → Upgrade all packages                     |
| `dnf install`      | Install packages  | `sudo dnf install package_name` → Install new package         |
| `dnf remove`       | Remove packages   | `sudo dnf remove package_name` → Uninstall package            |
| `dnf search`       | Search packages   | `dnf search keyword` → Find packages matching keyword         |
| `dnf list`         | List packages     | `dnf list installed` → Show installed packages                |
| `rpm -i`           | Install .rpm file | `sudo rpm -i package.rpm` → Install from downloaded .rpm file |

### Arch Linux (Pacman)

| Command       | Description           | Example                                                  |
| ------------- | --------------------- | -------------------------------------------------------- |
| `pacman -Sy`  | Sync package database | `sudo pacman -Sy` → Update package database              |
| `pacman -Syu` | Update system         | `sudo pacman -Syu` → Update package database and upgrade |
| `pacman -S`   | Install packages      | `sudo pacman -S package_name` → Install new package      |
| `pacman -R`   | Remove packages       | `sudo pacman -R package_name` → Uninstall package        |
| `pacman -Ss`  | Search packages       | `pacman -Ss keyword` → Find packages matching keyword    |
| `pacman -Q`   | List packages         | `pacman -Q` → Show installed packages                    |

## Network Commands

| Command      | Description             | Example                                                               |
| ------------ | ----------------------- | --------------------------------------------------------------------- |
| `ping`       | Test connectivity       | `ping google.com` → Check connection to google.com                    |
| `ifconfig`   | Show network interfaces | `ifconfig` → Display network interface configuration                  |
| `ip addr`    | Modern interface config | `ip addr` → Show IP addresses and network interfaces                  |
| `netstat`    | Network statistics      | `netstat -tuln` → Show active network connections                     |
| `ss`         | Socket statistics       | `ss -tuln` → Modern replacement for netstat                           |
| `wget`       | Download files          | `wget https://example.com/file.zip` → Download file                   |
| `curl`       | Transfer data           | `curl https://example.com` → Fetch web page content                   |
| `ssh`        | Secure shell            | `ssh user@hostname` → Connect to remote server                        |
| `scp`        | Secure copy             | `scp file.txt user@hostname:/path/` → Copy file to remote server      |
| `rsync`      | Remote sync             | `rsync -avz folder/ user@host:/path/` → Sync directory to remote host |
| `dig`        | DNS lookup              | `dig example.com` → Query DNS for domain                              |
| `nslookup`   | Name server lookup      | `nslookup example.com` → Query DNS for domain                         |
| `traceroute` | Trace network path      | `traceroute google.com` → Show path packets take to server            |

## Text Processing

| Command | Description                 | Example                                                     |
| ------- | --------------------------- | ----------------------------------------------------------- |
| `echo`  | Print text                  | `echo "Hello World"` → Display text                         |
| `cut`   | Extract sections from lines | `cut -d "," -f 1 file.csv` → Extract first column from CSV  |
| `sort`  | Sort lines                  | `sort file.txt` → Sort file content alphabetically          |
| `uniq`  | Remove duplicates           | `sort file.txt \| uniq` → Show unique sorted lines          |
| `tr`    | Translate characters        | `cat file.txt \| tr '[a-z]' '[A-Z]'` → Convert to uppercase |
| `sed`   | Stream editor               | `sed 's/old/new/g' file.txt` → Replace "old" with "new"     |
| `awk`   | Pattern scanning            | `awk '{print $1}' file.txt` → Print first column            |

## Compression and Archiving

| Command  | Description         | Example                                                      |
| -------- | ------------------- | ------------------------------------------------------------ |
| `tar`    | Archive files       | `tar -cf archive.tar files/` → Create tar archive            |
| `tar -x` | Extract archive     | `tar -xf archive.tar` → Extract tar archive                  |
| `tar -z` | Compress with gzip  | `tar -czf archive.tar.gz files/` → Create compressed archive |
| `gzip`   | Compress files      | `gzip file.txt` → Compress to file.txt.gz                    |
| `gunzip` | Decompress gzip     | `gunzip file.txt.gz` → Decompress gzip file                  |
| `zip`    | Create zip archive  | `zip -r archive.zip directory/` → Compress directory to zip  |
| `unzip`  | Extract zip archive | `unzip archive.zip` → Extract zip archive                    |

## User Management

| Command   | Description          | Example                                                |
| --------- | -------------------- | ------------------------------------------------------ |
| `useradd` | Create user          | `sudo useradd newuser` → Create new user account       |
| `usermod` | Modify user          | `sudo usermod -aG group user` → Add user to a group    |
| `userdel` | Delete user          | `sudo userdel username` → Delete user account          |
| `passwd`  | Change password      | `passwd` → Change your password                        |
| `sudo`    | Execute as superuser | `sudo command` → Run command with superuser privileges |
| `su`      | Switch user          | `su username` → Switch to another user account         |
| `groups`  | Show user groups     | `groups username` → Show groups a user belongs to      |

## Special Operators

| Operator | Description       | Example                                                             |
| -------- | ----------------- | ------------------------------------------------------------------- |
| `>`      | Redirect output   | `command > file.txt` → Save output to file.txt                      |
| `>>`     | Append output     | `command >> file.txt` → Append output to file.txt                   |
| `<`      | Input redirection | `command < file.txt` → Use file.txt as input                        |
| `\|`      | Pipe output       | `command1 \| command2` → Use output of command1 as input to command2 |
| `&`      | Run in background | `command &` → Run command in the background                         |
| `&&`     | Logical AND       | `command1 && command2` → Run command2 if command1 succeeds          |
| `\|\|`     | Logical OR        | `command1 \|\| command2` → Run command2 if command1 fails             |
| `;`      | Command separator | `command1 ; command2` → Run command2 after command1                 |

## System Control

| Command            | Description              | Example                                                 |
| ------------------ | ------------------------ | ------------------------------------------------------- |
| `shutdown`         | Shutdown system          | `sudo shutdown -h now` → Shutdown immediately           |
| `reboot`           | Restart system           | `sudo reboot` → Restart immediately                     |
| `systemctl`        | Control systemd services | `sudo systemctl start service` → Start a service        |
| `systemctl status` | Check service status     | `systemctl status service` → Show service status        |
| `journalctl`       | View logs                | `journalctl -u service` → View logs for a service       |
| `crontab`          | Schedule tasks           | `crontab -e` → Edit cron jobs                           |
| `at`               | Schedule one-time tasks  | `at now + 1 hour` → Schedule task in 1 hour             |
| `mount`            | Mount filesystems        | `sudo mount /dev/sdb1 /mnt` → Mount device to directory |
| `umount`           | Unmount filesystems      | `sudo umount /mnt` → Unmount directory                  |

## Shell Scripting Basics

| Command/Syntax     | Description                  | Example                                                   |
| ------------------ | ---------------------------- | --------------------------------------------------------- |
| `#!/bin/bash`      | Shebang line                 | First line of script to specify interpreter               |
| `if [ condition ]` | Conditional statement        | `if [ "$a" -eq "$b" ]; then echo "Equal"; fi`             |
| `for loop`         | Loop through items           | `for i in {1..5}; do echo $i; done`                       |
| `while loop`       | Loop while condition is true | `while [ $i -lt 10 ]; do echo $i; i=$((i+1)); done`       |
| `$variable`        | Variable reference           | `echo $HOME` → Display HOME variable value                |
| `$()`              | Command substitution         | `echo "Date: $(date)"` → Include command output in string |
| `$(())`            | Arithmetic expansion         | `echo $((5+3))` → Perform arithmetic                      |


## Contributing

Contributions are welcome! If you have any suggestions, improvements, or additional commands that you think should be included in this cheatsheet, please feel free to submit a pull request or open an issue on GitHub.

To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

- [Linux Documentation Project](http://www.tldp.org/)
- [Linux Command](https://linuxcommand.org/)
- [SS64](https://ss64.com/bash/)
- [TLDP Advanced Bash-Scripting Guide](http://tldp.org/LDP/abs/html/)

Thank you to all the contributors and the open-source community for their valuable resources and support.

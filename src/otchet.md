## Part 1. Installation of the OS

**== Task ==**

##### Install **Ubuntu 20.04 Server LTS** without GUI. (Use VirtualBox).
- There should be no GUI.
- Check Ubuntu version by running the command \
  `cat /etc/issue`
- Add a screenshot of the command output to the report.

**== Execution ==**

![task1](./screenshots/task1.png)

## Part 2. Creating a user

**== Task ==**

## Create a user other than the one created during installation. The user must be added to `adm` group.
- Add a screenshot of command call to create user.
- The new user must be in the output of the command: \
  `cat /etc/passwd`
- Add a screenshot of the command output.

**== Execution ==**

![task21](./screenshots/task21.png)

![task211](./screenshots/task211.png)

## Part 3. Setting up the OS network

**== Task ==**

## Set the machine name as user-1
## Set the time zone corresponding to your current location.

## Output the names of the network interfaces using a console command.
- In the report give an explanation for the presence of the lo interface.
## Use the console command to get the ip address of the device you are working on from the DHCP server.
- Decode DHCP in the report.
## Define and display the external ip address of the gateway (ip) and the internal IP address of the gateway, aka default ip address (gw).
## Set static (manually set, not received from DHCP server) ip, gw, dns settings (use public DNS servers, e.g. 1.1.1.1 or 8.8.8.8).

## Reboot the virtual machine. Make sure that the static network settings (ip, gw, dns) correspond to those set in the previous point.
- Describe in the report what you have done to complete all seven points (you can do it in text or with screenshots).
- Successfully ping 1.1.1.1 and ya.ru remote hosts and add a screenshot of the output command to the report. There should be "0% packet loss" phrase in command output.

**== Execution ==**

## Settting a new name for the machine:
![task31](./screenshots/task31.png)
![task311](./screenshots/task311.png)

## Setting the time zone Asia/Novosibirsk:
![task32](./screenshots/task32.png)

## Output the names of network intefraces:
![task33](./screenshots/task33.png)

`---` lo (loopback device) - virtual interface present by default in any Linux. It is used to debug network programs and run server application on a local machine. 

## Getting the devices IP address from DHCP
![task34](./screenshots/task34.png)

`---`DHCP (Dynamic Host Configuration Protocol) - application protocol that allows nerwotk devices to automatically recive an IP address and other parameters necessary to work in a TCP/IP.

## Determining the defailt IP address:
![task35](./screenshots/task35.png)

## Setting static ip, gw, dns settings:
![task36](./screenshots/task36.png)

## Reboot machine and cheching ip, gw, dns:
![task37](./screenshots/task37.png)

## Ping ya.ru and 1.1.1.1 servers:
![task371](./screenshots/task371.png)

## Part 4. OS Update

**== Task ==**

## Update the system packages to the latest version
- After updating the system packages, if you enter the update command again, a message should appear saying there are no updates.
- Add a screenshot of this message to the report.

**== Execution ==**

## System update:
![task41](./screenshots/task41.png)
![task411](./screenshots/task411.png)

## Checking update:
![task42](./screenshots/task42.png)

## Part 5. Using the **sudo** command

**== Task ==**

##### Allow user created in [Part 2](#part-2-creating-a-user) to execute sudo command.
- In the report explain the *true* purpose of sudo command (don’t write about the fact that this word is "magic" one).
- Change the OS hostname via the user created in [Part 2](#part-2-creating-a-user) (using sudo).
- Add screenshot with changed hostname to the report.

**== Execution ==**

`---` sudo - program for Unix-like computer OS that enables users to run programs with the security privileges of another user.

## Setting new permission for second user from Part 2:
![task51](./screenshots/task51.png)

## Load second user:
![task52](./screenshots/task52.png)

## Prove for change name after reboot machine:
![task521](./screenshots/task521.png)

## Part 6. Installing and configuring the time service

**== Task ==**

##### Set up the automatic time synchronisation service.
- Output the time of the time zone in which you are currently located.
- The output of the following command must contain `NTPSynchronized=yes`: \
  `timedatectl show`
- Add screenshots of the correct time and command output to the report.

**== Execution ==**

## Output my time zone:
![task61](./screenshots/task61.png)

## Part 7. Installing and using text editors

**== Task ==**

##### Install **VIM** text editor (+ any two others if you like **NANO**, **MCEDIT**, **JOE** etc.)

##### Using each of the three selected editors, create a *test_X.txt* file, where X is the name of the editor in which the file is created. Write your nickname in it, close the file and save the changes.
- Add screenshots to the report:
    - Of each editor with the contents of the file before closing.
- Write down in the report what you have done to exit with the changes saved.

##### Using each of the three selected editors, open the file for editing, edit the file by replacing the nickname with the "21 School 21" string, close the file without saving the changes.
- Add screenshots to the report:
    - Of each editor with the contents of the file after editing.
- Write down in the report what you have done to exit without saving the changes.
##### Using each of the three selected editors, edit the file again (similar to the previous point) and then master the functions of searching through the contents of a file (a word) and replacing a word with any other one.
- Add screenshots to the report:
    - Of each editor with word search results.
    - Of each editor with commands entered to replace a word with another.

**== Execution ==**

##### Installing JOE (nano and vim was on my VM):
![task71](./screenshots/task71.png)

```VIM```

## Working with VIM:

##### Editing and saving: 
`Im used ':x' for edit and save`
![task72VIM](./screenshots/task72VIM.png)

##### Exit without saving:
`Im used '!q'`
![task721VIM](./screenshots/task721VIM.png)
![task7211VIM](./screenshots/task7211VIM.png)

##### Find and replacement:
`Im used /21 for find '21' and :s/21/42/g 2 for replace two 21 symbols on 42`
![task73VIM](./screenshots/task73VIM.png)
![task731VIM](./screenshots/task731VIM.png)

```NANO```

##### Working with NANO:

##### Editing and saving: 
`For exit press Ctrl+X and then accept to save with Y`
![task7NANO1](./screenshots/task7NANO.png)

##### Exit without saving:
`Exit and press N`
![task7NANO2](./screenshots/task7NANO1.png)
![task7NANO3](./screenshots/task7NANO2.png)

##### Find and replacement:
`Press Ctrl+W+Enter and write what u wanna change, after Enter press Ctrl+R and write what u wanna replace`
![task7NANO4](./screenshots/task7NANO3.png)
![task7NANO5](./screenshots/task7NANO4.png)
![task7NANO6](./screenshots/task7NANO5.png)

```JOE```

##### Working with JOE: 

##### Editing and saving: 
`For exit and save u need to use Ctrl+K+Q and then Y`
![task7JOE](./screenshots/task7JOE.png)

##### Exit without saving:
`For exit and not save u need to use Ctrl+K+Q and then N`
![task7JOE1](./screenshots/task7JOE1.png)
![task7JOE2](./screenshots/task7JOE2.png)

##### Find and replacement:
`For find u neen to press Ctrl+K+F, input what u want and press Enter dooble times. For replacement press Ctrl+K+F+Enter and R, input text-switch and Enter`
![task7JOE3](./screenshots/task7JOE3.png)
![task7JOE4](./screenshots/task7JOE4.png)
![task7JOE5](./screenshots/task7JOE5.png)

## Part 8. Installing and basic setup of the **SSHD** service

**== Task ==**

## Install the SSHd service.
## Add an auto-start of the service whenever the system boots.
## Reset the SSHd service to port 2022.
## Show the presence of the sshd process using the ps command. To do this, you need to match the keys to the command.
- Explain in the report the meaning of the command and each key in it.
## Reboot the system.
- Describe in the report what you have done to complete all five points (you can do this in text or with screenshots).
- The output of the netstat -tan command should contain \
  `tcp 0 0.0.0.0:2022 0.0.0.0:* LISTEN` \
  (if there is no netstat command, it needs to be installed)
- Add a screenshot of the command output to the report.
- Explain the meaning of the -tan keys, the value of each output column, the value 0.0.0.0. in the report.

**== Execution ==**

## Installing and add ssh in the autoload:
![task81](./screenshots/task81.png)

## Resetting SSHd to the 2022 port:
![task82](./screenshots/task82.png)

## Using ps and grep for search proccess of SSHd
![task83](./screenshots/task83.png)

## Reboot the system:
![task84](./screenshots/task84.png)

## Keys which I used for search:
##### -t (--tcp) --- show just TCP ports
##### -a (--all) --- show condition all sokets
##### -n (--numeric) --- show addresses as numbers

## All columns:

##### Proto is the protocol used by the socket. Since the [-t | --tcp] option was used, only TCP sockets are present in the output.
##### Recv-Q is a counter of bytes not copied by the user's program from this socket.
##### Send-Q is a counter of bytes not confirmed by the remote node.
##### Local Address - the address and port number of the local end of the socket. If the [-n | --numeric] option is specified, output in the format [socket address:port number], otherwise - [canonical node name:corresponding service name]. In the line we are interested in, # 0.0.0.0 is the address of the local end of the socket, 2022 is the port number, which we changed from 22 to 2022. Address 0.0.0.0 means that the remote end of the socket will be accessible to all local ip addresses.
##### Foreign Address - the address and port number of the remote end of the socket.
##### State - the state of the socket. The LISTEN state means that the socket is waiting for incoming connections.

## Part 9. Installing and using the **top**, **htop** utilities

**== Task ==**

##### Install and run the top and htop utilities.
- From the output of the top command determine and write in the report:
    - uptime
    - number of authorised users
    - total system load
    - total number of processes
    - cpu load
    - memory load
    - pid of the process with the highest memory usage
    - pid of the process taking the most CPU time
- Add a screenshot of the htop command output to the report:
    - sorted by PID, PERCENT_CPU, PERCENT_MEM, TIME
    - filtered for sshd process
    - with the syslog process found by searching
    - with hostname, clock and uptime output added

**== Execution ==**

###### Top:
![task932](./screenshots/task9.png)

##### Top utility uptime:
![task9432](./screenshots/task9UP.png)

##### Numbers of authoriser users:
![task9423](./screenshots/task9U.png)

##### Total system load - system load avg over the last 1, 5, 15 mins:
![task9124](./screenshots/task9LA.png)

##### Total number of processes - shows total tasks or threads, depending on the state of the Threads-mode toggle:
![task9523](./screenshots/task9ALL.png)

##### Work with htop:
![task9214](./screenshots/task9onPID.png)

##### CPU:
![task9CPU](./screenshots/task9CPU.png)

##### MEM:
![task9MEM](./screenshots/task9MEM.png)

##### Time:
![task9Time](./screenshots/task9Time.png)

##### Sorting by SSHd:
![task9S](./screenshots/task9S.png)

##### Searching syslog:
![task9sy](./screenshots/task9sy.png)

##### Clock, uptime and hostname:
![task9cuh](./screenshots/task9cuh.png)

## Part 10. Using the **fdisk** utility

**== Task ==**

##### Run the fdisk -l command.
- In the report write the name of the hard disk, its capacity and number of sectors, and also the swap size.

**== Execution ==**

##### sudo fdisk -l > duskinfo.txt; vim diskinfo.txt
![task10](./screenshots/task10.png)

# Name: /dev/sda
# Space: 10 GiB
# Sectors: 20971520
# swap: 1.9 Gi

## Part 11. Using the **df** utility

**== Task ==**

##### Run the df command.
- In the report write for the root partition (/):
    - partition size
    - space used
    - space free
    - percentage used
- Determine and write the measurement unit in the report.

##### Run the df -Th command.
- In the report write for the root partition (/):
    - partition size
    - space used
    - space free
    - percentage used
- Determine and write the file system type for the partition in the report.

**== Execution ==**

##### Output from df command:
![task11](./screenshots/task11.png)

# size: 16445308 
# used: 6458136   
# free space: 9132084  
# used in percent: 42%
# 1K-block = 1024 bytes

##### Output from df -Th command:
![task111](./screenshots/task111.png)

# size: 16G  
# used: 6.2G  
# free space: 8.8G  
# used in percent: 42%

## df -Th: '-T' - print system files, '-h' - print size in human-readable format (1024).

## Part 12. Using the **du** utility

**== Task ==**

##### Run the du command.
##### Output the size of the /home, /var, /var/log folders (in bytes, in human readable format)
##### Output the size of all contents in /var/log (not the total, but each nested element using *)
- Add screenshots with the output of all used commands to the report.

**== Execution ==**

##### Output from du for /home, /var, /var/log in bytes and then in human-readable format:
![task12](./screenshots/task12.png)

##### Size all files from /var/log/*:
![task121](./screenshots/task121.png)


## Part 13. Installing and using the **ncdu** utility

**== Task ==**

##### Install the ncdu utility.
##### Output the size of the /home, /var, /var/log folders.
- The size should be approximately the same as in [Part 12](#part-12-using-the-du-utility).

- Add screenshots of the used commands to the report.

**== Execution ==**

##### Output from ncdu:
# /home and /var:
![task13](./screenshots/task13.png)

# /var/log:
![task131](./screenshots/task131.png)


## Part 14. Working with system logs

**== Task ==**

##### Open for viewing:
##### 1. /var/log/dmesg
##### 2. /var/log/syslog
##### 3. /var/log/auth.log
- Write the last successful login time, user name and login method in the report.
- Restart SSHd service.
- Add a screenshot of the service restart message to the report (search for it in the logs).

**== Execution ==**

##### I used VIM for checking all files:

# /var/log/dmesg:
![task131](./screenshots/task14.png)

# /var/log/syslog:
![task131](./screenshots/task141.png)

# /var/log/auth.log: 
![task131](./screenshots/task142.png)

# Infomation about authorization:
![task131](./screenshots/task143.png)

# Restart SSHd and check it in logs /var/log/syslog:
![task131](./screenshots/task144.png)

## Part 15. Using the **CRON** job scheduler

**== Task ==**

##### Using the job scheduler, run the uptime command in every 2 minutes.
- Find lines in the system logs (at least two within a given time range) about the execution.
- Display a list of current jobs for CRON.
- Add screenshots of the execution lines and the list of current tasks to the report.

##### Remove all tasks from the job scheduler.
- Add a screenshot of the list of current tasks for CRON to the report.

**== Execution ==**

# For remake cron file: 
`crontab -e`

# For check this file:
`crontab -l`
![task131](./screenshots/task15.png)

# Write in /var/log/syslog:
![task131](./screenshots/task151.png)

# For delete all cron files:
`crontab -r`

![task131](./screenshots/task152.png)

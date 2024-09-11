<h1>Backup Ubuntu Server Full</h1>


<h2>Description</h2>
The project consists of an Bash script that performs a full backup of a volume on Ubuntu Linux to a backup drive.<br/>

<h2>Language</h2>

- <b>Bash</b>

<h2>Environments Used </h2>

- <b>Ubuntu 22.04.4 LTS</b>

<h2>Setup</h2>


  1. Create /opt/backup directory:</br>
    $ sudo mkdir /opt/backup

  2. Create /opt/backup/backup_server_full.sh and copy contents of backup_server_full.sh.txt</br>
    into /opt/backup/backup_server_full.sh:</br>
    $ sudo nano /opt/backup/backup_server_full.sh

  3. Grant the execute permissions to /opt/backup/backup_server_full.sh:</br>
    $ sudo chmod +x /opt/backup/backup_server_full.sh
    
  4. Setup Cron Jobs to run the backup scripts at selected times:</br>
    $ sudo crontab -e

  5. Add the following lines to crontab:</br>
  
    <span>#</span> Run backup_server_full.sh every Sunday at 12:00pm.</br>
    0 12 * * 0 /opt/backup/backup_server_full.sh > /dev/null 2>&1</br>
</br>
</br>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

# Linux-Commands
---

### PostgreSQL Database Backup

**Command:**
```bash
pg_dump -U ringoncore -d ringoncore -f ringoncore.sql -h localhost
```

---

### Securely Copy a File to a Remote Server

**Command:**
```bash
scp ringoncore.sql root@73.88.91.174
```

---

### Connect to a PostgreSQL Database Using `psql`

**Command:**
```bash
psql -h localhost -U ringoncore -d ringoncore
```

---

### Real-Time SIP Packet Analysis with `sngrep`

**Command:**
```bash
sngrep
```

---

### Check if Docker is Running

**Command:**
```bash
ps aux | grep docker
```

---

### Terminate a Process by Name with `pkill`

#### **Kill a Process by Name**
```bash
pkill sngrep
```

#### **Force Kill a Stuck Process**
```bash
pkill -9 chrome
```

#### **Kill All Instances of a Process**
```bash
pkill python
```

#### **Kill Processes by User**
```bash
pkill -u nishant
```

#### **Match Process Command Line**
```bash
pkill -f java
```

#### **Case-Insensitive Match**
```bash
pkill -i myprocess
```

#### **Preview Processes Before Killing**
```bash
pgrep -fl sngrep
```

---

### Monitoring Commands for Linux Systems

---

### **Real-Time Process Monitoring**

**Command:**
```bash
top
```

**Alternative:** More user-friendly interface for system monitoring:
```bash
htop
```

---

### **Monitor Disk I/O Usage**

**Command:**
```bash
iotop
```

---

### **Monitor Network Usage**

**Command:**
```bash
nload
```

**Alternative:**
```bash
iftop
```

---

### **System Performance and Resource Monitoring**

**Command:**
```bash
vmstat 1
```

---

### **Monitor Disk Usage**

**Command:**
```bash
iostat -x 1
```

---

### **Monitor Free and Used Memory**

**Command:**
```bash
free -h
```

---

### **Monitor Network Connections**

**Command:**
```bash
netstat -tuln
```

---

### **Monitor Specific Logs in Real-Time**

**Command:**
```bash
tail -f /var/log/syslog
```

**For Specific Application Logs:**
```bash
tail -f /var/log/nginx/access.log
```

---

### **Monitor System Load Average**

**Command:**
```bash
uptime
```

---

### **CPU and Memory Usage of a Specific Process**

**Command:**
```bash
ps -p <pid> -o %cpu,%mem,cmd
```

---

### **Real-Time Network Packet Monitoring**

**Command:**
```bash
tcpdump
```

---

### **Real-Time Disk Usage Monitoring**

**Command:**
```bash
watch -n 1 df -h
```

---

### **Monitor System D-Bus Events**

**Command:**
```bash
dbus-monitor
```

---

### **View All Active Connections**

**Command:**
```bash
ss -tulwn
```

---

### **Monitor Services with Systemd**

**Command:**
```bash
systemctl list-units --type=service --state=running
```

---

### **Real-Time Monitoring with Glances**

**Command:**
```bash
glances
```

---

### Deploying to a Web Server (Nginx/Apache)

Follow these steps to deploy the updated build of your application to a web server:

### **1. Replace Existing Build:**

1. **Copy the Contents of the New Build or `dist` Folder**:
   - Use the following command to copy your newly built application files to your server's web root directory (`/var/www/html/` for Nginx or Apache):
     ```bash
     sudo cp -r ./build/* /var/www/html/
     ```

2. **Restart the Web Server**:
   - After copying the new files, restart your web server to apply the changes:
     ```bash
     sudo systemctl restart nginx
     ```
   - If you are using Apache, replace `nginx` with `apache2`:
     ```bash
     sudo systemctl restart apache2
     ```

---

### Creating a Snapshot of Your Code

To take a snapshot of your code before making any changes, you can compress the entire project directory. This will allow you to back up the current state of your code:

### **1. Compress the Folder**:

You can use either the `tar` or `zip` command to create an archive of your code.

#### **Using `tar`**:
```bash
tar -czvf snapshot.tar.gz /path/to/your/code
```

- This will create a `tar.gz` compressed archive of the `code` directory.

#### **Using `zip`**:
```bash
zip -r snapshot.zip /path/to/your/code
```

# Networking and Process Monitoring Commands

---

### PostgreSQL Database Backup

**Command:**
```bash
pg_dump -U ringoncore -d ringoncore -f ringoncore.sql -h localhost
```

---

### Securely Copy a File to a Remote Server

**Command:**
```bash
scp ringoncore.sql root@73.88.91.174
```

---

### Connect to a PostgreSQL Database Using `psql`

**Command:**
```bash
psql -h localhost -U ringoncore -d ringoncore
```

---

### Real-Time SIP Packet Analysis with `sngrep`

**Command:**
```bash
sngrep
```

---

### Check if Docker is Running

**Command:**
```bash
ps aux | grep docker
```

---

### Terminate a Process by Name with `pkill`

#### **Kill a Process by Name**
```bash
pkill sngrep
```

#### **Force Kill a Stuck Process**
```bash
pkill -9 chrome
```

#### **Kill All Instances of a Process**
```bash
pkill python
```

#### **Kill Processes by User**
```bash
pkill -u nishant
```

#### **Match Process Command Line**
```bash
pkill -f java
```

#### **Case-Insensitive Match**
```bash
pkill -i myprocess
```

#### **Preview Processes Before Killing**
```bash
pgrep -fl sngrep
```

---

### Monitoring Commands for Linux Systems

---

### **Real-Time Process Monitoring**

**Command:**
```bash
top
```

**Alternative:** More user-friendly interface for system monitoring:
```bash
htop
```

---

### **Monitor Disk I/O Usage**

**Command:**
```bash
iotop
```

---

### **Monitor Network Usage**

**Command:**
```bash
nload
```

**Alternative:**
```bash
iftop
```

---

### **System Performance and Resource Monitoring**

**Command:**
```bash
vmstat 1
```

---

### **Monitor Disk Usage**

**Command:**
```bash
iostat -x 1
```

---

### **Monitor Free and Used Memory**

**Command:**
```bash
free -h
```

---

### **Monitor Network Connections**

**Command:**
```bash
netstat -tuln
```

---

### **Monitor Specific Logs in Real-Time**

**Command:**
```bash
tail -f /var/log/syslog
```

**For Specific Application Logs:**
```bash
tail -f /var/log/nginx/access.log
```

---

### **Monitor System Load Average**

**Command:**
```bash
uptime
```

---

### **CPU and Memory Usage of a Specific Process**

**Command:**
```bash
ps -p <pid> -o %cpu,%mem,cmd
```

---

### **Real-Time Network Packet Monitoring**

**Command:**
```bash
tcpdump
```

---

### **Real-Time Disk Usage Monitoring**

**Command:**
```bash
watch -n 1 df -h
```

---

### **Monitor System D-Bus Events**

**Command:**
```bash
dbus-monitor
```

---

### **View All Active Connections**

**Command:**
```bash
ss -tulwn
```

---

### **Monitor Services with Systemd**

**Command:**
```bash
systemctl list-units --type=service --state=running
```

---

### **Real-Time Monitoring with Glances**

**Command:**
```bash
glances
```

---

### Deploying to a Web Server (Nginx/Apache)

Follow these steps to deploy the updated build of your application to a web server:

### **1. Replace Existing Build:**

1. **Copy the Contents of the New Build or `dist` Folder**:
   - Use the following command to copy your newly built application files to your server's web root directory (`/var/www/html/` for Nginx or Apache):
     ```bash
     sudo cp -r ./build/* /var/www/html/
     ```

2. **Restart the Web Server**:
   - After copying the new files, restart your web server to apply the changes:
     ```bash
     sudo systemctl restart nginx
     ```
   - If you are using Apache, replace `nginx` with `apache2`:
     ```bash
     sudo systemctl restart apache2
     ```

---

### Creating a Snapshot of Your Code

To take a snapshot of your code before making any changes, you can compress the entire project directory. This will allow you to back up the current state of your code:

### **1. Compress the Folder**:

You can use either the `tar` or `zip` command to create an archive of your code.

#### **Using `tar`**:
```bash
tar -czvf snapshot.tar.gz /path/to/your/code
```

- This will create a `tar.gz` compressed archive of the `code` directory.

#### **Using `zip`**:
```bash
zip -r snapshot.zip /path/to/your/code
```

- This will create a `zip` file of the `code` directory.

---

### **Advanced File Management**

**Search for Files by Name:**
```bash
find /path/to/search -name "filename"
```

**Search for Files by Size:**
```bash
find /path/to/search -size +50M
```

**Delete Files Older than X Days:**
```bash
find /path/to/search -type f -mtime +30 -delete
```

**List Files with Human-Readable Sizes:**
```bash
ls -lh
```

---

### **Package Management**

**Update Package List (Debian/Ubuntu):**
```bash
sudo apt update
```

**Upgrade Installed Packages:**
```bash
sudo apt upgrade
```

**Clean Up Unused Packages:**
```bash
sudo apt autoremove
```

**Check Package Information:**
```bash
dpkg -l | grep packagename
```

---

### **Docker Management**

**List All Running Containers:**
```bash
docker ps
```

**List All Containers (Including Stopped):**
```bash
docker ps -a
```

**Stop All Running Containers:**
```bash
docker stop $(docker ps -q)
```

**Remove All Stopped Containers:**
```bash
docker rm $(docker ps -a -q)
```

**Remove All Unused Images:**
```bash
docker image prune -a
```

---

### **Git Commands**

**Clone a Repository:**
```bash
git clone https://github.com/user/repo.git
```

**Check Status of Local Repository:**
```bash
git status
```

**View Commit History:**
```bash
git log --oneline
```

**Revert a Specific Commit:**
```bash
git revert <commit_hash>
```

**Stash Changes:**
```bash
git stash
```

---

### **Networking Tools**

**Check External IP Address:**
```bash
curl ifconfig.me
```

**Ping a Host to Check Connectivity:**
```bash
ping google.com
```

**Check Open Ports:**
```bash
nmap localhost
```

**Flush DNS Cache:**
```bash
sudo systemd-resolve --flush-caches
```

**Test Network Bandwidth:**
```bash
iperf3 -c server_ip
```

---

### **Performance Optimization**

**Clear Cache Memory:**
```bash
sudo sync; sudo sysctl -w vm.drop_caches=3
```

**Optimize System Swappiness:**
```bash
sudo sysctl vm.swappiness=10
```

**Check Current Swappiness Value:**
```bash
cat /proc/sys/vm/swappiness
```

---

### **Backup and Restore**

**Backup Entire Directory:**
```bash
rsync -av --progress /source/directory /destination/directory
```

**Restore Files from Backup:**
```bash
rsync -av --progress /backup/directory /original/directory
```

**Database Backup with Compression:**
```bash
pg_dump -U username dbname | gzip > backup.sql.gz
```

**Restore Database from Backup:**
```bash
gunzip < backup.sql.gz | psql -U username dbname
```

---

### **Log Management**

**View Last 50 Lines of a Log File:**
```bash
tail -n 50 /var/log/syslog
```

**View Logs with Timestamp:**
```bash
journalctl -u servicename --since "1 hour ago"
```

**Clear Specific Log File:**
```bash
sudo truncate -s 0 /var/log/syslog
```

---

### **User Management**

**Create a New User:**
```bash
sudo adduser username
```

**Add User to a Group:**
```bash
sudo usermod -aG groupname username
```

**Switch User:**
```bash
su - username
```

**Delete a User:**
```bash
sudo deluser username
```

---

### **Advanced Monitoring**

**Monitor Disk Partitions:**
```bash
df -Th
```

**Trace System Calls of a Process:**
```bash
strace -p <pid>
```

**Check Kernel Messages:**
```bash
dmesg | tail
```

**Real-Time Hardware Monitoring:**
```bash
sensors
```

---

### **System Updates and Upgrades**

**Check for Kernel Version:**
```bash
uname -r
```

**List Available Kernel Updates:**
```bash
apt list --upgradable | grep linux
```

**Install a Specific Kernel Version:**
```bash
sudo apt install linux-image-x.x.x
```

---







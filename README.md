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

- This will create a `zip` file of the `code` directory.



---


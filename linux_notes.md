Navigation 
### pwd — print working directory.
  ➜ Example: pwd

● ls — list directory contents.
  ➜ Example: ls

● ls -la — list all files with details.
  ➜ Example: ls -la

● cd /path — change to path.
  ➜ Example: cd /usr/local

● cd .. — go to parent directory.
  ➜ Example: cd ..

● cd ~ — go to home directory.
  ➜ Example: cd ~

● tree — display directories as a tree.
  ➜ Example: tree

### Files and directories 
● touch file.txt — create an empty file or update timestamp.
  ➜ Example: touch notes.txt

● mkdir dir — create a directory.
  ➜ Example: mkdir myfolder

● mkdir -p a/b/c — create nested directories.
  ➜ Example: mkdir -p project/src/utils

● cp src dst — copy a file or directory.
  ➜ Example: cp file.txt /tmp/

● cp -r dir1 dir2 — copy a directory recursively.
  ➜ Example: cp -r folder1 folder2

● mv old new — move or rename a file or directory.
  ➜ Example: mv oldname.txt newname.txt

● rm file — remove a file.
  ➜ Example: rm notes.txt

● rm -rf dir — remove a directory tree (use with caution).
  ➜ Example: rm -rf old_files/

● rmdir emptydir — remove an empty directory.
  ➜ Example: rmdir temp

● stat file — show file metadata and timestamps.
  ➜ Example: stat linux_commands.md

● basename /path/file — print filename from path.
  ➜ Example: basename /etc/passwd

● dirname /path/file — print directory path from filename.
  ➜ Example: dirname /etc/passwd

### Viewing and paging 
● cat file — print file contents.
  ➜ Example: cat /etc/os-release

● tac file — print file contents in reverse.
  ➜ Example: tac file.txt

● head -n 20 file — show first 20 lines.
  ➜ Example: head -n 20 logs.txt

● tail -n 20 file — show last 20 lines.
  ➜ Example: tail -n 20 logs.txt

● tail -f logfile — follow file updates (logs).
  ➜ Example: tail -f /var/log/syslog

● less file — page through a file with search.
  ➜ Example: less document.txt

● more file — basic pager for files.
  ➜ Example: more document.txt

● nl file — number lines while viewing.
  ➜ Example: nl script.sh

● wc -l file — count lines in a file.
  ➜ Example: wc -l /etc/passwd

### Search and text processing 
● grep "pattern" file — search pattern in a file.
  ➜ Example: grep "error" /var/log/syslog

● grep -ri "pattern" dir/ — recursive, case-insensitive search.
  ➜ Example: grep -ri "error" /var/log/

● sort file — sort lines in a file.
  ➜ Example: sort names.txt

● uniq file — omit repeated adjacent lines.
  ➜ Example: uniq sorted.txt

● cut -d ':' -f 1 file — select delimited fields.
  ➜ Example: cut -d ':' -f 1 /etc/passwd

● awk '{print $1}' file — print the first column.
  ➜ Example: awk '{print $1}' data.txt

● sed -i 's/old/new/g' file — in-place find and replace.
  ➜ Example: sed -i 's/http/https/g' index.html

● tr 'a-z' 'A-Z' — translate characters (lower to upper).
  ➜ Example: echo "linux" | tr 'a-z' 'A-Z'

● paste file1 file2 — merge lines side by side.
  ➜ Example: paste a.txt b.txt

● tee out.txt — write output to file and stdout.
  ➜ Example: echo "hello" | tee test.txt

### Permissions and ownership 
● chmod 644 file — set rw-r--r-- permissions.
  ➜ Example: chmod 644 notes.txt

● chmod 755 file — set rwxr-xr-x permissions.
  ➜ Example: chmod 755 script.sh

● chmod +x script.sh — make a file executable.
  ➜ Example: chmod +x deploy.sh

● chown user:group file — change owner and group.
  ➜ Example: sudo chown root:root secure.txt

● chgrp group file — change group ownership.
  ➜ Example: sudo chgrp admin data.txt

● umask 022 — set default permissions mask.
  ➜ Example: umask 022

● getfacl file — view file ACLs.
  ➜ Example: getfacl report.pdf

● setfacl -m u:user:rwx file — set ACL for a user.
  ➜ Example: setfacl -m u:john:rwx file.txt

### Processes and jobs 
● ps aux — list all processes with details.
  ➜ Example: ps aux | grep nginx

● top — interactive process viewer.
  ➜ Example: top

● htop — enhanced process viewer (if installed).
  ➜ Example: htop

● pgrep name — find PIDs by process name.
  ➜ Example: pgrep apache2

● pkill name — send signals by process name.
  ➜ Example: pkill firefox

● kill PID — terminate a process by PID.
  ➜ Example: kill 1234

● killall name — terminate processes by name.
  ➜ Example: killall name

● nice -n 10 cmd — start with adjusted priority.
  ➜ Example: nice -n 10 myscript.sh

● renice -n 10 -p PID — change priority of running process.
  ➜ Example: renice -n 10 -p 2345

● jobs — list shell jobs.
  ➜ Example: jobs

● bg %1 — resume job in background.
  ➜ Example: bg %1

● fg %1 — bring job to foreground.
  ➜ Example: fg %1

● nohup command & — ignore hangups and run in background.
  ➜ Example: nohup python3 script.py &

● time command — measure execution time.
  ➜ Example: time ls -la

● watch -n 1 free — rerun a command at intervals.
  ➜ Example: watch -n 1 df -h

### System info and logs 
● uname -a — kernel and system information.
  ➜ Example: uname -a

● hostnamectl — view or set hostname.
  ➜ Example: hostnamectl

● uptime — show load averages and uptime.
  ➜ Example: uptime

● free -h — memory and swap usage.
  ➜ Example: free -h

● vmstat — virtual memory statistics.
  ➜ Example: vmstat 1 5

● iostat — CPU and I/O statistics.
  ➜ Example: iostat -x 1 3

● mpstat — per-CPU usage statistics.
  ➜ Example: mpstat -P ALL 1

● pidstat — per-process statistics.
  ➜ Example: pidstat -u 1

● lscpu — CPU architecture details.
  ➜ Example: lscpu

● lsusb — list USB devices.
  ➜ Example: lsusb

● lspci — list PCI devices.
  ➜ Example: lspci

● lshw — hardware inventory.
  ➜ Example: sudo lshw -short

● dmesg — kernel ring buffer messages.
  ➜ Example: dmesg | tail

● journalctl -xe — view recent critical system logs.
  ➜ Example: journalctl -xe

● journalctl -u nginx — view logs for a systemd unit.
  ➜ Example: journalctl -u nginx

### Disks, partitions, and filesystems 
● df -h — mounted filesystem disk usage.
  ➜ Example: df -h

● du -sh dir/ — directory size summary.
  ➜ Example: du -sh Downloads/

● lsblk — list block devices.
  ➜ Example: lsblk

● blkid — print block device attributes.
  ➜ Example: blkid

● fdisk -l — list partition tables.
  ➜ Example: sudo fdisk -l

● parted -l — list partitions with parted.
  ➜ Example: sudo parted -l

● mkfs.ext4 /dev/sdX1 — create an ext4 filesystem.
  ➜ Example: sudo mkfs.ext4 /dev/sdb1  # destructive!

● fsck /dev/sdX1 — check and repair filesystem.
  ➜ Example: sudo fsck /dev/sdb1

● mount /dev/sdX1 /mnt — mount a partition.
  ➜ Example: sudo mount /dev/sdb1 /mnt

● umount /mnt — unmount a filesystem.
  ➜ Example: sudo umount /mnt

● cat /etc/fstab — view persistent mount table.
  ➜ Example: cat /etc/fstab

### Networking and DNS 
● ip addr — show IP addresses.
  ➜ Example: ip addr

● ip route — show routing table.
  ➜ Example: ip route

● ping -c 4 host — test connectivity.
  ➜ Example: ping -c 4 8.8.8.8

● traceroute host — trace network path.
  ➜ Example: traceroute 8.8.8.8

● ss -tuln — list listening sockets and ports.
  ➜ Example: ss -tuln

● netstat -tuln — legacy sockets and ports list.
  ➜ Example: netstat -tuln

● nslookup example.com — DNS query.
  ➜ Example: nslookup example.com

● dig example.com — detailed DNS query.
  ➜ Example: dig example.com

● curl -I https://example.com — HTTP request.
  ➜ Example: curl -I https://example.com

● wget https://example.com/file — download a file.
  ➜ Example: wget https://example.com/file

● ssh user@host — connect via SSH.
  ➜ Example: ssh user@192.168.1.10

● scp file user@host:/path/ — copy file over SSH.
  ➜ Example: scp file.txt user@192.168.1.10:/tmp/

● sftp user@host — interactive file transfer over SSH.
  ➜ Example: sftp user@192.168.1.10

● nc -l -p 1234 — listen on TCP port.
  ➜ Example: nc -l -p 1234

● nc host 80 — connect to TCP port.
  ➜ Example: nc localhost 80

● tcpdump -i eth0 port 443 — capture packets.
  ➜ Example: sudo tcpdump -i eth0 port 443

● nmap -sS host — scan ports with SYN.
  ➜ Example: nmap -sS localhost

● ufw enable — enable uncomplicated firewall.
  ➜ Example: sudo ufw enable

● ufw allow 22 — allow SSH.
  ➜ Example: sudo ufw allow 22

● iptables -L — list firewall rules.
  ➜ Example: sudo iptables -L

● firewall-cmd --list-all — show firewalld config.
  ➜ Example: sudo firewall-cmd --list-all

### Archiving, compression, and sync 
● tar -czf archive.tar.gz dir/ — create gzip tarball.
  ➜ Example: tar -czf backup.tar.gz project/

● tar -xzf archive.tar.gz — extract gzip tarball.
  ➜ Example: tar -xzf backup.tar.gz

● tar -cf archive.tar — create tar archive.
  ➜ Example: tar -cf backup.tar project/

● tar -xf archive.tar — extract tar archive.
  ➜ Example: tar -xf backup.tar

● zip -r archive.zip dir/ — create zip archive.
  ➜ Example: zip -r archive.zip docs/

● unzip archive.zip — extract zip archive.
  ➜ Example: unzip archive.zip

● gzip file — compress with gzip.
  ➜ Example: gzip file.txt

● gunzip file.gz — decompress gzip file.
  ➜ Example: gunzip file.txt.gz

● bzip2 file — compress with bzip2.
  ➜ Example: bzip2 file.txt

● bunzip2 file.bz2 — decompress bzip2 file.
  ➜ Example: bunzip2 file.txt.bz2

● xz file — compress with xz.
  ➜ Example: xz file.txt

● unxz file.xz — decompress xz file.
  ➜ Example: unxz file.txt.xz

● rsync -avz src/ dest/ — sync files locally.
  ➜ Example: rsync -avz src/ dest/

● rsync -avz -e ssh src/ user@host:/dest/ — sync over SSH.
  ➜ Example: rsync -avz -e ssh src/ user@host:/dest/

● cpio -ov < filelist > archive.cpio — create cpio archive.
  ➜ Example: cpio -ov < filelist > archive.cpio

### Package management (Debian/Ubuntu) 
● apt-get update — refresh package lists.
  ➜ Example: sudo apt-get update

● apt-get install nginx — install a package.
  ➜ Example: sudo apt-get install -y nginx

● apt-get upgrade — upgrade installed packages.
  ➜ Example: sudo apt-get upgrade

● apt-get remove pkg — remove a package.
  ➜ Example: sudo apt-get remove package-name

● apt-cache search nginx — search packages.
  ➜ Example: apt-cache search nginx

● apt-cache show pkg — show package details.
  ➜ Example: apt-cache show nginx

● dpkg -i pkg.deb — install a .deb file.
  ➜ Example: sudo dpkg -i package.deb

● dpkg -r pkg — remove a .deb package.
  ➜ Example: sudo dpkg -r package-name

### Package management (RHEL/CentOS/Fedora) 
● yum install pkg — install a package.
  ➜ Example: sudo yum install -y httpd

● yum update — update packages.
  ➜ Example: sudo yum update

● yum remove pkg — remove a package.
  ➜ Example: sudo yum remove package-name

● dnf install pkg — install with dnf.
  ➜ Example: sudo dnf install -y nginx

● dnf update — update with dnf.
  ➜ Example: sudo dnf update

● rpm -i pkg.rpm — install an RPM.
  ➜ Example: sudo rpm -i package.rpm

● rpm -e pkg — erase an RPM.
  ➜ Example: sudo rpm -e package-name

### Services and scheduling 
● systemctl start nginx — start a service.
  ➜ Example: sudo systemctl start ssh  # safer example using ssh

● systemctl stop nginx — stop a service.
  ➜ Example: sudo systemctl stop ssh

● systemctl restart nginx — restart a service.
  ➜ Example: sudo systemctl restart ssh

● systemctl status nginx — check service status.
  ➜ Example: sudo systemctl status ssh

● systemctl enable nginx — enable at boot.
  ➜ Example: sudo systemctl enable ssh

● systemctl disable nginx — disable at boot.
  ➜ Example: sudo systemctl disable ssh

● service nginx start — legacy start command.
  ➜ Example: sudo service ssh start

● service nginx status — legacy status command.
  ➜ Example: sudo service ssh status

● crontab -e — edit cron jobs.
  ➜ Example: crontab -e

● crontab -l — list cron jobs.
  ➜ Example: crontab -l

● crontab -r — remove all cron jobs (use carefully).
  ➜ Example: crontab -r

● at 09:00 — schedule one-time job.
  ➜ Example: echo "echo hello" | at 09:00

● batch — run when load is low.
  ➜ Example: echo "script.sh" | batch

● sleep 5s — delay for five seconds.
  ➜ Example: sleep 5s

### Environment and shell 
● env — print environment variables.
  ➜ Example: env

● echo $VAR — print a variable value.
  ➜ Example: echo $HOME

● export VAR=value — set an environment variable.
  ➜ Example: export MYVAR=hello

● which command — show command path.
  ➜ Example: which python3

● history — show command history.
  ➜ Example: history | tail

● alias ll='ls -la' — create a command alias.
  ➜ Example: alias ll='ls -la'

● unalias ll — remove an alias.
  ➜ Example: unalias ll

### Containers and orchestration 
● docker run image — run a container.
  ➜ Example: docker run --rm hello-world

● docker ps — list running containers.
  ➜ Example: docker ps

● docker ps -a — list all containers.
  ➜ Example: docker ps -a

● docker exec -it container bash — open a shell in a container.
  ➜ Example: docker exec -it mycontainer bash

● docker logs container — show container logs.
  ➜ Example: docker logs mycontainer

● docker build -t image . — build an image.
  ➜ Example: docker build -t myapp .

● docker rmi image — remove an image.
  ➜ Example: docker rmi myapp

● docker-compose up — start multi-container app.
  ➜ Example: docker-compose up -d

● docker-compose down — stop and remove app.
  ➜ Example: docker-compose down

● kubectl get pods — list pods.
  ➜ Example: kubectl get pods

● kubectl get nodes — list nodes.
  ➜ Example: kubectl get nodes

● kubectl get services — list services.
  ➜ Example: kubectl get services

● kubectl apply -f file.yaml — apply configuration.
  ➜ Example: kubectl apply -f deployment.yaml

● kubectl logs pod — view pod logs.
  ➜ Example: kubectl logs mypod

● kubectl exec -it pod -- bash — exec into a pod.
  ➜ Example: kubectl exec -it mypod -- bash

● kubectl describe pod podname — describe a pod.
  ➜ Example: kubectl describe pod mypod

● kubectl scale deployment name --replicas=3 — scale a deployment.
  ➜ Example: kubectl scale deployment myapp --replicas=3

● kubectl rollout restart deployment name — restart a deployment.
  ➜ Example: kubectl rollout restart deployment myapp

● helm install release chart — install a Helm chart.
  ➜ Example: helm install myrelease mychart

● helm upgrade release chart — upgrade a release.
  ➜ Example: helm upgrade myrelease mychart

● helm list — list releases.
  ➜ Example: helm list

● helm delete release — delete a release.
  ➜ Example: helm delete myrelease

### Cloud CLIs 
● aws configure — set up AWS CLI credentials.
  ➜ Example: aws configure

● aws s3 cp file s3://bucket/ — upload a file to S3.
  ➜ Example: aws s3 cp file.txt s3://my-bucket/

● aws ec2 describe-instances — list EC2 instances.
  ➜ Example: aws ec2 describe-instances

● az login — authenticate Azure CLI.
  ➜ Example: az login

● az vm list — list Azure VMs.
  ➜ Example: az vm list

● gcloud auth login — authenticate gcloud.
  ➜ Example: gcloud auth login

● gcloud compute instances list — list GCP instances.
  ➜ Example: gcloud compute instances list

### Shutdown and reboot 
● shutdown -h now — power off immediately. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

● shutdown -r now — reboot immediately. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

● shutdown -h +10 — schedule power off in 10 minutes. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

● reboot — restart the system. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

● poweroff — power off the system. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

● halt — halt the system. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

● init 0 — switch to shutdown runlevel. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

● init 6 — switch to reboot runlevel. ⚠ dangerous — example omitted.
  ➜ Example: # not shown for safety

### Summary Index 
Navigation 
Files and directories 
Viewing and paging 
Search and text processing 
Permissions and ownership 
Processes and jobs 
System info and logs 
Disks, partitions, and filesystems 
Networking and DNS 
Archiving, compression, and sync 
Package management (Debian/Ubuntu) 
Package management (RHEL/CentOS/Fedora) 
Services and scheduling 
Environment and shell 
Containers and orchestration 
Cloud CLIs 
Shutdown and reboot

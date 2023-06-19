Linux Command Reference: 100 Essential Commands for the Command-Line Enthusiast

1. `sudo ls`: List directory contents. Example: `sudo ls /var/log`
2. `sudo cd`: Change directory. Example: `sudo cd /root`
3. `sudo pwd`: Print working directory. Example: `sudo pwd`
4. `sudo mkdir`: Create a directory. Example: `sudo mkdir /opt/mydir`
5. `sudo touch`: Create an empty file. Example: `sudo touch /etc/myfile.txt`
6. `sudo rm`: Remove files or directories. Example: `sudo rm /tmp/myfile.txt`
7. `sudo cp`: Copy files and directories. Example: `sudo cp /home/user/file.txt /var/www/html`
8. `sudo mv`: Move or rename files and directories. Example: `sudo mv /tmp/file.txt /home/user/documents`
9. `sudo cat`: Concatenate and display file content. Example: `sudo cat /var/log/syslog`
10. `sudo grep`: Search for a specific pattern in files. Example: `sudo grep "error" /var/log/syslog`
11. `sudo find`: Search for files and directories. Example: `sudo find / -name "myfile"`
12. `sudo chmod`: Change permissions of files and directories. Example: `sudo chmod 755 /var/www/html`
13. `sudo chown`: Change ownership of files and directories. Example: `sudo chown user:group /var/www/html`
14. `sudo tar`: Create or extract compressed archives. Example: `sudo tar -czvf archive.tar.gz /home/user`
15. `sudo gzip`: Compress files. Example: `sudo gzip myfile.txt`
16. `sudo gunzip`: Decompress files. Example: `sudo gunzip myfile.txt.gz`
17. `sudo zip`: Create a compressed ZIP archive. Example: `sudo zip -r archive.zip /home/user`
18. `sudo unzip`: Extract files from a ZIP archive. Example: `sudo unzip archive.zip -d /home/user`
19. `sudo ssh`: Secure shell, remote login. Example: `sudo ssh username@hostname`
20. `sudo scp`: Securely copy files between hosts. Example: `sudo scp myfile.txt username@hostname:/path/to/destination`
21. `sudo wget`: Download files from the web. Example: `sudo wget https://example.com/file.txt`
22. `sudo curl`: Transfer data from or to a server. Example: `sudo curl -O https://example.com/file.txt`
23. `sudo ping`: Send ICMP echo requests to a network host. Example: `sudo ping 8.8.8.8`
24. `sudo ifconfig`: Configure network interfaces. Example: `sudo ifconfig eth0 up`
25. `sudo netstat`: Network statistics and connections. Example: `sudo netstat -tuln`
26. `sudo route`: View and manipulate IP routing table. Example: `sudo route -n`
27. `sudo df`: Disk space usage. Example: `sudo df -h`
28. `sudo du`: Estimate file and directory space usage. Example: `sudo du -sh /var/log`
29. `sudo top`: Monitor system processes. Example: `sudo top`
30. `sudo ps`: Display running processes. Example: `sudo ps aux`
31. `sudo kill`: Terminate processes. Example: `sudo kill 1234`
32. `sudo man`: Display manual pages. Example: `sudo man ls`
33. `sudo uname`: Print system information. Example: `sudo uname -a`
34. `sudo whoami`: Print the current username. Example: `sudo whoami`
35. `sudo date`: Display or set the system date and time. Example: `sudo date`
36. `sudo history`: Display command history. Example: `sudo history`
37. `sudo tail`: Output the last part of files. Example: `sudo tail /var/log/syslog`
38. `sudo head`: Output the first part of files. Example: `sudo head /var/log/syslog`
39. `sudo sort`: Sort lines in text files. Example: `sudo sort myfile.txt`
40. `sudo sed`: Stream editor for text manipulation. Example: `sudo sed 's/foo/bar/g' myfile.txt`
41. `sudo awk`: Text processing and pattern scanning. Example: `sudo awk '{print $1}' myfile.txt`
42. `sudo cut`: Extract sections from lines of files. Example: `sudo cut -d',' -f1 myfile.csv`
43. `sudo diff`: Compare files line by line. Example: `sudo diff file1.txt file2.txt`
44. `sudo patch`: Apply changes to files using diff files. Example: `sudo patch myfile.txt patchfile.diff`
45. `sudo tee`: Read from standard input and write to files. Example: `echo "Hello" | sudo tee myfile.txt`
46. `sudo echo`: Display a line of text. Example: `sudo echo "Hello, world!"`
47. `sudo alias`: Create aliases for commands. Example: `sudo alias l="ls -l"`
48. `sudo source`: Execute commands from a file. Example: `sudo source myscript.sh`
49. `sudo su`: Switch user or become superuser. Example: `sudo su -`
50. `sudo passwd`: Change user password. Example: `sudo passwd username`
51. `sudo crontab`: Schedule commands to run at specific times. Example: `sudo crontab -e`
52. `sudo systemctl`: Control the system and service manager. Example: `sudo systemctl start apache2`
53. `sudo service`: Control system services. Example: `sudo service nginx restart`
54. `sudo apt-get`: Package handling utility for Debian-based systems. Example: `sudo apt-get update`
55. `sudo yum`: Package manager for RPM-based systems. Example: `sudo yum install package`
56. `sudo dnf`: Next-generation package manager for Fedora. Example: `sudo dnf upgrade`
57. `sudo ps aux`: Display all running processes. Example: `sudo ps aux`
58. `sudo killall`: Kill processes by name. Example: `sudo killall processname`
59. `sudo chmod +x`: Make a file executable. Example: `sudo chmod +x script.sh`
60. `sudo uname -a`: Print detailed system information. Example: `sudo uname -a`
61. `sudo locate`: Find files by name. Example: `sudo locate myfile.txt`
62. `sudo lsof`: List open files and processes. Example: `sudo lsof -i :80`
63. `sudo uptime`: Show how long the system has been running. Example: `sudo uptime`
64. `sudo free`: Display system memory usage. Example: `sudo free -h`
65. `sudo ssh-keygen`: Generate SSH key pairs. Example: `sudo ssh-keygen -t rsa`
66. `sudo ssh-copy-id`: Copy SSH public key to a remote host. Example: `sudo ssh-copy-id user@hostname`
67. `sudo dig`: DNS lookup utility. Example: `sudo dig example.com`
68. `sudo nslookup`: Query DNS for IP addresses. Example: `sudo nslookup google.com

`
69. `sudo host`: DNS lookup utility. Example: `sudo host www.example.com`
70. `sudo nc`: Netcat, network utility for reading/writing network connections. Example: `sudo nc -l 80`
71. `sudo iptables`: Administration tool for IPv4 packet filtering and NAT. Example: `sudo iptables -L`
72. `sudo sysctl`: Configure kernel parameters at runtime. Example: `sudo sysctl -p`
73. `sudo useradd`: Create a new user. Example: `sudo useradd newuser`
74. `sudo usermod`: Modify user account. Example: `sudo usermod -aG sudo newuser`
75. `sudo userdel`: Delete a user account. Example: `sudo userdel olduser`
76. `sudo groupadd`: Create a new group. Example: `sudo groupadd newgroup`
77. `sudo groupmod`: Modify a group. Example: `sudo groupmod -n newname oldgroup`
78. `sudo groupdel`: Delete a group. Example: `sudo groupdel oldgroup`
79. `sudo chmod 600`: Set file permissions to read and write for the owner. Example: `sudo chmod 600 myfile.txt`
80. `sudo chmod 644`: Set file permissions to read for the owner and read for others. Example: `sudo chmod 644 myfile.txt`
81. `sudo chown user:group`: Change the owner and group of a file or directory. Example: `sudo chown newuser:newgroup myfile.txt`
82. `sudo chgrp`: Change the group ownership of a file or directory. Example: `sudo chgrp newgroup myfile.txt`
83. `sudo uptime`: Show how long the system has been running. Example: `sudo uptime`
84. `sudo w`: Display who is logged in and what they are doing. Example: `sudo w`
85. `sudo who`: Show who is logged in. Example: `sudo who`
86. `sudo which`: Display the location of a command. Example: `sudo which ls`
87. `sudo tar cvf`: Create a tar archive. Example: `sudo tar cvf archive.tar file1.txt file2.txt`
88. `sudo tar xvf`: Extract files from a tar archive. Example: `sudo tar xvf archive.tar`
89. `sudo df -h`: Show disk space usage in human-readable format. Example: `sudo df -h`
90. `sudo du -sh`: Display the total size of a directory in human-readable format. Example: `sudo du -sh /var/log`
91. `sudo history -c`: Clear command history. Example: `sudo history -c`
92. `sudo source ~/.bashrc`: Reload the bash configuration file. Example: `sudo source ~/.bashrc`
93. `sudo grep -r "pattern" .`: Recursively search for a pattern in files. Example: `sudo grep -r "error" /var/log`
94. `sudo locate -b "filename"`: Quickly find the location of a file. Example: `sudo locate -b "myfile.txt"`
95. `sudo find /path -name "filename"`: Search for files with a specific name. Example: `sudo find / -name "myfile"`
96. `sudo ps -ef | grep "process"`: Find running processes matching a name. Example: `sudo ps -ef | grep "nginx"`
97. `sudo tail -f /path/to/file`: Continuously monitor a file for new content. Example: `sudo tail -f /var/log/syslog`
98. `sudo sed -i 's/old/new/g' file`: Replace all occurrences of

 a pattern in a file. Example: `sudo sed -i 's/foo/bar/g' myfile.txt`
99. `sudo awk '{print $1,$3}' file`: Print specific fields from a file. Example: `sudo awk '{print $1}' myfile.txt`
100. `sudo cut -d',' -f1 file`: Extract a specific field from a file. Example: `sudo cut -d',' -f1 myfile.csv`

Please note that some commands may require additional options or arguments based on your specific use case. Make sure to refer to the respective command's documentation or man pages for more information.

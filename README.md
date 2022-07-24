<h1>Brute-Force SSH Credentials</h1>

<h2>Description</h2>
Project consists of a brute force attack to get access to a remote host. This project has served to a way of highlighting the importance of owning a strong password. We will be exploring different ways of implementing brute force attack against combinations of usernames and passwords on open SSH ports.
<br />

<h2>Environments Used </h2>

- <b>Kali Linux</b>

<h2>Program walk-through:</h2>

<p align="center">
Metasploit version (Nmap scan): <br/>
  
  - <b>First we have to discover and determine which of our devices on the network might have an SSH port open</b>
  - <b>We will be starting with getting the network range</b>
  - <b>This command filteres the information to only displaying the phrases that contain the word inet </b>

<p align="center">
<img src="https://i.imgur.com/wEZa4Yu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
  
  - <b>We discovered that our IP address is 10.0.2.15 </b>
  - <b>To get the network range we will be executing the following command </b>
  - <b>The network range is 10.0.2.0/24</b>

<p align="center">
<img src="https://i.imgur.com/iIhE5Td.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
  
  - <b>The reason why we need this for our nmap scan is because it allows us to scan every device within the network</b>
  - <b>The command within the picture bellow will be showing information about the SSH port(port 22) that are open only as we are only interested in the open ports</b>

<p align="center">
<img src="https://i.imgur.com/0x7BQhz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
  
  - <b>Because our port 22 is closed, we will have to make it listen</b>
  - <b>Fist install openssh-server</b>
  - <b>Then access the sshd_config file within the /etc/ssh directory</b>

<p align="center">
<img src="https://i.imgur.com/b4qHvI8.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
 
  - <b>In this file you can also assign the ssh port to another port (for security purposes)</b>

<p align="center">
<img src="https://i.imgur.com/rdjowzl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
  
  - <b>To open the port just run the command service ssh start and now we can see that the port 22 is not open for our IP</b>

<p align="center">
<img src="https://i.imgur.com/aH6g4n9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

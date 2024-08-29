# Configure-a-Firewall-UFW
Configure a Firewall (Uncomplicated Firewall)

<h2>Description</h2>
This project involves setting up and configuring a secure web server on an Ubuntu system, utilizing the Uncomplicated Firewall (UFW) to manage access and enhance security. The primary objective is to deploy a web server, configure necessary firewall rules, and verify access via HTTP and HTTPS protocols, ensuring the system is functional and secure against unauthorized access.
<br />


<h2>Objectives:</h2>

1) <b>Deploy a Web Server:</b> Install and configure a web server (Apache or Nginx) on an Ubuntu system.
2) <b>Firewall Configuration:</b> Use UFW to manage and secure network traffic, specifically allowing SSH, HTTP, and HTTPS access while blocking all other unauthorized connections.
3) <b>Access Testing:</b> Verify the correct configuration by testing remote SSH access and HTTP and HTTPS connectivity from different devices.
4) <b>Security Assurance:</b> Ensure the web server is accessible only through the allowed ports and secure the system from potential threats.

<h2>Scope:</h2>

1) <b>System Setup:</b>
- Installation of the Ubuntu operating system.
- Installation and configuration of Apache/Nginx web server.

2) <b>Firewall Configuration:</b>
- Installation and configuration of UFW.
- Setting up firewall rules to allow SSH (port 22), HTTP (port 80), and HTTPS (port 443).
- Restricting access to all other ports.

3) <b>Access Verification:</b>
- Testing SSH access from a remote machine to ensure secure shell connectivity.
- Testing HTTP and HTTPS access to ensure the web server is reachable and serving content correctly.

4) <b>Logging and Monitoring:</b>
- Enabling and reviewing UFW logs to monitor firewall activity.
- Checking web server logs to ensure proper operation and identify any potential issues. 

<h2>Tools and Technologies:</h2>

- <b>Operating System:</b> Ubuntu.
- <b>Web Server:</b> Apache or Nginx
- <b>Firewall:</b> Uncomplicated Firewall (UFW) 
- <b>Protocols:</b> SSH, HTTP, HTTPS 
- <b>Testing Tools:</b> Web browser, curl, telnet, SSH client

<h2>Expected Outcome:</h2>
By the end of this project, the Ubuntu system will be configured as a secure web server, accessible via SSH, HTTP, and HTTPS. The UFW firewall will be properly configured to allow only necessary traffic, enhancing the security of the system. The system's setup will be verified through comprehensive testing to ensure it meets security and functionality requirements.
<br />

<h2>Screenshot:</h2>
<p align="center">
Step by Step configuration: <br/>
1
<img src="https://imgur.com/fpC6qgH.png" width="33%"/>
2
<img src="https://imgur.com/FaQoact.png" width="33%"/>
3
<img width = "33%" src="https://imgur.com/wg8JU8u.png"/>
4
<img width = "33%" src="https://imgur.com/CsBHsyI.png"/>
5
<img src="https://imgur.com/KeWMZak.png" width="33%"/>
<br />


<p align="center">
Testing SHH Connection and Web Server Connection: <br/>
  <img src="https://imgur.com/CGv8l3Q.png" height="50%" width="33%" alt="Program Result"/>
  <img src="https://imgur.com/T6NOhCa.png" height="50%" width="33%" alt="Program Result"/>
 
<br />
  
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

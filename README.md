# Ubuntu UFW Firewall Configuration — SSH & Web Access Control

I built an Ubuntu firewall lab to manage network access using **Uncomplicated Firewall (UFW)**. The project focuses on configuring service-based access rules for **SSH (TCP 22), HTTP (TCP 80), and HTTPS (TCP 443)**, reviewing the firewall configuration, and examining SSH and web-server connectivity.

The screenshots below document the firewall configuration and connection-testing activities carried out during the lab.

## Project overview

| Area | Work completed or documented | Technologies |
| --- | --- | --- |
| Host firewall | Set up a UFW configuration workflow on Ubuntu | Ubuntu, UFW |
| Remote access | Included an SSH allow rule before enabling the firewall | SSH, TCP 22 |
| Web access | Defined rules for HTTP and HTTPS service ports | TCP 80, TCP 443 |
| Rule inspection | Reviewed commands for checking firewall status and active rules | `ufw status`, `ufw status verbose` |
| Connectivity | Documented SSH and web-server connection checks | SSH client, web browser |
| Monitoring | Included UFW logging and firewall-event inspection | UFW logs |

## Firewall configuration

The lab centered on allowing required administrative and web-service traffic while managing access through UFW.

**Core commands used in the documented configuration workflow:**

```bash
sudo ufw allow ssh
sudo ufw allow http
sudo ufw allow https
sudo ufw enable
sudo ufw status verbose
```

Allowing SSH before enabling the firewall is an important precaution when administering a Linux system remotely. The configuration also explores additional rule-management options, including IP-based restrictions and specific port allowances.

### Configuration evidence

| Firewall configuration | Rule management |
| --- | --- |
| ![UFW configuration screenshot 1](https://imgur.com/fpC6qgH.png) | ![UFW configuration screenshot 2](https://imgur.com/FaQoact.png) |
| ![UFW configuration screenshot 3](https://imgur.com/wg8JU8u.png) | ![UFW configuration screenshot 4](https://imgur.com/CsBHsyI.png) |

![UFW configuration screenshot 5](https://imgur.com/KeWMZak.png)

## SSH and web-server connectivity

I documented connection checks for two key services:

- **SSH:** Examining remote administration access through the permitted SSH service port.
- **Web server:** Checking browser connectivity to the Ubuntu-hosted web service.

| SSH connection check | Web-server connection check |
| --- | --- |
| ![SSH connection test](https://imgur.com/CGv8l3Q.png) | ![Web-server connection test](https://imgur.com/T6NOhCa.png) |

## Firewall logging and monitoring

The lab also covers UFW logging and firewall-event inspection as part of the security monitoring workflow:

```bash
sudo ufw logging on
sudo tail -f /var/log/ufw.log
```

These commands support reviewing firewall activity and investigating network access issues.

## Project outcomes

- Developed a practical Ubuntu UFW firewall configuration centered on SSH and web-service access.
- Documented service-specific access rules and firewall status inspection.
- Captured firewall configuration and SSH/web connectivity screenshots.
- Explored logging, rule review, and access-control practices relevant to Linux system administration and network security.

## Technical documentation

- [Firewall configuration case study (Markdown)](UFW-Firewall-Case-Study.md)
- [Firewall configuration case study (PDF)](01-ufw-firewall-case-study.pdf)
- [Configuration notes (PDF)](Configuration-Steps.pdf)

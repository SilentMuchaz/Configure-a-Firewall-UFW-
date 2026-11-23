# Ubuntu UFW Firewall Configuration — Technical Case Study

## Project overview

This lab documents an Ubuntu host-firewall configuration using Uncomplicated Firewall (UFW). Its purpose was to manage inbound SSH and web-service access, review firewall state, and outline validation and logging activities. The project README includes five linked configuration screenshots and two linked connectivity screenshots.

The supplied files contain a configuration guide and screenshot links. They do not include an exported `ufw status` result, a complete web-server configuration, or terminal output from connectivity checks. Findings below distinguish documented configuration work from independently verified outcomes.

## Environment and tools

| Component | Role in the lab |
| --- | --- |
| Ubuntu | Host operating system |
| UFW | Host firewall rule management |
| SSH / TCP 22 | Remote administration access |
| HTTP / TCP 80 | Web-service access |
| HTTPS / TCP 443 | Intended encrypted web-service access |
| Browser, SSH client, telnet/curl | Documented connectivity-testing tools |
| UFW logs | Proposed monitoring and troubleshooting evidence |

The project description refers to Apache or Nginx but does not identify which server was installed or provide its service configuration.

## Work documented

### 1. Firewall initialization and administrative access

The configuration guide includes UFW installation, status inspection, and activation. It explicitly places `sudo ufw allow ssh` before `sudo ufw enable` to avoid accidentally blocking an existing SSH session.

**Commands documented:** `sudo apt install ufw`, `sudo ufw status`, `sudo ufw allow ssh`, `sudo ufw enable`.

**Evidence available:** Externally hosted configuration screenshots; no locally archived `ufw status` output.

### 2. Service-access rules

The documented service rules allow SSH, HTTP, and HTTPS. Additional commands for port 8080, TCP ranges, and IP-specific allow/deny policies appear as optional examples. They are not treated as the effective firewall configuration.

| Service | Documented command | Intended access |
| --- | --- | --- |
| SSH | `sudo ufw allow ssh` | TCP/22 |
| HTTP | `sudo ufw allow http` | TCP/80 |
| HTTPS | `sudo ufw allow https` | TCP/443 |

**Important distinction:** Allowing TCP/443 through a firewall does not establish that HTTPS is actually served with a valid TLS configuration. Likewise, a rule list without the default inbound policy does not prove that every other port is blocked.

### 3. Connection testing

The README links two screenshots labeled as SSH and web-server connection checks. The configuration guide also describes tests from another machine and denied-port testing.

**Evidence available:** Two external screenshots, not present as files in the archive.

**Not independently established:** Exact SSH login outcome, HTTP status, HTTPS/TLS negotiation, or blocked-port results.

### 4. Firewall monitoring

The guide documents `sudo ufw logging on` and `sudo tail -f /var/log/ufw.log` for observing firewall activity. It does not include exported UFW log entries or event analysis.

## Assessment and results

| Area | Supported by supplied files | Additional validation needed |
| --- | --- | --- |
| UFW configuration workflow | Yes — commands and linked screenshots | Active status and final rule listing |
| SSH/HTTP/HTTPS rule intent | Yes — documented commands | Effective policy and service listeners |
| Remote connectivity tests | Tests described; screenshots linked | Readable command output or local screenshots |
| Denied-port enforcement | Test procedure described | Negative connection test plus rule/default-policy output |
| Firewall monitoring | Logging commands documented | Timestamped log entries and interpretation |

## Security considerations

- Preserve an administrative access path before activating a remote host firewall.
- Confirm the effective default incoming policy rather than assuming that unspecified ports are blocked.
- Keep the exposed service list limited to what is required; optional broad port/IP examples should not be treated as recommended production rules.
- Verify that the web server actually listens on the expected ports and that HTTPS is configured, not merely allowed through the firewall.
- Pair connection tests with the corresponding UFW rule list and log entries to support the final assessment.

## Outcome

The project records a UFW host-firewall configuration and testing workflow for Ubuntu, supported by seven linked screenshots. The available materials demonstrate the configuration approach and the planned validation methods, but do not establish a fully verified final security posture. Adding exported status output, local screenshots, and positive/negative connection results would strengthen the evidence without changing the underlying lab.


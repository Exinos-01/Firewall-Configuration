# Firewall-Configuration
## Objective

The purpose of this task was to configure and test basic firewall rules using **UFW (Uncomplicated Firewall)** on a Linux system. The key goals were to:

- Block traffic on **port 23 (Telnet)**
- Allow traffic on **port 22 (SSH)**
- Verify firewall behavior
- Understand how firewalls filter network traffic

---

##  System Used

- **OS:** Kali Linux (Debian-based)
- **Firewall Tool:** UFW
- **Network Tools:** `telnet`, `ssh`

---

##  Steps Performed

### Enabled UFW
Checked UFW status and made sure it was active:
sudo ufw status
Viewed Current Rules
sudo ufw status numbered
Blocked Port 23 (Telnet)
sudo ufw deny 23
Allowed Port 22 (SSH)
sudo ufw allow 22 Viewed Detailed Firewall Status
sudo ufw status verbose
This showed:

Port 23 is blocked

Port 22 is allowed

Logging is enabled

Tested Telnet Block

telnet localhost 23
Result: Connection refused – confirms port 23 is successfully blocked.

Removed Port 23 Block Rule

sudo ufw delete deny 23
Verified SSH Access

ssh root@<remote-ip>
This test confirms port 22 was open and accessible.

Screenshot
Screenshot of the full task (all commands and results) is included in:

screenshots/task-4.jpg
Key Concepts Practiced
Port-based traffic filtering

Allowing vs denying inbound traffic

Testing with telnet and ssh

UFW rule management and cleanup

Outcome
Successfully configured UFW to:

Block and test traffic on Telnet (port 23)

Allow SSH access (port 22)

Gain hands-on experience in managing Linux firewall rules

This improves system security by ensuring only required ports are open and helps understand how firewalls protect against unwanted network access.

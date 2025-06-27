# /ElevateLabs/

# Cyber Security Internship - Task 1

## Task Title:
Scan Your Local Network for Open Ports

## Objective:
To discover open ports on devices in the local network using `Nmap` and analyze their exposure.

## Tools Used:

- Nmap (TCP SYN scan)

## 💻 Command Used:

sudo nmap -sS 192.168.1.0/24



# Cyber Security Internship - Task 2

 **Analyze a Phishing Email Sampl**

 # Objective:
Simulate a real-world phishing attack using social engineering techniques to understand how attackers craft and deliver fake emails, host phishing pages, and collect sensitive user data — purely for ethical and educational purposes.

🛠️ What i Did in This Task:
# Created a Netflix-Themed Phishing Email
Designed a realistic HTML email mimicking a Netflix account suspension alert.

Included official branding such as the Netflix logo, color palette, and formatting.

Added a “Verify Account” button with a hover URL masked as:

https://www.netflix.com/account/verify

# Tools Used:

-Inline CSS for email compatibility

-Gmail HTML injection using Inspect Element

-Social Engineer Toolkit (SET) for testing email delivery

# Hosted a Phishing Page
Cloned Netflix’s login UI using HTML/CSS

Hosted the fake page locally using:

-python3 -m http.server 8000
-Publicly exposed it via:

--cloudflared tunnel --url http://localhost:8000-- 

# Outcome:
Victims visiting the phishing link were presented with a fully functional, fake Netflix login interface.

# Generated Phishing Link Using MIP22 Tool
Used the MIP22 tool to cloak the raw Cloudflare link with a cleaner, more deceptive domain:

**http://collar-comparable-patrick-astrology.trycloudflare.com**

This enhanced believability and helped avoid detection by spam filters or URL previews.

# Advantage:
MIP22 generated a custom subdomain to make the phishing link look safe and legitimate.

# Captured Victim Credentials
Inputs from the phishing form (email/phone and password) were collected via a backend script.

Optional fingerprinting could capture:

Victim IP address

Device type

Browser

Date/time

# Logged To:

data.txt — for credentials

fingerprint.txt — for metadata

*Everything is shown in the screenshots for better understand*




 # Cybersecurity Internship – Task 4

--Firewall Configuration using UFW on Linux--


#  Objective:
To configure and test basic firewall rules using the ufw (Uncomplicated Firewall) tool in Linux, demonstrating how firewall rules filter network traffic and enhance system security.

#  Tool Used:
✔️ UFW (Uncomplicated Firewall)
UFW is a frontend for iptables designed to simplify the process of configuring a host-based firewall. It enables users to manage firewall rules through simple commands.

 Experiment Overview:
# Step 1: Enabled the Firewall
To start managing incoming and outgoing network traffic, the firewall was activated using:


**sudo ufw enable**

 This ensures UFW starts filtering packets based on rules.

#  Step 2: Blocked Port 23 (Telnet)
Telnet is an outdated protocol that sends data in plaintext. To improve security, we blocked port 23 using:


**sudo ufw deny 23**

 This prevents remote connections over Telnet to the system.

# Step 3: Tested the Firewall Rule
To verify that port 23 was effectively blocked, we used:

**telnet localhost 23**

 Result: Connection was refused or timed out — confirming the firewall rule was active.

# Step 4: Allowed Port 22 (SSH)
To allow secure remote access via SSH, we added an allow rule:


**sudo ufw allow 22**

 This ensures that administrators can still access the system remotely without being blocked.

# Step 5: Verified Active Firewall Rules
All active rules were listed with:

**sudo ufw status numbered**

 Displayed all currently applied firewall rules with numbering for management.

#  Step 6: Removed the Test Rule (Optional)
To restore the original state of the firewall and remove the test block:

**sudo ufw delete deny 23**

Or reset everything:

**sudo ufw reset**

 Learning Outcome:


# Through this task, I learned:

How to enable and configure UFW for basic firewall tasks

The difference between blocking and allowing ports

How to test blocked ports using tools like telnet

Why blocking unsecured ports (like 23) improves security

How to view, manage, and clean firewall rules

#  Screenshots:
All screenshots of terminal outputs have been added in the /screenshots/ folder:

Firewall enabled

Port 23 blocked

Port 22 allowed

Rule verification

Telnet test results

# Useful Commands Summary:

sudo ufw enable
sudo ufw status numbered
sudo ufw deny 23
sudo ufw allow 22
telnet localhost 23
sudo ufw delete deny 23
sudo ufw reset

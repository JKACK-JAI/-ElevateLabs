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

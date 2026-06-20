# ToolsRus TryHackMe Writeup

This repository contains my writeup for the TryHackMe room **ToolsRus**.

The room focuses on using common penetration-testing tools to enumerate a target machine, identify exposed services, discover credentials, and gain access to the system.

## Tools Used

* Nmap
* Gobuster
* Hydra
* Nikto
* Metasploit

## Summary

The investigation began with an Nmap scan to identify the services running on the target. Web enumeration with Gobuster revealed hidden directories, including a page that exposed the username `bob`.

Hydra was then used to identify the password for the protected web directory. The credentials were also valid for the Apache Tomcat Manager interface running on port 1234.

Nikto was used to review the authenticated Tomcat Manager area. Metasploit’s `tomcat_mgr_upload` module was then used to upload a payload through the Tomcat Manager interface and obtain a shell as root.

## Writeup

[ToolsRus-tryhackme-writeup.pdf](./ToolsRus-tryhackme-writeup.pdf)

## Disclaimer

This writeup was created for educational and portfolio purposes only. All testing was performed in the TryHackMe lab environment.

© 2026 Osman Dhaqane. All rights reserved.

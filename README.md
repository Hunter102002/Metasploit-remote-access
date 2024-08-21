# Remote Access Exploitation Using Metasploit

## Objective

Executed a remote access attack on a vulnerable virtual machine (VM) using Metasploit, demonstrating the process of exploiting security weaknesses to gain unauthorized control over a system.

### Skills Learned

- Vulnerability Scanning: Identifying exploitable services and weaknesses on the target VM.
- Exploit Development: Leveraging Metasploit modules to exploit vulnerabilities and gain remote access.
- Post-Exploitation: Performing system reconnaissance and privilege escalation after gaining access.
- Linux Command Line Operations: Managing the attack process and interactions with the compromised VM from Kali Linux.

### Tools Used

- Kali Linux: As the base environment for conducting the exploitation.
- Metasploit Framework: For scanning, exploiting, and gaining remote access to the target VM.
- Nmap: For preliminary network scanning to identify open ports and vulnerable services on the VM.
- Meterpreter: As the payload for controlling the compromised system remotely.

### Outcome
This project successfully demonstrated the use of Metasploit to exploit a vulnerable virtual machine, gain remote access, and perform post-exploitation activities. It highlighted key skills in vulnerability scanning, exploitation, post-exploitation, and command-line operations within a penetration testing framework.

## Steps

ensure machine are able to talk to each other 

![Screenshot 2024-08-20 141808](https://github.com/user-attachments/assets/43124784-3e52-4917-973f-bc3a65a865aa)

![Screenshot 2024-08-20 141919](https://github.com/user-attachments/assets/460a5bfa-bd0c-4794-abbf-6f4a5a17e99d)

![Screenshot 2024-08-20 141928](https://github.com/user-attachments/assets/ad34194f-e374-4f40-9d9c-a632393d2455)

-----------------------------------------------------------------------------------------

run s nmap scan on the target vm to find any open ports that we may be able to exploit 

![Screenshot 2024-08-20 142015](https://github.com/user-attachments/assets/c1876a62-aba7-4dbe-9240-f7a3d2067673)

-----------------------------------------------------------------------------------------

use the same command but with (-sV) to find the version they are running 

![Screenshot 2024-08-20 142105](https://github.com/user-attachments/assets/8393fb14-d521-4d05-8a6b-97845de78a86)

-----------------------------------------------------------------------------------------

For this project we are going to using a samba exploit of port 445 - we can ruin (searchsploit) to find any known vulnerabilities for this port 

![Screenshot 2024-08-20 143131](https://github.com/user-attachments/assets/80cd852e-b585-488f-bf04-9ad48281b172)

-----------------------------------------------------------------------------------------

From here once you know what exploit you will be targeting start up metasploit 

![Screenshot 2024-08-20 142252](https://github.com/user-attachments/assets/b791476c-6ed2-473d-b914-ba1731d07e56)

-----------------------------------------------------------------------------------------

from here you can (search Samba) and find the correct exploit we want to use 

![Screenshot 2024-08-20 143248](https://github.com/user-attachments/assets/e039438d-a177-4717-87d3-1e24d5a23983)

-----------------------------------------------------------------------------------------

Now we configure our setting setting the RHOSTS(target machine) 

![Screenshot 2024-08-20 143337](https://github.com/user-attachments/assets/af299145-d3eb-486b-b6f0-da7627e1f053)

-----------------------------------------------------------------------------------------

Now run (exploit) and gain access to their machine by meterpeter

![Screenshot 2024-08-20 153639](https://github.com/user-attachments/assets/240eb7a7-061d-4527-b4b9-b37c80065d92)

-----------------------------------------------------------------------------------------

From here we have full access to their machine and can delete files, run malisuous code. or if this is a pentest you can then go in and patch this exploit or close that port













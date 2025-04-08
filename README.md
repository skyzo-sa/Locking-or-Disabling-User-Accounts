# Linux Lab – Locking or Disabling User Accounts
## Objective

The objective of this script is to block incoming network traffic from a list of specified IP addresses using the iptables firewall in Linux. It automates the process of applying IP-based traffic restrictions for network security purposes.

### Job Skills Learned

- Linux System Administration
- Managing firewall rules using iptables.
- Bash Shell Scripting
- Using loops and conditional commands.
- Network Security and Access Control
- Automation and Efficiency


### Tools Used

- Linux Terminal Command Line Interface (CLI)
- Bash Shell
- iptables (Firewall)
- Networking Commands: ping, ifconfig
- VMware Tools: Linux VM


### STEPS

# Creating a user account
useradd [OPTIONS] username
# OPTIONS:
# -m => create home directory
# -d directory => specify another home directory
# -c "comment"
# -s shell
# -G => specify the secondary groups (must exist)
# -g => specify the primary group (must exist)
![image](https://github.com/user-attachments/assets/c9dc2d6b-f94c-490f-bc75-61f102f211bc)
 

# Locking password authentication
`sudo passwd -l USERNAME`
`sudo password --lock USERNAME`
![image](https://github.com/user-attachments/assets/94ef823a-7e2b-4369-b386-ba1b05dd6db6)
  
# Checking the account status
`sudo passwd --status USERNAME`
`sudo chage -l USERNAME`
![image](https://github.com/user-attachments/assets/b348b08a-ae22-4572-a04a-aaf70ac3022f)
 
 
# Unlocking password authentication
`sudo passwd -u USERNAME`
![image](https://github.com/user-attachments/assets/24a2db71-f5aa-4db6-94f2-938179fc8b45)
 
 
# Disable an account completely
`sudo usermod --expiredate 1 USERNAME`
`sudo usermod --expiredate 1970-01-02 USERNAME`
![image](https://github.com/user-attachments/assets/382e6313-a042-4aea-a305-a555b88e4ba7)
 
 
# Checking the account expiration date
`sudo chage -l USERNAME`
![image](https://github.com/user-attachments/assets/a91ae2da-01ed-4ddd-b6f9-d5ac8f1ca3ac)

 

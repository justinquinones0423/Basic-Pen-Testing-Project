# Basic-Pen-Testing-Project

## In this project that I did with CodePath, I was able to gain hands-on experience in basic penetration testing exploiting a vulnerability on port 21 in a simulated lab experience in their ubuntu virtual machine.

### What I did first as shown in the CodePath Project 4 - Part 1 Comparison.png screenshot was utilizing the lsb release -a command to identify the operating systems of the two terminals which were my regular ubuntu terminal on the left and the metasploitable terminal on the right.

### Secondly, I then utilized Nmap at first to get a general scan of all the ports. Then as shown in the CodePath Project 4 - Part 2 Nmap Port 21.png, I used the nmap 172.17.0.2 --script vuln -p 21 command to specifically see what possible vulnerabilities were present on port 21. I then identified that the vsFTPd version 2.3.4 backdoor was there as a vulnerability and that it was exploitable.

### Upon taking note of that vulnerability, I loaded the metassploit framework console. Once doing so, as shown in CodePath Project 4 - Part 3 Loading Exploit Port 21.png, I entered "use exploit/unix/ftp/vsftpd_234_backdoor". It then says "no payload configured", so I entered "options" and then configured the target IP 172.17.0.2 as the RHOSTS parameter as shown in the CodePath Project 4 - Part 3 Executing Metasploit Port 21.png screenshot. In that same screenshot I entered "exploit" and was able to successfully exploit port 21.

## Lastly, I entered the lsb_release -a command in the exploited shell to demonstrate successful system compromise shown in the CodePath Project 4 - Part 3 Executing Metasploit with outputs Port 21.png screeenshot. 

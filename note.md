## HackTheBox Blurry Machine

### Nmap Service and Port Scan
```shell
nmap -v -sC -sV -oA nmap/tcp 10.10.11.19
```
### Sub-domain Enumeration using Gobuster
```
gobuster dns -d "blurry.htb" -w subdomains-top1million-20000.txt -o dns_enumeration.txt -t 100
```
The following subdomains was found and added to the **/etc/hosts** file
**app.blurry.htb**
**chat.blurry.htb**
**files.blurry.htb**
**api.blurry.htb**

**Note:** Refer to the **dns_enumeration.txt** file in the pentest folder. 

I have come to the conclusion that the software we are dealing with is **clearml** a tool for AI developers to build AI tools.

Open an account 


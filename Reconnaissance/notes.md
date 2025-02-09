
### **1. Passive Reconnaissance**

#### **Step 1: Gather Domain Information**
- **Whois Lookup**:  
  ```bash
  whois qayssarayra.com
  ```
- **DNSDumpster**:  
  Visit: [https://dnsdumpster.com/](https://dnsdumpster.com/)
- **Shodan**:  
  Visit: [https://www.shodan.io/](https://www.shodan.io/)

#### **Step 2: Subdomain Enumeration**
- **Sublist3r**:  
  ```bash
  sublist3r -d qayssarayra.com
  ```
- **Amass**:  
  ```bash
  amass enum -d qayssarayra.com
  ```
- **Crt.sh**:  
  Visit: [https://crt.sh/](https://crt.sh/)

#### **Step 3: Social Media & Web Research**
- **TheHarvester**:  
  ```bash
  theharvester -d qayssarayra.com -b all
  ```

#### **Step 4: Analyze SSL Certificates**
- **SSL Labs' SSL Test**:  
  Visit: [https://www.ssllabs.com/ssltest/](https://www.ssllabs.com/ssltest/)

---

### **2. Active Reconnaissance**

#### **Step 5: Network Scanning**
- **Nmap**:  
  ```bash
  nmap -sS -T1 -Pn --open --min-rate=1000 --max-retries=1 -v --scan-delay 1s --badsum qayssarayra.com
  ```
- **Masscan**:  
  ```bash
  masscan 192.168.1.0/24 --rate=1000 -p1-65535
  ```
- **Netdiscover**:  
  ```bash
  netdiscover -r 192.168.1.0/24
  ```

#### **Step 6: Service Enumeration**
- **Nikto**:  
  ```bash
  nikto -h http://qayssarayra.com
  ```
- **Dirb**:  
  ```bash
  dirb http://qayssarayra.com
  ```
- **Enum4linux**:  
  ```bash
  enum4linux -a 192.168.1.10
  ```

#### **Step 7: Vulnerability Scanning**
- **OpenVAS/GVM**:  
  Use OpenVAS GUI or CLI for scanning.
- **Nessus**:  
  Use Nessus GUI for scanning.
- **Metasploit**:  
  ```bash
  msfconsole
  use auxiliary/scanner/portscan/tcp
  set RHOSTS 192.168.1.10
  run
  ```

#### **Step 8: Exploitation Testing**
- **Burp Suite**:  
  Proxy traffic through Burp Suite manually.
- **SQLmap**:  
  ```bash
  sqlmap -u "http://qayssarayra.com/page?id=1" --dbs
  ```
- **Hydra**:  
  ```bash
  hydra -l admin -P /path/to/passwords.txt ssh://192.168.1.10
  ```

 
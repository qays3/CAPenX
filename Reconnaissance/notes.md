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
- **SecurityTrails**:  
  Visit: [https://securitytrails.com/](https://securitytrails.com/)
- **Censys**:  
  Visit: [https://censys.io/](https://censys.io/)

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
- **Assetfinder**:  
  ```bash
  assetfinder qayssarayra.com
  ```
- **Findomain**:  
  ```bash
  findomain -t qayssarayra.com
  ```

#### **Step 3: Social Media & Web Research**
- **TheHarvester**:  
  ```bash
  theHarvester -d qayssarayra.com -b all
  ```
- **SpiderFoot**:  
  ```bash
  spiderfoot -l -m all -s qayssarayra.com
  ```

#### **Step 4: Analyze SSL Certificates**
- **SSL Labs' SSL Test**:  
  Visit: [https://www.ssllabs.com/ssltest/](https://www.ssllabs.com/ssltest/)
- **SSLyze**:  
  ```bash
  sslyze --regular qayssarayra.com
  ```
- **TLS Scan Misconfiguration**:
  ```bash
  git clone https://github.com/drwetter/testssl.sh.git
  cd testssl.sh && ./testssl.sh qayssarayra.com
  ```

---

### **2. Active Reconnaissance**

#### **Step 5: Network Scanning**
- **Nmap**:  
  ```bash
  nmap -sS -T1 -Pn --open --min-rate=1000 --max-retries=1 -v --scan-delay 1s --badsum qayssarayra.com
  ```
- **Masscan**:  
  ```bash
  sudo masscan 77.37.125.41/24 --rate=1000 -p1-65535
  ```
- **Netdiscover**:  
  ```bash
  netdiscover -r 77.37.125.41/24
  ```
- **RustScan**:  
  ```bash
  rustscan -a 77.37.125.41 -- -A
  ```

#### **Step 6: Service Enumeration**
- **Nikto**:  
  ```bash
  nikto -h http://qayssarayra.com
  ```
- **Ffuf**:  
  ```bash
  ffuf -u http://qayssarayra.com/FUZZ -w /usr/share/wordlists/dirb/common.txt
  ffuf -u http://qayssarayra.com/FUZZ -w /usr/share/wordlists/dirb/common.txt -recursion
  ffuf -u http://qayssarayra.com/FUZZ -w /usr/share/wordlists/dirb/common.txt -fc 403,404
  ffuf -u http://qayssarayra.com/FUZZ -w /usr/share/wordlists/dirb/common.txt -o results.txt
  ```
- **Gobuster**:  
  ```bash
  gobuster dir -u http://qayssarayra.com -w /usr/share/wordlists/dirb/common.txt
  ```
- **Enum4linux**:  
  ```bash
  sudo enum4linux -a 77.37.125.41
  ```
- **WPScan**:  
  ```bash
  wpscan --url http://qayssarayra.com
  ```

 
#### **Step 7: Email Harvesting & Phishing Analysis**
- **Hunter.io**:  
  Visit: [https://hunter.io/](https://hunter.io/)
- **EmailHarvester**:  
  ```bash
  emailharvester -d qayssarayra.com
  ```

 
 

 


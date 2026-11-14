# Week 2 – Cybersecurity Practical Report
## Footprinting and Network Scanning

### 1. Introduction

This practical was conducted as part of the Week 2 cybersecurity project using the NetworkWalks learning materials. The main purpose was to gain hands-on experience with information gathering, footprinting techniques, and network scanning.

The practical focused on two modules:
- **W2-PM2:** GHDB-Based Footprinting Attacks
- **W2-PM5:** Zenmap-Based Network Scanning

These activities provided an opportunity to explore how publicly indexed information can be identified through search operators and how network discovery can be performed using cybersecurity tools.
All network scanning activities described in this report were conducted within my authorised VirtualBox laboratory environment.

---

### 2. Objectives

The objectives of this practical were:

1. To understand the fundamentals of footprinting and information gathering.
2. To explore Google Hacking Database (GHDB) search techniques.
3. To identify publicly indexed information using Google search operators.
4. To understand basic network scanning using Zenmap.
5. To identify the local IP address and subnet information.
6. To gain practical experience using Kali Linux for cybersecurity activities.

---

### 3. Laboratory Environment and Tools

The practical was performed using a virtualised Kali Linux environment.

| Component | Description |
|---|---|
| Operating System | Kali Linux |
| Virtualisation Software | Oracle VirtualBox |
| Footprinting Technique | Google Hacking Database (GHDB) |
| Network Scanning Tool | Zenmap |
| Network Scanning Engine | Nmap |
| Network Configuration | VirtualBox NAT Network |

**Network configuration used:**

| Network Information | Value |
|---|---|
| Local IP Address | 10.0.0.2 |
| Subnet Mask | 255.255.255.0 |
| Network Prefix | /24 |
| LAN Subnet | 10.0.0.0/24 |
| Default Gateway | 10.0.0.1 |

---

### 4. Module 1 – GHDB-Based Footprinting Attacks (W2-PM2)

#### 4.1 Introduction

Footprinting is an information-gathering technique used to identify publicly available information about systems, websites, and network resources.
For this module, I explored the Google Hacking Database (GHDB) approach by using Google search operators, commonly known as Google Dorks.
These search operators help narrow search results and locate specific types of publicly indexed information.

#### 4.2 Activities Performed
The module consisted of two main tasks.

**Task 1: Identifying Security Camera Listings**
The objective was to identify ten publicly accessible security camera listings using relevant Google search operators.

Examples of search techniques included:

- `intitle:` – Searches for specific words in webpage titles.
- `inurl:` – Searches for specific terms within URLs.
- `site:` – Limits search results to a particular website or domain.

The search results were recorded in the provided worksheet together with their corresponding links and search operators.

**Task 2: Finding Mathematics Ebooks in PDF Format**

The second task involved identifying ten mathematics ebook listings available in PDF format.
Search operators such as `filetype:pdf` and `intitle:` were used to narrow down the results and locate relevant documents.
The identified links and corresponding Google Dorks were recorded in the worksheet.

#### 4.3 Results and Observations

Through this activity, I learned how search engines can unintentionally reveal information that website owners may not expect to be easily discoverable.
I also learned that search operators can make information gathering more organised and efficient.

The two tasks demonstrated how publicly indexed resources can be identified through carefully constructed search queries.

**Security consideration:** Publicly indexed links do not automatically grant permission to access private information or control devices. The activity focused on identifying and documenting search results, without attempting to bypass authentication or gain unauthorised access.

---

### 5. Module 2 – Zenmap-Based Network Scanning (W2-PM5)

#### 5.1 Introduction

Zenmap is a graphical user interface for Nmap, a network discovery and security auditing tool.
This module introduced the process of identifying network information and performing basic network scanning within a laboratory environment.

#### 5.2 Laboratory Setup

The scanning activity was performed using Kali Linux running in Oracle VirtualBox.
Before performing the scan, I checked the network configuration to identify the local IP address and LAN subnet.

The network configuration showed:

- IP Address: `10.0.0.2`
- Subnet Mask: `255.255.255.0`
- Network Range: `10.0.0.0/24`
- Gateway: `10.0.0.1`

This information was used to identify the authorised laboratory network for the scanning activity.

#### 5.3 Scanning Process

The following steps were performed:

1. Started the Kali Linux virtual machine.
2. Opened Zenmap through the Kali Linux application menu.
3. Entered the laboratory network range as the target.
4. Selected the Ping Scan option.
5. Executed the scan to perform host discovery.
6. Reviewed the scan output and discovered host information.

The equivalent Nmap command used for the ping scan was:

```bash
nmap -sn 10.0.0.0/24
```

The `-sn` option performs host discovery without carrying out a port scan.

#### 5.4 Results and Observations

Zenmap successfully executed the ping scan against the specified laboratory subnet and produced scan output showing the discovered host information.
During the process, I also noticed that the topology legend displayed the message:

`No traceroute information`

This indicated that traceroute information was not available in the scan results. It did not necessarily indicate that the ping scan had failed, as the selected scan was intended for host discovery.
The activity helped me understand how network scanning tools identify active hosts and display network-related information.

---

### 6. Challenges Encountered
Throughout the practical, I encountered several challenges while setting up and performing the activities.

**1. Understanding Google Search Operators**
Initially, it required some practice to understand how different Google search operators worked together. I had to become familiar with operators such as `intitle:`, `inurl:`, `site:`, and `filetype:` to narrow down relevant search results.

**2. Setting Up the Kali Linux Environment**
Running the practical in a virtual machine required checking the network configuration and ensuring that the correct laboratory environment was being used.

**3. Understanding Network Information**
Identifying the local IP address, subnet mask, and network range helped me understand how devices are organised within a local network.

**4. Interpreting Zenmap Results**
Although the ping scan completed, understanding the displayed scan information and the topology message about missing traceroute information required additional attention.

By following the practical instructions and reviewing the results, I gained a better understanding of how Zenmap presents network discovery information.

---

### 7. Skills and Knowledge Gained

After completing both modules, I gained practical exposure to:

- Basic footprinting and information-gathering techniques.
- Google Hacking Database (GHDB) search operators.
- Identifying publicly indexed resources.
- Using Kali Linux in a virtualised environment.
- Understanding IP addresses and subnet configurations.
- Performing basic network discovery using Zenmap.
- Understanding the relationship between Zenmap and Nmap.
- Interpreting basic network scan output.
- Recognising the importance of authorised security testing.

---

### 8. Conclusion

Overall, this Week 2 cybersecurity practical was a valuable hands-on learning experience that allowed me to apply theoretical cybersecurity concepts using real tools. Through the GHDB-based footprinting activity, I learned how search engines can be used to identify publicly indexed information and why proper information exposure management is important. Through the Zenmap-based network scanning activity, I gained practical experience with Kali Linux, network configuration, and basic host discovery using Nmap. Although I encountered some challenges during the setup and interpretation of scan results, troubleshooting these issues helped me develop a better understanding of the tools and techniques involved. This practical strengthened my interest in cybersecurity, particularly in information gathering, network reconnaissance, and security assessment. It also reminded me that all security testing must be conducted responsibly and within an authorised environment.

**Practical completed:**
- W2-PM2 – GHDB-Based Footprinting Attacks
- W2-PM5 – Zenmap-Based Network Scanning

---

### 9. Evidence and Screenshots

The following evidence can be included in this repository:

1. Kali Linux virtual machine running in VirtualBox.

2. Google Dork search results for security camera listings.
3. Google Dork search results for mathematics PDF resources.
4. Completed W2-PM2 worksheet.
5. Kali Linux network configuration showing the local IP address and subnet.
6. Zenmap target configuration.
7. Zenmap ping scan results.
8. Zenmap topology view.

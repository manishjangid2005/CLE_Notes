# Unit - 1 Networks and the Internet 

## Three Aspects of Information Security:

1. Confidentiality: Ensuring that information is accessible only to those authorized to have access.
2. Integrity: Ensuring that information is accurate and has not been tampered with.
3. Availability: Ensuring that information and resources are available to authorized users when needed.

## IP Addresses
* An IP address (Internet Protocol address) is a unique identifier for devices connected to a network, specifically on the internet. 
* IP addresses ensure that data is sent to the correct destination during network communication. 
* A MAC Address (Media Access Control) is a physical, hardware-layer address assigned to a network interface card (NIC) by the manufacturer. It is unique to the device and remains constant, regardless of the network.

There are two versions of IP addresses:


### IPv4
* The most common version, consisting of 32-bit addresses formatted as four decimal numbers separated by dots (e.g., 192.168.0.1). 
* However, with the increasing number of devices, IPv4 addresses are running out.

### IPv6
* To solve the shortage of IPv4 addresses, IPv6 was introduced. It uses 128-bit addresses, represented as eight groups of hexadecimal numbers 
* (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334), providing a much larger address space.

## Types of	IP address

### Static IP address

* Manually input by network administrator
* Manageable for small networks
* Requires careful checks to avoid duplication

### Dynamic IP address

* Examples - BOOTP,	DHCP
* Assigned by	server when host boots
* Derived automatically from a range of  addresses
* Duration of ‘lease’ negotiated, then address  released back to server

## URL - Uniform Resource Locator
A URL (Uniform Resource Locator) consists of several fields that work together to provide the complete address of a resource on the internet. Below are the main fields of a URL, explained with an example:

Example URL:
https://www.example.com:8080/path/to/page?query=abc

1. Scheme (Protocol)
* Field: https://
* Purpose: Specifies the protocol used to access the resource. Common schemes include HTTP (http), HTTPS (https), FTP (ftp), etc.
* Example: In the URL https://www.example.com, the scheme is https.

2. Host (Domain Name or IP Address)
* Field: www.example.com
* Purpose: The domain name or IP address of the server where the resource is located.
* Example: www.example.com is the domain in the URL.

3. Port
* Ports are logical endpoints used to manage specific types of network traffic.
* Specifies the port number on the server. If omitted, the default port for the scheme is used (e.g., 80 for HTTP, 443 for HTTPS).

4. Path
* Field: /path/to/page
* Purpose: Specifies the specific location or file on the server.



## Basic Network Utilities: IP Config, Ping, Tracert
Basic network utilities help manage, diagnose, and troubleshoot network issues. Some common utilities include:

### IP Config (ipconfig): 
* This command-line utility (on Windows) provides details about the network configuration of a device. 
* It can display the IP address, subnet mask, and default gateway. 
* It displays all current TCP/IP network  configuration values and refreshes DHCP and DNS settings.


### Ping: 
* Ping is a simple utility used to check if a device on a network is reachable. 
* It sends ICMP (Internet Control Message Protocol) echo requests to the target and listens for responses. 
* For example, you can run ping google.com to test if you can reach Google's servers.

### Tracert (or Traceroute): 
* Tracert is a command used to trace the path packets take from your device to a destination. 
* It shows each hop (router or network device) the packet goes through and how long it takes to reach each one. 
* This helps identify where delays or failures occur in the network path.
* For example, tracert google.com will show all the intermediate devices that a request to Google passes through.<br><br>

# Unit - 2 Introduction to Computer Security

## Malware
Malware, short for malicious software, refers to any program or file that is harmful to a computer user. It can be spread via physical means like USB drives or over the internet through methods like drive-by downloads.

### Common types of malware:
* Virus: The most common type that can execute itself and spread by infecting other programs or files.
* Worm: Can self-replicate without a host program and spreads without any human interaction.
* Trojan Horse: Disguised as legitimate software to gain access to the system and execute malicious functions.
* Spyware: Collects data about a user's activities without their knowledge.
* Ransomware: Encrypts a user’s data and demands ransom for decryption.
* Rootkit: Provides attackers with administrator-level access to a system.
* Backdoor Virus or RAT (Remote Access Trojan): Creates a secret backdoor for attackers to remotely access a system.
* Adware: Tracks browsing history to display targeted advertisements.
* Keyloggers: Track everything a user does, including keystrokes.

### Detection and Removal:
* Malware can be detected through unusual behavior like slow speeds, loss of disk space, or increased unwanted internet activity. 
* Tools like antivirus software are essential for detecting and removing malware.

## Denial of Service (DoS) Attacks
A Denial of Service (DoS) attack is when an attacker attempts to make a network or server unavailable to legitimate users by overwhelming it with fake requests.

<img src="https://www.manageengine.com/products/netflow/images/dos-attack.jpeg" width="350">

### Types of DoS Attacks:
* Flooding the Network: Overloading the network to prevent legitimate traffic.
* Disrupting Connections: Interrupting connections between machines, preventing access to services.
* Targeting Individuals: Preventing a specific user from accessing a service.
* Disrupting Service State: Resetting sessions (e.g., TCP) to interfere with ongoing services.

### How to Handle DoS:
* Preparation: Ensuring the network design is robust, implementing detection mechanisms, having a response plan, and considering insurance policies.
* Detection: Analyzing logs and using automated intrusion detection systems.
* Reaction: Following the response plan, limiting traffic, and blocking malicious traffic.

### Web Attacks
Web attacks target websites or web services to compromise their functionality or steal data. Types of web attacks include Cross-Site Scripting (XSS), SQL Injection, and Cross-Site Request Forgery (CSRF).

### DNS Poisoning
DNS poisoning, also known as DNS spoofing, is when attackers corrupt the DNS records, redirecting legitimate traffic to malicious websites. This can be used to steal sensitive information like usernames and passwords by tricking users into interacting with fake websites.

## Session hijacking 
Session hijacking is when an attacker takes control of an active TCP/IP communication session without the user's consent. By hijacking a session, attackers can assume the identity of the compromised user and gain the same access to resources, effectively leading to identity theft, information theft, and the stealing of sensitive data.

### How Session Hijacking Works:
* TCP/IP Sessions: When a user connects to a server (e.g., during a login), a session is established using protocols like TCP. 
* If an attacker manages to capture or guess the session ID, they can hijack the session and act as the legitimate user.

### Impacts of Session Hijacking:
* Identity theft
* Data theft (personal and sensitive information)
* Unauthorized access to systems

### Types of Session Hijacking

1. Active Session Hijacking:
* In an active session hijacking attack, the attacker actively takes control of the session.
* The attacker silences the legitimate user (often by disrupting their connection) and takes over their place in the communication exchange.
* This type of attack allows the attacker to issue commands and interact with the server on behalf of the legitimate user.
* Potential Harm: Attackers can create new user accounts, execute transactions, or access sensitive data on the network.

2. Passive Session Hijacking:
* In passive hijacking, the attacker does not take control of the session but rather monitors the traffic between the legitimate user and the server.
* The goal is to collect information like passwords, session tokens, or other valuable data.
* Since the attacker is simply observing, this form of attack is harder to detect, but it still compromises sensitive data.

Firewall − It is a software or hardware which is used to filter network traffic based on rules.<br>
Antivirus or Antimalware − Is a software that operates on different OS which is used to prevent from malicious software.



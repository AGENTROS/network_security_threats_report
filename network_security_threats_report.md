##### Research Report: An Analysis of Common Network Security Threats



A Detailed Examination of Denial-of-Service, Man-in-the-Middle, and Spoofing Attacks



Prepared for: Professional Audience



Date: OCT 18, 2025



Author: SHARVAN KOUL



Submitted for: Internship Task 4 - Research Report on Common Network Security Threats







##### 1\. Abstract



This report provides a clear and accessible explanation of three prevalent network security threats: Denial-of-Service (DoS), Man-in-the-Middle (MITM), and Spoofing. As organizations increasingly depend on digital infrastructure, understanding these attack vectors has become critical for professionals across all industries. Based on a comprehensive review of technical literature, government publications, and incident case studies, this document details the mechanics, potential impact, real-world examples, and effective mitigation strategies for each threat. The primary aim is to equip a non-specialist professional audience with the foundational knowledge required to recognize and defend against these common and disruptive cyberattacks.











##### 2\. Introduction



As organizations increasingly rely on web-based applications for critical services, securing these platforms against disruptive and authentication-related attacks is paramount. The digital threat landscape has expanded dramatically; according to security reports, cybercrime has escalated by 600% due to the Covid-19 pandemic, and victim losses from cyber-attacks totaled an astonishing $13.3 billion over the past five years. This environment demands a clear understanding of the most common threats that businesses and individuals face daily. This report's primary goal is to dissect three of the most common and impactful categories of network security threats—Denial-of-Service (DoS/DDoS), Man-in-the-Middle (MITM), and Spoofing—making their complex mechanisms understandable for a professional, non-specialist audience. By deconstructing these attacks, this analysis aims to provide actionable insights into their operation and effective countermeasures.









##### 3\. Objectives



The objectives of this report are as follows:



* Objective 1: To define and differentiate between Denial-of-Service (DoS), Distributed Denial-of-Service (DDoS), Man-in-the-Middle (MITM), and various Spoofing attacks.
* Objective 2: To analyze the step-by-step mechanics of how each of these attacks is executed.
* Objective 3: To evaluate the potential impact and consequences of these attacks on individuals and organizations, including operational disruption and financial loss.
* Objective 4: To synthesize and present effective mitigation and prevention strategies for each threat, drawing from established best practices.
* Objective 5: To illustrate the threats with documented, real-world examples and case studies.









##### 4\. Methodology



This report is the result of a comprehensive literature review, synthesizing information from a diverse range of authoritative sources. These include academic papers on network security, government cybersecurity publications, technical case studies of major incidents, and expert analysis from the information security industry. The process involved identifying the core concepts for each attack type and deconstructing their operational mechanics into understandable steps. Real-world incidents were then analyzed to contextualize the theoretical mechanics and demonstrate their tangible impact. Finally, recommended defense and mitigation strategies were compiled and consolidated from multiple sources to present a unified overview of current best practices.









##### 

##### 5\. Tools and Resources



Both attackers and defenders utilize a wide range of software tools to achieve their objectives. Attackers leverage specific programs to orchestrate attacks, while cybersecurity professionals use analysis and monitoring tools to detect and mitigate them. This section lists some of the common tools mentioned in security literature for executing attacks or for network analysis and defense.

###### 

###### Attack and Analysis Tools

###### 

###### \* Aircrack-ng

###### \* Airgeddon

###### \* ARPoison

###### \* Cain e Abel

###### \* DNScat2

###### \* Dsniff

###### \* Ettercap

###### \* Hashcat

###### \* Iodine

###### \* Low Orbit Ion Canon (LOIC)

###### \* Parasite

###### \* tcpdump

###### \* Wireshark

###### 

###### Defense and Monitoring Platforms

###### 

###### \* Intrusion Detection Systems (IDS) like Suricata

###### \* Runtime Application Self-Protection (RASP)

###### \* Security Information and Event Management (SIEM) platforms like  Splunk and the Elastic Stack (Elasticsearch, Kibana)

###### \* Web Application Firewall (WAF)

###### 

###### 





##### 

##### 6\. Common Network Security Threats



This section forms the core of the report, providing a detailed breakdown of three major categories of network attacks. These threats were selected for their prevalence, impact, and the fundamental security principles they challenge. While distinct, these threats are often interconnected. Spoofing can be a precursor to a Man-in-the-Middle attack, and both can be used to harvest credentials for further exploitation or to build botnets for DDoS campaigns. For each threat, the analysis will cover its definition, operational mechanics, potential consequences, effective defensive measures, and notable real-world incidents that highlight its significance.



###### 6.1. Denial-of-Service (DoS/DDoS) Attacks

###### 

###### Definition



A Denial-of-Service (DoS) attack is a malicious assault intended to disrupt the normal function of a service, such as a website or network, preventing legitimate users from accessing it. The attack achieves this by overwhelming the target with traffic or by sending requests that exploit a vulnerability and cause the target system to crash or become unresponsive.



A Distributed Denial-of-Service (DDoS) attack is a more potent variant where the attack traffic originates from multiple, often geographically dispersed, sources. These sources are typically a network of compromised computers and devices known as a botnet. This distributed nature makes DDoS attacks far more difficult to block, as there is no single source IP to blacklist. The primary goal is to exhaust the target's resources, such as bandwidth, CPU processing power, and memory.



###### How it Works



DDoS attacks are most often perpetrated using a botnet—a network of hijacked computers, servers, and Internet of Things (IoT) devices that have been infected with malware. These compromised devices, known as "bots" or "zombies," are controlled remotely by an attacker (the "botmaster") and can be directed to flood a target with traffic simultaneously.

###### 

###### DDoS attacks can be categorized based on the layer of the Open Systems Interconnection (OSI) model they target:



\* Volumetric Attacks (Network Layer): These are the most common type of DDoS attack and aim to saturate the target's bandwidth with a massive amount of traffic. By sending more data than the network can handle, the attack creates a traffic jam that prevents legitimate requests from getting through. Examples include UDP floods and ICMP floods, which use standard network protocols to generate overwhelming volumes of junk traffic.





\* Protocol Attacks (Transport Layer): These attacks exploit vulnerabilities in network protocols to consume the resources of servers or network equipment like firewalls and load balancers. A classic example is the SYN Flood, which exploits the three-way handshake (the SYN, SYN-ACK, ACK process used to establish a TCP connection). The attacker sends a succession of SYN requests (the first step of the handshake) but never sends the final ACK packet to complete the connection. This leaves the server's ports in a half-open, busy state, waiting for a response that never comes, eventually exhausting its capacity to accept new, legitimate connections. This is akin to a mailroom clerk receiving thousands of "return-to-sender" requests but never being told which packages to return. The clerk's desk becomes overwhelmed with pending tasks, and they can no longer process legitimate mail.







\* Application Layer Attacks (Application Layer): These attacks are more sophisticated and target the layer where web pages are generated and delivered. They mimic legitimate user traffic, making them harder to detect. For example, Multiple HTTP GET/POST Flooding overwhelms a server by repeatedly requesting resource-intensive web pages or submitting data through web forms. More stealthy variants, known as "Low and Slow" attacks, include methods like R-U-Dead-Yet (RUDY), which opens a connection and sends partially formed requests very slowly, tying up server resources for extended periods to exhaust its connection table.

###### 

###### Impact and Consequences



The consequences of a successful DDoS attack can be devastating. They include widespread service disruption for legitimate users, leading to severe financial loss. According to the Information Technology Intelligence Consulting (ITIC), a single hour of downtime can cost an organization between $300,000 and $1,000,000. Beyond the immediate financial impact, DDoS attacks cause significant reputational damage, eroding customer trust and confidence in the targeted organization's ability to provide reliable and secure services.



###### Mitigation and Preventive Measures



A multi-layered defense is required to effectively mitigate DDoS attacks.



\* Network Configuration: Properly configure firewalls and routers to reject bogus traffic and ensure all network devices are updated with the latest security patches to close known vulnerabilities.





\* Packet Filtering: Implement filtering techniques to identify and drop illegitimate packets. Hop Count Filtering (HCF), for instance, validates incoming packets by checking their Time-To-Live (TTL) field against an expected value, helping to identify spoofed traffic.





\* Rate-Limiting: Set thresholds on routers and firewalls to limit the number of requests a single IP address or a range of addresses can make in a given timeframe. This can help slow down volumetric and application-layer floods.





\* Web Application Firewalls (WAFs): A WAF acts as a shield at the network perimeter, specifically designed to filter, monitor, and block malicious HTTP traffic targeting web applications. It can identify and stop application-layer attacks that might bypass traditional firewalls.





\* DDoS Mitigation Services: For large-scale attacks, partnering with a dedicated DDoS protection service is crucial. These services operate massive, globally distributed networks with the capacity to absorb and filter enormous volumes of attack traffic before it ever reaches the organization's infrastructure.



##### Real-World Examples



\* The 2016 Dyn Attack: One of the most infamous DDoS attacks in history was launched against the DNS provider Dyn. The attack was executed by the Mirai malware, which created a massive botnet by compromising tens of thousands of insecure Internet of Things (IoT) devices like cameras, printers, and baby monitors. The resulting flood of traffic crippled Dyn's services, causing widespread outages for major websites including Netflix, Amazon, Reddit, and The New York Times.





\* The 2018 GitHub Attack: In February 2018, the software development platform GitHub was hit with what was, at the time, one of the largest recorded DDoS attacks, peaking at 1.3 Terabits per second (Tbps). This attack utilized a memcached amplification technique. This is a reflection-amplification attack: the attacker sends a small request to a third-party server (the memcached server) while spoofing the victim's IP. The server then sends a massively larger response to the victim. It's like sending a postcard asking for a full encyclopedia set to be delivered to someone else's address. Fortunately, GitHub's DDoS protection service detected the anomaly and mitigated the attack within 20 minutes.





\* The 2020 Amazon Web Services (AWS) Attack: This incident set a new record, demonstrating the escalating scale of these threats. AWS successfully mitigated a DDoS attack that culminated at a volume of 2.3 Tbps. The attack highlighted the growing power of botnets and the critical importance of robust, cloud-scale defense infrastructure.



##### 6.2. Man-in-the-Middle (MITM) Attacks

###### 

###### Definition



A Man-in-the-Middle (MITM) attack is a form of cyber eavesdropping where an attacker secretly intercepts and relays communications between two parties who believe they are communicating directly with each other. The attacker positions themself in the "middle" of the conversation, allowing them to observe, inject, and alter traffic without the users' knowledge. This effectively compromises the confidentiality and integrity of the entire communication channel.



###### How it Works



MITM attacks can be executed through several vectors, often by exploiting unsecured networks or manipulating network protocols.



\* Wi-Fi Eavesdropping: This is one of the most common MITM vectors, frequently occurring on public Wi-Fi networks. An attacker sets up a malicious Wi-Fi access point, often with a legitimate-sounding name like "Free\_Airport\_WiFi" or "Cafe\_Guest\_WiFi." This is known as an "Evil Twin" attack. When unsuspecting users connect, all their unencrypted internet traffic passes through the attacker's system, allowing the attacker to monitor their activity, capture login credentials, and steal sensitive information.





\* ARP Spoofing (or ARP Cache Poisoning): On a local area network (LAN), devices use the Address Resolution Protocol (ARP) to map IP addresses to physical MAC addresses. Both ARP and DNS Spoofing are foundational techniques for network traffic interception, making them primary enablers for Man-in-the-Middle attacks. In an ARP spoofing attack, the attacker sends forged ARP messages across the network to associate their own MAC address with the IP address of a legitimate device, such as the network's gateway router. This tricks other devices on the network into sending their internet-bound traffic to the attacker's machine instead of the legitimate gateway, allowing the attacker to intercept it.





\* DNS Spoofing: This technique involves corrupting the records of a Domain Name System (DNS) server to redirect users to malicious websites. For example, an attacker could alter the DNS entry for mybank.com to point to a fake website they control. When a user tries to visit their bank's website, their browser is directed to the attacker's fraudulent site, which may be designed to look identical to the real one to harvest login credentials.





\* SSL/HTTPS Hijacking: An attacker first intercepts the user's initial, unencrypted request to connect to a secure website. The attacker then presents a fake security certificate to the user's browser. If the user ignores the browser's warning and proceeds, an encrypted session is established with the attacker—not the real website. The attacker, in turn, creates a separate, legitimate encrypted session with the real website, allowing them to decrypt, read, and modify all traffic passing between the user and the server.



###### Impact and Consequences



The risks associated with MITM attacks are severe. Successful attacks can lead to the theft of sensitive personal and financial information, such as login credentials, credit card numbers, and private messages. Attackers can also perform session hijacking to gain unauthorized access to user accounts, corrupt transmitted data, or deploy malware onto the victim's device. Ultimately, a MITM attack results in a complete loss of data confidentiality and integrity.



###### Mitigation and Preventive Measures



Defending against MITM attacks requires a combination of technical controls and user awareness.



\* Strong Encryption: Ensure that all data in transit is protected using secure communication protocols like Transport Layer Security (TLS), particularly modern versions such as TLS 1.3. Websites should enforce HTTPS to encrypt all traffic between the user and the server.





\* Virtual Private Networks (VPNs): Using a VPN is highly recommended, especially when connected to public or unsecured Wi-Fi networks. A VPN creates a secure, encrypted tunnel for all internet traffic, preventing local eavesdroppers from intercepting the data.





\* Secure Wireless Protocols: Home and corporate wireless networks should be configured to use strong security protocols like WPA3, which offers enhanced protection against eavesdropping and prevents many common Wi-Fi-based attacks.





\* End-to-End Encryption (E2EE): For messaging applications, using services that provide E2EE (like Signal) is critical. E2EE ensures that only the sender and the intended recipient can read the messages, preventing even the service provider from intercepting the communication. To confirm that no MITM is present, users should perform out-of-band verification (e.g., comparing security codes in person, over a trusted phone call, or via another secure channel) by comparing security codes or fingerprints.



###### Real-World Examples



A typical MITM scenario unfolds in a public space like a coffee shop. A user connects to a rogue Wi-Fi hotspot named "Free Cafe Wi-Fi," which is actually controlled by an attacker. The user browses to a non-HTTPS website to log into a forum. The attacker, monitoring the unencrypted traffic, captures the user's username and password in plaintext. Later, the user logs into a social media site. The attacker intercepts the session cookie and uses it to hijack the active session, gaining full, unauthorized access to the user's account without needing the password.



##### 6.3. Spoofing Attacks



Definition



Spoofing is a broad category of attacks where a malicious actor successfully impersonates another person, device, or computer system to gain the trust of a target. The core of a spoofing attack is the use of false information to deceive a recipient into believing the communication is from a legitimate and trusted source. The ultimate goal is often to gain unauthorized access, steal information, or spread malware.



How it Works



Spoofing can manifest in several distinct forms, each targeting a different communication protocol or system.



*  E-Mail Spoofing: This involves forging the sender address (the "From" field) in an email to make it appear as if it came from a trusted source, such as a colleague, a bank, or a well-known company. E-mail spoofing is a primary enabler of phishing attacks, where the goal is to trick users into revealing sensitive information like passwords or credit card numbers. It is also used to spread malware via malicious attachments or to damage a person's reputation by sending fraudulent emails in their name.





*  IP Spoofing: In this attack, an attacker creates Internet Protocol (IP) packets with a modified source address to hide the sender's identity or to impersonate another computer system. This is often a component of DoS attacks. This is typically a "blind" attack, meaning the attacker sends packets but cannot receive the target's replies, as they are sent to the legitimate, spoofed IP address.





*  ARP Spoofing: As described in the MITM section, this is a specific type of spoofing that occurs on a local network. An attacker sends falsified ARP messages to link their machine's MAC address with the IP address of a legitimate user or server on the network. This allows the attacker to intercept, modify, or stop traffic intended for the legitimate device and is a key enabler for MITM attacks.





*  DNS Spoofing: Also a key enabler for MITM, DNS spoofing (or DNS cache poisoning) is an attack that compromises a DNS server to redirect traffic to a malicious site. The process is as follows:

  1. An attacker alters the DNS entry for a legitimate website (e.g., www.mybank.com) on a vulnerable DNS server.

  2. A customer queries the DNS server for the IP address of www.mybank.com.

  3. The compromised DNS server responds with the attacker's fake IP address.

  4. The customer's browser unknowingly connects to the attacker's fraudulent site, which may be designed to steal their credentials.



##### Impact and Consequences



The consequences extend beyond immediate system access. Successful spoofing facilitates credential harvesting (phishing), which directly fuels the underground economy for stolen accounts and enables more sophisticated intrusions. By impersonating trusted entities, attackers can bypass network access controls, distribute malware, and facilitate larger, more complex attacks, such as large-scale DDoS or sophisticated MITM operations.



###### Mitigation and Preventive Measures



Defenses against spoofing must be tailored to the specific type of attack.



*  For E-Mail Spoofing: Organizations should implement and enforce a trio of email authentication protocols:





*  Sender Policy Framework (SPF): Allows domain owners to specify which mail servers are authorized to send email on their behalf.







*  DomainKeys Identified Mail (DKIM): Adds a digital signature to outgoing emails, allowing the receiving server to verify that the message has not been altered in transit.





*  Domain-based Message Authentication, Reporting, and Conformance (DMARC): A policy layer that builds on SPF and DKIM, telling receiving servers what to do with emails that fail authentication (e.g., quarantine or reject them).





*  For IP Spoofing: Network administrators should use packet filtering systems to block packets with illegitimate source IP addresses.





*  Ingress Filtering: Checks incoming packets to ensure they are from their claimed source network.





*    Egress Filtering: Checks outgoing packets to ensure they have source IP addresses from within the local network, which prevents users inside the network from launching outbound spoofing attacks.





*  For ARP Spoofing: On smaller networks, using static ARP tables can manually map IP addresses to the correct MAC addresses. On larger networks, many managed network switches offer features like MAC binding, which can prevent unauthorized changes to the ARP cache.



###### Real-World Examples



A common example of email spoofing involves a social engineering attack within a company. An employee receives an email that appears to be from administrator@company.net. The email contains an urgent message stating that their network password is about to expire and instructs them to click a link to update it immediately. The link leads to a fake login page, visually identical to the company's real portal, which is designed to harvest the employee's username and password.









##### 7\. Challenges and Limitations in Defense



Despite the availability of a wide array of defensive measures, significant challenges remain in protecting networks from these common threats. The cybersecurity landscape is a constant "arms race," and attackers are continually adapting their strategies to circumvent even the most robust defenses.



* Evolving Tactics: Attackers constantly change their methods to evade detection. For example, modern DDoS botnets use millions of unique IP addresses and send very few requests from each one, a tactic designed to stay below the thresholds of static rate-limiting rules. Similarly, MITM attackers leverage public Wi-Fi's inherent trust model, and phishers use sophisticated social engineering to bypass technical controls, demonstrating that attackers consistently adapt their methods to exploit both technical and human vulnerabilities.





* The Human Factor: Many attacks, particularly those involving social engineering, phishing, and connecting to unsecured public Wi-Fi, successfully exploit human error, curiosity, or a simple lack of security awareness. Technology alone cannot protect an organization if its users are not trained to recognize and avoid common traps.





* Stealth and Deception: By their very nature, MITM and spoofing attacks are designed to be invisible to their victims. They mimic legitimate communications and often leave no obvious trace, making them inherently difficult to detect until after the damage has been done.





* Fundamental Protocol Weaknesses: Some attacks exploit inherent weaknesses in foundational internet protocols that were designed decades ago without modern security threats in mind. Protocols like ARP (for local networking) and SMTP (for email) were not originally built with strong authentication, making them susceptible to spoofing.



* Scale and Complexity: The sheer scale of modern DDoS attacks, reaching multiple terabits per second, can overwhelm the resources of all but the most prepared organizations. Furthermore, the increasing complexity of corporate networks—spanning on-premises data centers, multiple cloud providers, and remote workforces—creates a vast and difficult-to-defend attack surface.









##### 

##### 8\. Conclusion and Future Work



This report has detailed the mechanisms, impact, and mitigation strategies for three of the most persistent threats in cybersecurity: Denial-of-Service, Man-in-the-Middle, and Spoofing attacks. It is clear that these are not isolated or static threats; they are evolving, often used in combination, and continue to pose a significant risk to organizations of all sizes. The analysis underscores that there is no single "silver bullet" solution. Effective defense requires a multi-layered, defense-in-depth security posture that combines robust technical controls (such as encryption, packet filtering, and modern authentication protocols), continuous monitoring and anomaly detection, and, critically, comprehensive and ongoing user education.



Looking ahead, the "arms race" in cybersecurity will undoubtedly continue and accelerate. Future developments will likely see the increased use of Artificial Intelligence (AI) and Machine Learning (ML) by both sides. Attackers will leverage AI to create more adaptive and evasive malware and to automate the discovery of vulnerabilities. In response, defenders are already deploying AI and ML to build more sophisticated, behavior-based threat detection and response systems that can identify novel attacks in real time without relying on known signatures. For any organization to remain resilient in this dynamic landscape, proactive vigilance, a commitment to continuous learning, and strategic investment in modern security frameworks are not just recommended—they are essential.









##### 9\. References



1. Babu, P. R., Bhaskari, D. L., \& Satyanarayana, C. (2010). A Comprehensive Analysis of Spoofing. International Journal of Advanced Computer Science and Applications, 1(6).



2\. Canadian Centre for Cyber Security. (2022). ITSP.30.035 Strategies for Protecting Web Application Systems Against Credential Stuffing Attacks.



3\. Centraleyes. (n.d.). What is Man-in-the-Middle Attack? Types \& How to Detect. Retrieved May 24, 2024, from https://www.centraleyes.com/glossary/man-in-the-middle-attack/



4\. Contrast Security. (n.d.). WAF and RASP: Raising the bar for application protection. Retrieved May 24, 2024, from Contrast Security.



5\. Datalink Networks. (2024). Preventing Email Spoofing: A Guide to DMARC Implementation. Retrieved May 24, 2024, from https://www.datalinknetworks.net/blog/preventing-email-spoofing-a-            guide-to-dmarc-implementation



6\. Firch, J. (2021). 2021 Cyber security statistics: The ultimate list of stats, data \& trends. PurpleSec. As cited in International Journal on Semantic Web and Information Systems, 18(1).



6\. GeeksforGeeks. (n.d.). What is DDoS(Distributed Denial of Service)? Retrieved May 24, 2024, from https://www.geeksforgeeks.org/what-is-ddosdistributed-denial-of-service/



7\. Indusface. (n.d.). Mitigating a Botnet-Driven DDoS Attack on a Fortune 500 Company. Retrieved May 24, 2024, from Indusface.



8\. Mallik, A. (2024). A Review on Man-in-the-Middle Attack: Threats, Intrusion, Detection, and Prevention. World Journal of Advanced Engineering Technology and Sciences, 13(2), 919-933.



9\. OWASP. (n.d.). Manipulator-in-the-middle attack. Retrieved May 24, 2024, from https://owasp.org/www-community/attacks/Manipulator-in-the-middle\_attack



10\. Podder, S. (n.d.). IT - Case Study: Dyn DDoS attack (2016), GitHub DDoS attack (2018). Scribd. Retrieved May 24, 2024, from https://www.scribd.com/presentation/679124409/IT-Case-Study



11\. Salat, L., Davis, M., \& Khan, N. (2023). DNS Tunnelling, Exfiltration and Detection over Cloud Environments. Sensors, 23(5), 2760.


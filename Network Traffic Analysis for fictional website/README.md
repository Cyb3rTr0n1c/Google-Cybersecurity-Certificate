# 🕵️‍♂️🔍 Network Traffic Analysis for YummyRecipesForMe

## 🎯 Objective
The goal of this project is to analyze DNS and ICMP traffic in transit to identify which network protocol was impacted during a cybersecurity incident affecting the website www.yummyrecipesforme.com. The analysis will help determine the cause of the issue and provide insights into potential network vulnerabilities.

## 📖 Scenario
You are a cybersecurity analyst working for an IT services company. Several customers have reported that they are unable to access the client company website www.yummyrecipesforme.com, receiving the error “destination port unreachable.” Your task is to investigate the issue using a network protocol analyzer tool (tcpdump), identify the affected network protocol, and determine the root cause of the problem.

Your analysis will involve reviewing tcpdump logs to trace the flow of network traffic, identify any errors, and understand the implications of these errors on the network’s security.

### 📚 Skills Learned
- 🛡️ Identification and analysis of network protocols and traffic.
- 🧠 Critical thinking and problem-solving in cybersecurity contexts.
- 📋 Documentation and reporting of network security incidents.

### 🛠️ Tools Used
- 🖥️ Network protocol analyzer (e.g., tcpdump) for capturing and analyzing network traffic.
- 🌐 Understanding of TCP/IP model layers and network protocols (e.g., DNS, ICMP).

## 📝 Steps
Steps followed to conduct the network traffic analysis:

1. **🔍 Review Supporting Materials**
   - Access and review the following documents:
     - tcpdump log of the incident
     - TCP/IP model layers
     - Network protocol descriptions

2. **📊 Analyze the Traffic**
   - Load the tcpdump log and examine the timestamps, source and destination IP addresses, and protocol details.
   - Identify the sequence of network events leading up to the “destination port unreachable” error.
   ![Image Log](logs.png)


3. **📝 Document Findings**
   - Record the details of the DNS request and the ICMP error message.
   - Determine the cause of the error and which network protocol was affected.

4. **📋 Report the Incident**
   - Prepare a follow-up report detailing your analysis, findings, and recommendations for addressing the issue.

## 🔍 Step-By-Step Instructions

1. **🔍 Review Supporting Materials**
   - Open the tcpdump log file to analyze the captured network traffic data.

2. **📊 Analyze the Traffic**
   - The first two lines of the log show the initial outgoing DNS request from your computer (192.51.100.15) to the DNS server (203.0.113.2.domain).
   - The third and fourth lines show the ICMP error message indicating that the UDP packet was undeliverable to port 53 of the DNS server.

3. **📝 Document Findings**
   - The DNS request was sent in a UDP packet to the DNS server to retrieve the IP address for the domain www.yummyrecipesforme.com.
   - The ICMP error message “udp port 53 unreachable” indicates that the DNS server was not available to process the request, leading to the failure to resolve the domain name.

4. **📋 Report the Incident**
   - The network protocol impacted during this incident was DNS, as the UDP packets sent to port 53 of the DNS server were not successfully delivered.
   - The ICMP protocol provided the error message indicating the issue.

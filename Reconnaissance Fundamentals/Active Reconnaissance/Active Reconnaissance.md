▪ Active Reconnaissance is the act of gathering detailed information about the target
▪ This can include things like: port, service, version and more 
▪ Active Reconnaissance is also called scanning or enumeration, since each technique is actively generating traffic (in form of packets) and the results lies on the output 
▪ In a nutshell, every scanner sends specifically crafted packets, and based on their responses, it can determine the desired results 
▪ Active Reconnaissance usually is the next step after the passive one 
▪ The idea here is to collect more detailed information about the target 
▪ Use that information for basic context for vulnerabilities

## Port Scanning

Port scanning is one of the main enumeration techniques on every engagement.
It is usually done with nmap.
▪ Port scanning is sending packets on different ports, and based on the output determines if the port is open, closed and filtrated 
	▪ While open and close states are self explanatory, filtrated means that the port is behind a firewall, and the scanner cannot determine it's state
Port scanners like nmap can send packets on both transport layers (TCP, UDP)
▪ Port scanners like nmap have extended functionality, with given flags it can determine the running services on the opened ports

▪ If nmap fails to enumerate service and version, the port must be manually enumerated with netcat(nc)

▪ The idea of having opened ports is to host services on it 
▪ Mostly encountered services are: 
▪ FTP (Port 21) 
▪ HTTP/S (Port 80, 443) 
▪ SSH (Port 22) 
▪ HTTP/S Proxy (Port 8080, 8443) 
▪ SMTP (Port 25)

## Service Enumeration
▪ Each service is running its own software, having version and possible vulnerabilities
▪ It is essential to enumerate every single service on the targeted host, including as much details as possible 
▪ This can be done with nc or specific services (like BurpSuite)

## Enumerating FTP

▪ FTP is a service for file sharing, when enumerating the idea is to: 
▪ Enumerate the FTP Version 
▪ Enumerate the FTP Configuration (can we log in anonymously?) 
▪ If both, the version is updated and anon login is disabled, keep ftp at your backpack, you may further compromise credentials, valid for the service

## Enumerating HTTP/S

▪ Most usually, port 80 and 443 are being opened, these are HTTP/S ports 
▪ Most likely web applications can be found hosted on them 
▪ Web applications are whole new domain with various of specific (for web) vulnerabilities
▪ In a nutshell, when enumerating web application we are interested in: 
▪ Backend / Frontend technology or framework 
▪ Web server software and its version 
▪ Mapping the web application (seeing how it works, what it is all about) 
▪ Finding hidden files and directories 
▪ Finding hidden gems, like phpinfo, swagger and more 
▪ Quick wins (hardcoded / default credentials)

## Enumerating SMTP

▪ When enumerating SMTP, the idea is to: 
▪ Enumerate service version 
▪ Interact with the service, enumerate server name 
▪ Interact with the service, enumerate valid commands

# TOOLS
- Discover (https://github.com/leebaird/discover) can be used as active enumeration as well

- ▪ Maltego (https://www.maltego.com/) is software for data collection and visualization. It can perform BOTH passive and active scans, so you must be careful with it 	▪ It can be used as a context or investigation map ▪ It uses GUI and is easy to use ▪ It is OS independent

 -  Nmap is the widely used port scanner. Tools from here on out are doing only active enumeration ▪ Nmap is wide tool with a lot of options, it can perform TCP/UDP port enumeration ▪ It has the ability to: 
		- ▪ Manually filter what tcp packet to send 
		- ▪ Perform Firewall Bypassing 
		- ▪ Scanning for vulnerabilities with its own scripting engine ▪ A lot more after the break

	Netcat 
		▪ Nc is the swiss army knife of the penetration testers 
		▪ On its core, nc is a software able to connect to any remote service, and send any kind of custom packets 
		▪ It can be used for file transfers 
		▪ As well as reverse / bind shells 
		▪ And it was invented as a sysadmin tool … (Yes there is a windows version of it too) 
		▪ Of course, it was built with C

	Nikito 
	▪ Nikto is a web application scanner 
	▪ It scans for: 
	▪ Hidden gems like .robots.txt 
	▪ Backup files 
	▪ Basic misconfigurations

	Gobuster / dirb
▪ Gobuster and dirb are tools for directory brute forcing 
▪ Their idea is to scan for hidden directories and files

## Nuclei 

Nuclei is a modern, high-performance vulnerability scanner that leverages simple YAML-based templates. It empowers you to design custom vulnerability detection scenarios that mimic real-world conditions, leading to zero false positives.

- Simple YAML format for creating and customizing vulnerability templates.
- Contributed by thousands of security professionals to tackle trending vulnerabilities.
- Reduce false positives by simulating real-world steps to verify a vulnerability.
- Ultra-fast parallel scan processing and request clustering.
- Integrate into CI/CD pipelines for vulnerability detection and regression testing.
- Supports multiple protocols like TCP, DNS, HTTP, SSL, WHOIS JavaScript, Code and more.
- Integrate with Jira, Splunk, GitHub, Elastic, GitLab.
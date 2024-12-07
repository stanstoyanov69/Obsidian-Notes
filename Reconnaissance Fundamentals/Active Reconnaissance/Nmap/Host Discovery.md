Let’s start with the first question: who is online? This task aims to find out how to use Nmap to discover the live hosts. Nmap uses various sophisticated ways to discover live hosts.

Before we start, we should mention that Nmap uses multiple ways to specify its targets:

- IP range using `-`: If you want to scan all the IP addresses from 192.168.0.1 to 192.168.0.10, you can write `192.168.0.1-10`
- IP subnet using `/`: If you want to scan a subnet, you can express it as `192.168.0.1/24`, and this would be equivalent to `192.168.0.0-255`
- Hostname: You can also specify your target by hostname, for example, `example.thm`

Let’s say you want to discover the online hosts on a network. Nmap offers the `-sn` option, i.e., ping scan. However, don’t expect this to be limited like `ping`. Let’s see this in action.

Before we get started, we should note that throughout this room, we are either running `nmap` as `root` or using `sudo` because we don’t want to restrict Nmap’s abilities with our account privileges. Running Nmap as a local (non-root) user would limit us to fundamental types of scans such as ICMP echo and TCP connect scans; we will revisit this at the end of this room.

### Scanning a “Local” Network

In this context, we use the term “local” to refer to the network we are directly connected to, such as an Ethernet or WiFi network. In the first demonstration, we will scan the WiFi network to which we are connected. Our IP address is `192.168.66.89`, and we are scanning the `192.168.66.0/24` network. The `nmap -sn 192.168.66.0/24` command and its output are shown in the terminal below.Because we are scanning the local network, where we are connected via Ethernet or WiFi, we can look up the MAC addresses of the devices. Consequently, we can figure out the network card vendors, which is beneficial information as it can help us guess the type of target device(s).

When scanning a directly connected network, Nmap starts by sending ARP requests. When a device responds to the ARP request, Nmap labels it with “Host is up”.
# Network Port Scanning Task

**Objective:** Scan the local network for open ports using Nmap and analyze potential security risks.

**Network Range Scanned:** 192.168.1.0/24  
**Tool Used:** Nmap 7.98

## Devices and Open Ports

| IP Address     | Open Ports                 | Service(s)                  | Potential Risk / Notes |
|----------------|---------------------------|-----------------------------|-----------------------|
| 192.168.1.1    | 21,22,23,53,80,443        | FTP, SSH, Telnet, DNS, HTTP, HTTPS | FTP/SSH could be brute-forced; HTTP/HTTPS admin interface exposed |
| 192.168.1.2    | 80,554,8000               | HTTP, RTSP, HTTP-alt        | Camera web interface; default credentials risk |
| 192.168.1.4    | None open                 | N/A                         | vivo Mobile device, no open ports |
| 192.168.1.6    | 7 (filtered)              | Echo                        | Unknown device; port filtered |
| 192.168.1.9    | 80,7070                   | HTTP, RealServer            | Unknown/DVR; default credentials risk |
| 192.168.1.10   | 135,139,445,5357          | MSRPC, NetBIOS, SMB, WSDAPI | Windows file/printer sharing; firewall recommended |

## Summary / Recommendations

- Found 6 active hosts in the network.
- Ports like FTP, SSH, SMB, and HTTP interfaces are potentially exploitable if default credentials are used.
- IoT devices (camera/DVR) often have default passwords — change them for security.
- Keep firewalls enabled and unnecessary services disabled on PCs.

## Commands Used

```bash
nmap -sS 192.168.1.0/24 -oN scan_results.txt

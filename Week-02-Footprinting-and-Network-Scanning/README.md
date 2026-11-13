# Week 02 – Footprinting and Network Scanning

## Project Overview

This week focused on cybersecurity reconnaissance, footprinting, and network discovery using Kali Linux tools.

The practical exercises covered:
- Information gathering using theHarvester.
- Network discovery and host identification using Zenmap (Nmap).

All activities were conducted within the scope of the internship project authorization.

## Module 1: W2-PM4 – theHarvester-Based Footprinting

### Objective
To use theHarvester to gather publicly available information associated with the authorized target domain, `networkwalks.com`.

### Tool Used
- theHarvester 4.10.1
- Kali Linux 2026.2

### Methodology

TheHarvester was executed against the authorized domain using three data sources:

1. crt.sh
2. DuckDuckGo
3. Baidu

### Commands Used

```bash
theHarvester -d networkwalks.com -b crtsh
theHarvester -d networkwalks.com -b duckduckgo
theHarvester -d networkwalks.com -b baidu
```

### Findings

All three sources returned the following:

- No IP addresses found.
- No email addresses found.
- No people identified.
- No hosts returned.

These results indicate that the selected sources did not return matching records during the tests. They do not establish that the target has no publicly available information.

### Screenshots

See the `Screenshots/theHarvester/` directory.

## Module 2: W2-PM5 – Zenmap-Based Network Scanning

### Objective
To identify active devices within my own VirtualBox laboratory network using Zenmap.

### Environment

- Operating System: Kali Linux 2026.2
- Network: `10.0.0.0/24`
- Kali Linux IP: `10.0.0.2`
- Tool: Zenmap
- Nmap version: 7.99

### Scan Configuration

- Target: `10.0.0.0/24`
- Profile: Ping scan
- Nmap option: `-sn`

The ping scan was used for host discovery without performing port scanning.

### Results

A total of 256 IP addresses were considered in the subnet, and three active hosts were discovered.

| IP Address | Identified Device |
|---|---|
| 10.0.0.1 | VirtualBox NAT gateway |
| 10.0.0.2 | Kali Linux virtual machine |
| 10.0.0.254 | VirtualBox DHCP server |

### Scan Statistics

- Active hosts: 3
- Inactive hosts: 253
- Scan duration: Approximately 3.02 seconds.
- Port scanning: Not performed.

### Host Details

The VirtualBox gateway (`10.0.0.1`) was selected for additional host-detail inspection.

The displayed information included its IPv4 address, MAC address, and host status.

### Screenshots

See the `Screenshots/Zenmap/` directory.

## Challenges and Observations

- The selected theHarvester sources returned no matching records.
- The virtual laboratory network exposed three active devices during host discovery.
- The Ping scan profile was useful for identifying active hosts without conducting port scans.

## Conclusion

The Week 2 practical exercises provided hands-on experience with passive information gathering and local network host discovery.

The exercises improved my understanding of reconnaissance tools, network identification, scan configuration, evidence collection, and technical documentation.

## Scope and Ethical Considerations

All activities were limited to the authorized internship target and my own controlled laboratory network.

No exploitation, unauthorized access, password attacks, or disruptive testing was performed.

This documentation represents practical laboratory work and should not be interpreted as a professional security assessment of the target organization.

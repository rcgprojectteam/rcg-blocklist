# RCG Blocklist

Public blocklist for the RCG firewall fleet. Entries are supplied by RCG; inclusion is not an independent determination of malicious activity.

## Feed URLs

- Combined IPv4 addresses, IPv4 CIDR subnets, and FQDNs: https://raw.githubusercontent.com/rcgprojectteam/rcg-blocklist/main/blocklist.txt
- IPv4 addresses and subnets only: https://raw.githubusercontent.com/rcgprojectteam/rcg-blocklist/main/ipv4.txt
- FQDNs only: https://raw.githubusercontent.com/rcgprojectteam/rcg-blocklist/main/fqdn.txt

Each feed uses UTF-8 plain text, one entry per line, with no header or comments. URLs require no credentials. Use the combined feed only when your firewall supports mixed IP and FQDN entries. Otherwise configure the separate feeds according to the firewall documentation. Firewall import compatibility has not been verified.

## Maintenance

Edit `blocklist.txt` to add or remove entries. Keep `ipv4.txt` and `fqdn.txt` synchronized with the combined file in the same commit. IPv4 subnets use CIDR notation; FQDN entries contain only the hostname, without a scheme, path, or wildcard. Do not replace domains with resolved IP addresses, which may change or be shared.

The files and their Git history are public. Do not include credentials or private customer information. GitHub raw responses may be cached, and firewall refresh timing is controlled by each firewall.

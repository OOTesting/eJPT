# Information Gathering

## Passive Information Gathering

Passive information gathering is the first stage of pen testing,below covers information collection from public and company wide system.

- Website recon & footprinting
    - robots.txt:  allows us to specify what folder or files we don’t want, search engines to index 
    - sitemap.xml: file to provide search engines an organized way of index (URL/sitemap.xml)
used to do Stealthy scan
    - use add-ons like BuiltWith & Wappalyzer
    - whois enumeration - Whois target.com : WHOIS is a public database that houses the information collected when someone registers a domain 
    - Netcraft - netcraft.com : Used to do a lookup on the target gives information of the website
- dnsrecon
    - dnsrecon -d target.com : basic reconnaissance of DNS records for the domain
    - dnsdumpster.com
- WAF detection
    - wafw00f tool
    - it is preinstalled in Kali
    - usage - wafw00f target.com
- subdomain enumeration
    - sublist3r : tool to discover subdomains of a target domain.
    - Amass
    - subfinder
    - crt.sh
    - You can check the usage of this tools ONLINE
- Google dorking
    - site:target.com
    - site:target.com inurl:admin
    - site:*.target.com
    - site:*.target.com intitle:admin
    - filetype:log inurl:"/logs/" : logs capture
    - For more google dorking techniuqes check this website
- Email Harvesting
    - tool → theHarvester
    - usage → theHarvester -d [target.com](http://target.com) -b google, linkedin
- Leaked Password Database
    - haveibeenpwned.com

## Active Information Gathering

- DNS Zone Transfer
    - tools → dnsenum & dig
    - usage → dnsenum zonetransfer.me
- Host Discovery with Nmap
    - usage → sudo nmap -sn <target IP>/24
- Port Scanning with Nmap
    - nmap -p <port numbers you want to scan> <target IP>

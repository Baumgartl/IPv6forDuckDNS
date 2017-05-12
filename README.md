# IPv6forDuckDNS
Script to submit both IPv6 and IPv4 addresses to DuckDNS.

By default, DuckDNS cannot automatically resolve IPv6 addresses (See [DuckDNS FAQ](https://www.duckdns.org/faqs.jsp) for more details.) Using my script will allow you to easily and automatically submit your IPv4 and IPv6 addresses to DuckDNS.

# Understanding IPv6
While your public IPv4 address is shared across all devices in your network using NAT, each device will have its own public IPv6 address. Therefor, you must run this script on the device that is actually providing the service.

# Prerequisites
* curl, sed, grep, head
* working ipv6 address
* working internet connection w/ dns resolution

# Installation
1. Run ./autoconfig-duckdns6.sh
1. Type your site subdomain
1. Paste your DuckDNS token (watch for trailing whitespace)
1. If applicable, enter an IPv4 service. (Or press ENTER to use default.)
1. The curl request should return OK when Connecting to Duck DNS.
   1.  "K0" is an official error code from DuckDNS - check your subdomain and token
   1. If you get any other output, something is broken. *See prerequisites.*
1. The script will automatically save your configuration and create a cron job.

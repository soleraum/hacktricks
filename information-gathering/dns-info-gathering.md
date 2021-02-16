---
description: DNS
---

# DNS Info Gathering

Whois lookup:

```text
whois <domain>
```

nslookup for finding nameserver:

```text
nslookup google.com
nslookup -type=any google.com
```

host to convert IP to domain name or vice versa:

```text
host google.com
host 74.125.133.139
```

Zone transfers:

```text
# first find name server:
host -t ns google.com
# then request zone transfer: (try on zonetransfer.me to see actual results)
host -t axfr -l google.com ns1.google.com
```

dig for getting mail exchange or anything \(-t any\), even zone transfers

```text
dig -t mx google.com
dig -t any google.com
dig axfr @nsztm1.digi.ninja zonetransfer.me
```

fierce for aggressive non-contiguous ip ranges and wordlist utilization

```text
fierce -dns google.com --wordlist [path to wordlist]
```

dnsenum and dnsrecon 

```text
dnsenum [domainname]
dnsrecon -d google.com
```

Sublist3r - uses publicly available sources to enum subdomains

```text
apt update && apt -y install sublist3r
# default scan
sublist3r -d google.com
# brute forece
sublist3r -d google.com -b -t 100
```


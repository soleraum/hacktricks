# Host/Service Discovery

nmap

```text
# ping scan
nmap -sn 10.11.1.0/24

# TCP connect
nmap -sT 10.11.1.16
# TCP SYN
nmap -sS 10.11.1.16
# UDP
nmap -sU 10.11.1.16

# service and OS detection
nmap -sV -O 10.11.1.16
# service version, OS, script scanning and tracerout
nmap -A 10.11.1.16

# port options
# all ports
-p-
# ports by service name
-p netbios*,microsoft-ds
# top ports
--top-ports 2000
# specify UDP and TCP 
-p U:137-139,T:137-139,445

```

nmape NSE scripts

```text
nmap --script-help ftp-anon

nmap --script snmp-sysdescr --script-args creds.snmp=admin [target host]

HTTP: ls -l /usr/share/nmap/scripts/http*
SMTP: ls -l /usr/share/nmap/scripts/smtp*
SMB: ls -l /usr/share/nmap/scripts/smb*
MySQL: ls -l /usr/share/nmap/scripts/mysql*
WordPress: ls -l /usr/share/nmap/scripts/http-wordpress*
Drupal: ls -l /usr/share/nmap/scripts/http-drupal*
Citrix: ls -l /usr/share/nmap/scripts/citrix*
```

netdiscover

```text
netdiscover -r 10.11.1.0/24
```

SNMP:

```text
onesixtyone
snmpwalk -c public -v1 [target host]
snmpwalk -c public -v1 [target host] [OID]
```


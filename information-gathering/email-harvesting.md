# Email Harvesting

The Harvester

```text
# find emails in cisco.com using yahoo search engine
theHarvester -d cisco.com -b yahoo -l 100
```

recon-ng

```text
recon-ng
marketplace refresh
marketplace search
# search through Have I Been Pwned with this module
marketplace search hibp
marketplace install recon/contacts-credentials/hibp_breach
# need an API key ($3.50/mo) from 
# https://www.troyhunt.com/authentication-and-the-have-i-been-pwned-api/
keys add hibp_api [API key]
modules load recon/contacts-credentials/hibp_breach
options set SOURCE info@microsoft.com
run
# to show creds found in database:
show credentials
```

\(also see "recon/domainshosts/hackertarget" module for HackerTarget.com API to find hostnames\)




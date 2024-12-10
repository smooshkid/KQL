

```
// DNS filtering suggestions. This takes into account wildcard usage and limitations from https://learn.microsoft.com/en-us/azure/sentinel/connect-dns-ama#use-wildcards
// If you choose to exclude collection on a domain, you should be able to use the "exclusion_domain" field verbatim and follow the instructions https://learn.microsoft.com/en-us/azure/sentinel/connect-dns-ama#dont-collect-events-with-specific-domains
ASimDnsActivityLogs // identifying all subdomains and calculating the usage
| extend domain_parts = split(DnsQuery, ".")
| where array_length(domain_parts)>2
| extend exclusion_domain = strcat("*.",strcat_array(array_slice(domain_parts, - 2, -1), "."))
| summarize GB=sum(_BilledSize)/1000/1000/1000, subdomains_that_would_be_excluded=make_set(DnsQuery) by exclusion_domain
| union (ASimDnsActivityLogs // identifying all domains and calculating usage, then unioning with the top query
| extend domain_parts = split(DnsQuery, ".")
| where array_length(domain_parts)==2
| extend exclusion_domain = DnsQuery
| summarize GB=sum(_BilledSize)/1000/1000/1000 by exclusion_domain)
| top 100 by GB // limiting to the top 100 exclusion_domain recommendations by size
| project-reorder exclusion_domain, GB
```

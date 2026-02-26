
# silentpush

Silent Push integration.

In case of any queries, please reach out to support@silentpush.com

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|Silent Push API Key|True|Password|*****|
|Silent Push Server|SilentPush Server URL|True|String|silentpush.com|
|Verify SSL|If true, the SSL certificate of the Silent Push server will be verified.|False|Boolean|true|


#### Dependencies
| |
|-|
|requests-2.32.5-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.1.4-py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|


## Actions
#### Add Feed
This command add the new feed
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Name|Name of the feed.|True|String|test|
|Type|Feed Type.|True|String|test|
|Category|Feed Category.|False|String||
|Vendor|Vendor|False|String||
|Feed Description|URL for the screenshot.|False|String||
|Tags|Tags that should be attached with the feed.|False|String||



#### Add Feed Tags
This command add indicators to the feed
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Feed UUID|Never return query metadata, even if original request did include metadata.|False|String||
|Tags|Comma separated tags to be updated to the feed.|False|String||



#### Add Indicators
This command add indicators to the feed
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Feed UUID|UUID of the feed.|False|String|f8f4b201-801c-4355-a5fa-33fd5abc84c9|
|Indicators|Indicators for the feed.|False|String|qa.com|



#### Add Indicators Tags
This command add indicators to the feed
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Feed UUID|UUID of the feed.|True|String|9a418346-1824-414b-8cb6-82169a529334|
|Indicator Name|The name of the indicator to tag.|True|String|qa.com|
|Tags|Tags to be added to the indicator|True|String|qa|



#### Density Lookup
This action queries granular DNS/IP parameters (e.g., NS servers, MX servers, IPaddresses, ASNs) for density information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Qtype|Query Type|True|String|nssrv|
|Query|Value to query.|True|String|vida.ns.cloudflare.com|
|Scope|Match level|False|String||



#### Forward Padns Lookup
This action performs a forward PADNS lookup using various filtering parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Qtype|DNS record type.|False|String|ns|
|Qname|The DNS record name to lookup.|True|String|silentpush.com|
|Netmask|The netmask to filter the lookup results.|False|String||
|subdomain|Flag to include subdomains in the lookup results.|False|String||
|Regex|Regular expression to filter the DNS records.|False|String||
|Match|Type of match for the query (e.g., exact, partial).|False|String||
|First Seen After|Filter results to include only records first seen after this date.|False|String||
|First Seen Before|Filter results to include only records first seen before this date.|False|String||
|Last Seen After|Filter results to include only records last seen after this date.|False|String||
|Last Seen Before|Filter results to include only records last seen before this date.|False|String||
|As Of|Date or time to get the DNS records as of a specific point in time.|False|String||
|Sort|Sort the results by the specified field (e.g., date, score).|False|String||
|Output Format|The format in which the results should be returned (e.g., JSON, XML).|False|String||
|Prefer|Preference for specific DNS servers or sources.|False|String||
|With Metadata|Flag to include metadata in the DNS records.|False|String||
|Max Wait|Maximum number of seconds to wait for results before timing out.|False|String||
|Skip|Number of results to skip for pagination purposes.|False|String||
|Limit|Maximum number of results to return.|False|String||



#### Get ASN Reputation
This action retrieve the reputation information for an IPv4.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ASN|The ASN to lookup.|True|String|12345|
|Explain|Show the information used to calculate the reputation score.|False|Boolean|false|
|Limit|The maximum number of reputation history records to retrieve.|False|String||



#### Get ASN Takedown Reputation
This action retrieve the takedown reputation information for an Autonomous System Number (ASN).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|ASN|The ASN to lookup.|True|String|211298|
|Explain|Show the information used to calculate the reputation score.|False|Boolean|true|
|Limit|The maximum number of reputation history records to retrieve.|False|String||



#### Get ASNs for Domain
This action retrieves Autonomous System Numbers (ASNs) associated with a domain.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Domain|Domain name to search ASNs for. Retrieves ASNs associated with a records for the specified domain and its subdomains in the last 30 days.|True|String|silentpush.com|



#### Get Data Exports
This command runs the threat check on the specified
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Feed URL|The URL from which to export the feed data.|True|String|9b38bd50-ea46-4280-8739-9b71fc3a9291_indicators.csv|



#### Get Domain Certificates
This action get certificate data collected from domain scanning.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Certificate Issuer|Filter by certificate issuer.|False|String||
|Domain|The domain to query certificates for.|True|String|silentpush.com|
|Domain Regex|Regular expression to match domains.|False|String||
|Date Min|Filter certificates issued on or after this date.|False|String||
|Date Max|Filter certificates issued on or before this date.|False|String||
|Prefer|Prefer to wait for results for longer running queries or to return job_id immediately (Defaults to Silent Push API behaviour).|False|String||
|Max Wait|Number of seconds to wait for results before returning a job_id, with a range from 0 to 25 seconds.|False|String||
|With Metadata|Includes a metadata object in the response, containing returned results, total results, and job_id.|False|String||
|Skip|Number of results to skip.|False|String||
|Limit|Number of results to return.|False|String||



#### Get Enrichment Data
This action retrieves comprehensive enrichment information for a given resource (domain, IPv4, or IPv6).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Resource|Type of resource for which information needs to be retrieved {e.g. domain}.|True|String|ipv4|
|Value|Value corresponding to the selected "resource" for which information needs to be retrieved{e.g. silentpush.com}.|True|String|142.251.188.102|
|Explain|Include explanation of data calculations.|False|Boolean|false|
|Scan Data|Include scan data (IPv4 only).|False|Boolean|false|



#### Get Future Attack Indicatiors
This command fetch indicators of potential future attacks using a feed UUID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Feed UUID|Unique ID for the feed.|True|String|99da9b6a-146b-4a4d-9929-5fd5c6e2c257|
|Page No|The page number to fetch results from.|False|String|1|
|Page Size|The number of indicators to fetch per page.|False|String|10000|



#### Get IPV4 Reputation
This action retrieve the reputation information for an IPv4.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Nameserver|IPv4 address for which information needs to be retrieved.|True|String|a.dns-servers.net.ru|
|Explain|Show the information used to calculate the reputation score|False|Boolean|false|
|Limit|The maximum number of reputation history to retrieve.|False|String||



#### Get job status
This action retrieves the status of a running job or results from a completed job.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|ID of the job returned by Silent Push actions.|True|String|d4067541-eafb-424c-98d3-de12d7a91331|
|Max Wait|Number of seconds to wait for results (0-25 seconds).|False|String||
|Status Only|Return job status, even if job is complete.|False|Boolean|false|
|Force Metadata On|Always return query metadata, even if original request did not include metadata.|False|Boolean|false|
|Force Metadata Off|Never return query metadata, even if original request did include metadata.|False|Boolean|false|



#### Get Nameserver Reputation
This action retrieves historical reputation data for a specified nameserver, including reputation scores and optional detailed calculation information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Nameserver|Nameserver name for which information needs to be retrieved.|True|String|a.dns-servers.net.ru|
|Explain|Show the information used to calculate the reputation score.|False|String||
|Limit|The maximum number of reputation history to retrieve.|False|String||



#### Get Subnet Reputation
This action will retrieve the reputation history for a specific subnet.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subnet|IPv4 subnet for which reputation information needs to be retrieved.|True|String|192.168.0.0/16|
|Explain|Show the detailed information used to calculate the reputation score.|False|String||
|Limit|Maximum number of reputation history entries to retrieve.|False|String||



#### List Domain Information
This action get domain information along with Silent Push risk score and live whois information for multiple domains.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Domains|Comma-separated list of domains to query.|True|String|silentpush.com|
|Fetch Risk Score|Whether to fetch risk scores for the domains.|False|Boolean|false|
|Fetch Whois Info|Whether to fetch WHOIS information for the domains.	|False|Boolean|false|



#### List Domain Infratags
This action get infratags for multiple domains with optional clustering.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mode|Mode for lookup (live/padns). Defaults to "live". Default is live.|False|String||
|Match|Handling of self-hosted infrastructure. Defaults to "self". Default is self.|False|String||
|As Of|Build infratags from padns data where the as_of timestamp equivalent is between the first_seen and the last_seen timestamp.|False|String||
|Use Get|use|False|Boolean|true|
|Origin UID|origin_uid|False|String||
|Domain|Comma-separated list of domains.|True|String|silentpush.com|
|Cluster|Whether to cluster the results.|False|Boolean|false|



#### List IP Information
This action get IP information for multiple IPv4s and IPv6s
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Ips|Comma-separated list of IP addresses.|True|String|142.251.188.102|



#### Live URL Scan
This command scan a URL to retrieve hosting metadata.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URL|URL to scan.|True|String|https://silentpush.com|
|Platform|Platform to scan the URL on.|False|String||
|Os|Operating system to scan the URL on.|False|String||
|Browser|Browser to scan the URL on.|False|String||
|Region|Region to scan the URL in|False|String||



#### Ping

Timeout - 600 Seconds



#### Screenshot URL
This commandGenerate screenshot of a URL.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URL| URL for the screenshot.|True|String|https://www.virustotal.com/gui/domain/tbibank-bg.com|



#### search domains
This command searches for domains with optional filters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Domain|Name or wildcard pattern of domain names to search for.|False|String||
|Domain Regex|A valid RE2 regex pattern to match domains. Overrides the domain argument.|False|String||
|Name Server|Name server name or wildcard pattern of the name server used by domains.|False|String||
|Asnum|Autonomous System (AS) number to filter domains.|False|String||
|Asname|Search for all AS numbers where the AS Name begins with the specified value.|False|String||
|Min IP Diversity|Minimum IP diversity limit to filter domains.|False|String||
|Registrar|Name or partial name of the registrar used to register domains.|False|String||
|Min ASN Diversity|Minimum ASN diversity limit to filter domains.|False|String||
|Certificate Issuer|Filter domains that had SSL certificates issued by the specified certificate issuer. Wildcards supported.|False|String||
|Whois Date After|Filter domains with a WHOIS creation date after this date (YYYY-MM-DD).|False|String||
|Skip|Number of results to skip in the search query.|False|String||
|Limit|Number of results to return. Defaults to the SilentPush API's behavior.|False|String||



#### Search Scan Data
This command search Silent Push scan data repositories using SPQL queries.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|SPQL query string.|True|String|tld=cool|
|Fields|Fields to return in the response.|False|String||
|sort|Sorting criteria for results.|False|String||
|Skip|Number of records to skip in the response.|False|String||
|Limit|Maximum number of results to return.|False|String||
|With Metadat|Whether to include metadata in the response.|False|Boolean|true|



#### Reverse Padns Lookup
This action performs a reverse Passive DNS data for specific DNS record types.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Qtype|DNS record type.|False|String|ns|
|Qname|The DNS record name to lookup.|True|String|vida.ns.cloudflare.com|
|Netmask|The netmask to filter the lookup results.|False|String||
|subdomain|Flag to include subdomains in the lookup results.|False|String||
|Regex|Regular expression to filter the DNS records.|False|String||
|Match|Type of match for the query (e.g., exact, partial).|False|String||
|First Seen After|Filter results to include only records first seen after this date.|False|String||
|First Seen Before|Filter results to include only records first seen before this date.|False|String||
|Last Seen After|Filter results to include only records last seen after this date.|False|String||
|Last Seen Before|Filter results to include only records last seen before this date.|False|String||
|As Of|Date or time to get the DNS records as of a specific point in time.|False|String||
|Sort|Sort the results by the specified field (e.g., date, score).|False|String||
|Output Format|The format in which the results should be returned (e.g., JSON, XML).|False|String||
|Prefer|Preference for specific DNS servers or sources.|False|String||
|With Metadata|Flag to include metadata in the DNS records.|False|String||
|Max Wait|Maximum number of seconds to wait for results before timing out.|False|String||
|Skip|Number of results to skip for pagination purposes.|False|String||
|Limit|Maximum number of results to return.|False|String||



#### Run Threat check
This command runs the threat check on the specified
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Data|The name of the data source to query.|True|String|iofa|
|Query|The value to check for threats (e.g., IP or domain).|True|String|34.8.151.113|
|Type|The type of the value being queried (e.g., ip, domain).|True|String|ip|
|User Identifier|A unique identifier for the user making the request.|True|String|met77e3bb01b4c6483f0525f8c592e3f|










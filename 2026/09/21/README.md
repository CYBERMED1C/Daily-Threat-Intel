# Daily Threat Intelligence — 2026-09-21

**Run time:** 2026-09-21T13:00:00.180532Z

**CTI collection interval:** 2026-09-20T13:00:00.081404Z -> 2026-09-21T13:00:00.180532Z

**Normal target interval:** approximately 24 hours  
**Telemetry hunt window:** 30 days

## Executive summary

Selected 100 of 124 candidate indicators after high-confidence filtering.
Source reports considered: 36; stale reports rejected: 9456.
Sources represented: 1; selected reports: 1; candidate records rejected or removed: 23.
Source health: warning (6 recorded failure(s)); details are in [the intelligence report](threat-intel.md).
Source health and collection warnings are recorded in [the detailed intelligence report](threat-intel.md).
Published 100 high-confidence IOC(s). 100 new.

## Significant threats

### Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework

- Malware: Not established by the source
- Threat actor: Not established by the source
- Why selected: source reliability 22/25; independent corroboration 0/10 from 1 organization(s); freshness 20/20; explicit IOC labeling 20/20; technical malicious context 10/10; active campaign evidence 0/10; specificity 9/10
- Active exploitation: not confirmed
- Source: [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework)
- Accepted IOCs: 100


## Indicators of compromise — highest priority

Counts by type: domain=73, ipv4=25, sha1=2.

| IOC | Type | Confidence | Priority | First seen | Last seen | Threat | Sources | MITRE ATT&CK |
|---|---|---:|---|---|---|---|---|---|
| `b6bc9e1d0b2fb96ab7c47e04cb0be477410bc1f2` | sha1 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `caf2c54e400437da717cf215181b170f65187abf` | sha1 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `135.181.127.216` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `151.240.151.8` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `151.243.113.21` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `193.41.68.196` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `2.27.5.165` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `31.76.31.28` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `31.77.228.46` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `65.21.18.60` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `65.21.208.199` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `85.239.144.195` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `85.239.149.13` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `85.239.149.14` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `85.239.149.167` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `87.58.199.76` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `89.34.90.150` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `89.34.90.159` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `89.34.90.217` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |
| `91.92.33.156` | ipv4 | 74 | High | Not stated | Not stated | Exvicy: A Copycat of the ErrTraffic Malware Distribution Framework | [Sekoia.io](https://www.sekoia.com/blog/exvicy-a-copycat-of-the-errtraffic-malware-distribution-framework) | Not asserted |

## Filtering transparency

- Format validation rejected: 7
- Non-primary type rejected: 0
- Source contamination rejected: 6
- Benign/shared infrastructure rejected: 0
- Low-confidence rejected: 4
- Duplicates removed: 0
- Temporally ineligible indicators: 0
- Previously published suppressed: 1
- Reactivated historical indicators: 0
- 100-IOC safety ceiling rejected: 6

## Hunt and data files

- [IOC CSV](iocs.csv)
- [IOC JSON](iocs.json)
- [Microsoft Defender XDR Advanced Hunting KQL](mde-hunt.kql)
- [Elastic ES|QL](elastic-hunt.esql)
- [Sources](sources.md)
- [Detailed threat intelligence](threat-intel.md)

## Recommended analyst follow-up

1. Run the IOC summary query first and prioritize indicators observed on multiple endpoints.
2. Validate each hit against surrounding process, network, file, identity, and alert telemetry.
3. Confirm campaign timing and ownership before containment or blocking.
4. Scope related devices, accounts, persistence, lateral movement, and data-access activity.
5. Preserve evidence and follow the organization's incident-response process for confirmed activity.

## Analyst caution

An IOC match is an investigative lead, not an automatic malicious verdict. Review source context and enterprise telemetry before taking action.

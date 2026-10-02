# CYBERMEDIC Daily Threat Intelligence

Daily, analyst-ready indicators of compromise and lightweight threat-hunting queries for Microsoft Defender XDR and Elastic Security.

This repository is the publication archive for the CYBERMEDIC daily threat-intelligence workflow. Each dated directory contains a curated set of current, explicitly malicious indicators with source provenance, threat context, confidence, and simple queries an analyst can use for an initial enterprise hunt.

> Defensive use only. Validate findings in the context of your environment before blocking, isolating, or escalating.

## Start here

Browse the [`YYYY/MM/DD`](./2026/) directories and open the Markdown report for the date you want to review. Every completed daily publication contains exactly five files:

| File | Purpose |
|---|---|
| `MM-DD-YY-iocs.md` | Human-readable daily report with safely defanged IOC values and trusted source references |
| `MM-DD-YY-iocs.csv` | Flat IOC dataset for analyst workflows, enrichment, and controlled ingestion |
| `MM-DD-YY-iocs.json` | Structured IOC records with provenance and threat context |
| `mde-hunt.kql` | One copy-and-run Microsoft Defender XDR Advanced Hunting query |
| `elastic-hunt.esql` | One copy-and-run Elastic ES\|QL query |

Repository layout:

```text
YYYY/
  MM/
    DD/
      MM-DD-YY-iocs.csv
      MM-DD-YY-iocs.json
      MM-DD-YY-iocs.md
      mde-hunt.kql
      elastic-hunt.esql
```

The hunt files always live inside their matching date directory. They are never intentionally published at the repository root, year level, or month level.

## What is collected

The workflow supports:

- IPv4 and IPv6 addresses
- domains and fully qualified domain names
- malicious HTTP(S) URLs
- MD5, SHA1, and SHA256 file hashes

An IOC is accepted only when a current public source explicitly identifies it as malicious and provides useful operational context. Candidate values are normalized, structurally validated, checked for unsafe or non-public values, filtered for common false positives, and compared with durable publication history.

Previously published indicators are normally suppressed. A historical indicator may return only when current evidence establishes renewed malicious activity; those records are labeled `REACTIVATED` rather than being presented as newly discovered.

## Research standard

The daily process reviews approximately the previous 48 hours and uses a balanced source strategy:

1. Original threat-research reports and public IOC appendices
2. Government and national CERT/CSIRT advisories
3. Current, metadata-rich public IOC projects
4. Established security news publications for discovery

Every completed research handoff must include at least 20 current source records from at least eight independent organizations. Coverage must include primary research, government/CERT reporting, multiple structured IOC providers, and independent news discovery.

Sources such as BleepingComputer and The Hacker News are used to discover current campaigns. They are not treated as direct IOC evidence: useful leads must be followed to the original technical report, advisory, IOC appendix, or individual structured record before an indicator can be accepted.

If an initial pass produces fewer than five candidates, the workflow performs a documented second pass across additional IOC-rich sources. This increases research coverage without lowering the acceptance standard. There is no IOC quota, and a fully researched day may legitimately publish zero new indicators.

## Hunting queries

The included hunts are intentionally small and direct for use in large enterprise environments.

### Microsoft Defender XDR

The KQL query uses supported Advanced Hunting fields:

- `DeviceNetworkEvents.RemoteUrl` for domain pivots
- `DeviceNetworkEvents.RemoteIP` for IP pivots
- `DeviceFileEvents.MD5`, `SHA1`, and `SHA256` for file hashes

The query applies the time filter first, immediately filters on the daily IOC values, projects basic investigation context, and returns at most 500 newest results. It avoids joins, aggregation, regular expressions, URL parsing, full-text searches, and broad wildcard tables.

### Elastic Security

The ES\|QL query follows the same approach: filter time first, exact-match the IOC fields, keep basic endpoint context, sort newest first, and limit the result to 500 records.

The queries are hunt starters, not detections or automatic blocking rules. A match requires analyst validation.

## Safe handling

The Markdown report defangs every IOC so that an analyst cannot accidentally navigate to malicious infrastructure while reviewing the report:

- domains and IPv4 addresses use `[.]`
- IPv6 addresses use `[:]`
- URLs use `hxxp://` or `hxxps://` and defanged dots

Trusted intelligence-source links remain clickable for provenance.

The CSV, JSON, KQL, and ES\|QL files preserve operational IOC values because machines and hunting engines require the original form. Treat those files as security data: review them in a text editor or security platform, and do not browse to, resolve, ping, scan, or otherwise contact listed infrastructure.

## Suggested analyst workflow

1. Read the dated Markdown summary and source context.
2. Review confidence, campaign attribution, malware family, and publication status.
3. Run the dated KQL or ES\|QL query in the appropriate hunting portal.
4. Validate matches using device, process, user, network, and timeline context.
5. Enrich confirmed matches with your approved internal and external tools.
6. Escalate or contain according to your organization's incident-response procedures.

Do not automatically block every published value. Public infrastructure can change ownership, shared services can create contextual risk, and threat intelligence naturally ages.

## Publication integrity

Before publication, every daily bundle is checked for:

- malformed or unsupported IOC values
- non-public and obvious reference indicators
- duplicate and previously published indicators
- accidental secrets, credentials, and sensitive configuration
- personally identifiable information
- Markdown IOC defanging
- KQL and ES\|QL structure and efficiency
- exact five-file directory placement

Publication targets only [`CYBERMED1C/Daily-Threat-Intel`](https://github.com/CYBERMED1C/Daily-Threat-Intel) on `main`. The workflow verifies the remote repository, branch, commit, paths, and exact file contents before advancing publication history.

## Scope and limitations

- This is curated public-source intelligence, not a complete view of malicious infrastructure.
- Absence of an IOC does not mean an environment is safe.
- IOC matches are leads and can require substantial investigation.
- Confidence reflects the available source evidence, not certainty that every environment will observe malicious behavior.
- No malware is downloaded or executed, and the workflow does not actively probe IOC infrastructure.
- The repository does not use private customer telemetry or publish credentials, internal addresses, or proprietary intelligence.

## About CYBERMEDIC

CYBERMEDIC publishes practical defensive intelligence designed to reduce the time between public threat reporting and an analyst’s first hunt.

Questions and corrections can be submitted through this repository's [GitHub Issues](https://github.com/CYBERMED1C/Daily-Threat-Intel/issues).

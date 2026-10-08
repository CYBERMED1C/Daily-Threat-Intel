<!-- CYBERMEDIC-LIVE-STATUS:START -->
## Live status

🟢 **Operational**

**Last push:** 2026-10-08 13:11 UTC

**Overall health:** Healthy
<!-- CYBERMEDIC-LIVE-STATUS:END -->

# CYBERMEDIC Daily Threat Intelligence

Daily indicators of compromise (IOCs) and simple threat-hunting queries for Microsoft Defender XDR and Elastic Security.

This repository helps security analysts quickly review new public threat intelligence and search for related activity in their environment.

> Defensive use only. Always investigate a match before blocking or containing anything.

## Find the daily reports

Reports are organized by date:

```text
YYYY / MM / DD
```

Example: `2026/10/01/`

[Browse the daily intelligence folders](./2026/)

## What is included each day

Every completed daily folder contains five files:

| File | What it is for |
|---|---|
| `MM-DD-YY-iocs.md` | Easy-to-read daily threat summary |
| `MM-DD-YY-iocs.csv` | IOC list for spreadsheets and security tools |
| `MM-DD-YY-iocs.json` | Structured IOC data with source details |
| `mde-hunt.kql` | Microsoft Defender XDR hunting query |
| `elastic-hunt.esql` | Elastic Security hunting query |

The IOC list may include malicious IP addresses, domains, URLs, and file hashes.

## How to use it

1. Open the dated Markdown report to understand the threats and sources.
2. Run the KQL or ES|QL file in your hunting platform.
3. Review any matches using your normal investigation process.

The hunting queries are intentionally simple and return a maximum of 500 recent results.

## Safety

IOC values in the Markdown report are defanged so they cannot be accidentally clicked.

The CSV, JSON, KQL, and ES|QL files contain the original IOC values needed for hunting. Do not browse to, ping, scan, or otherwise contact listed infrastructure.

## Quality standards

IOCs are collected from current public cybersecurity research, government advisories, and reputable public intelligence sources. Values are validated, checked for false positives, and compared with previously published intelligence.

There is no daily IOC quota. Some days may contain only a few indicators—or none—when there is not enough reliable new intelligence.

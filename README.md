# Web Reconnaissance and Attack Surface Analysis

**Project type:** CEH v12 practical coursework
**Environment:** Kali Linux 2026.1
**Status:** Educational assessment completed

## Overview

This project documents a web reconnaissance exercise using Nmap, WhatWeb, Gobuster, and cURL. The objective was to examine the externally observable attack surface, identify exposed services and web technologies, inspect HTTP behavior, and document security-relevant observations.

The assessment focused on reconnaissance and documentation. Exploitation and authenticated testing are not claimed.

## Objectives

* Identify reachable services and exposed TCP ports.
* Fingerprint publicly observable web-server technologies.
* Examine reported HTTP methods.
* Inspect HTTP response headers and server information disclosure.
* Attempt directory enumeration and document its limitations.
* Translate observations into defensive recommendations.

## Lab Environment

| Component                     | Details                    |
| ----------------------------- | -------------------------- |
| Operating system              | Kali Linux 2026.1          |
| Port and service discovery    | Nmap                       |
| Web technology fingerprinting | WhatWeb                    |
| Directory enumeration         | Gobuster                   |
| HTTP response inspection      | cURL                       |
| Assessment type               | Educational reconnaissance |

**Scope and disclosure:** This public project version omits target identifiers and raw scan evidence. Testing should be conducted only against systems owned by the tester or explicitly authorized for assessment.

## Methodology

The assessment followed these stages:

1. **Service discovery:** Identified services and ports reported as reachable.
2. **Technology fingerprinting:** Examined web-server and hosting indicators.
3. **HTTP method inspection:** Recorded methods reported by the assessment.
4. **Directory enumeration:** Attempted wordlist-based discovery and assessed the reliability of the responses.
5. **Header inspection:** Reviewed HTTP response headers and observable security-related indicators.
6. **Reporting:** Documented observations, limitations, and defensive recommendations.

See [Methodology and Command Reference](docs/methodology.md) for example commands and the reporting checklist.

## Selected Observations

The original coursework report recorded the following observations:

* FTP, HTTP, HTTPS, and MySQL ports were reported as reachable.
* LiteSpeed and hosting-platform indicators appeared in HTTP responses.
* `GET`, `HEAD`, `POST`, and `OPTIONS` were reported as supported HTTP methods.
* Directory enumeration returned consistent `403 Forbidden` responses, preventing reliable differentiation between existing and nonexistent paths.
* HTTPS redirection and a Content Security Policy (CSP) indicator were observed.

These observations describe the assessment at the time it was performed. They do not establish the target's current configuration or prove that any service is exploitable. Port reachability and the presence of an HTTP method do not, by themselves, establish a vulnerability.

See [Findings Summary](docs/findings-summary.md) for interpretations and defensive actions.

## Defensive Recommendations

Based on the observations and limitations documented in the coursework:

* Verify the business need for externally reachable services and restrict access where appropriate.
* Minimize unnecessary server-version and banner disclosure.
* Enforce HTTPS and review security-header and TLS configurations.
* Treat directory enumeration as inconclusive when responses do not distinguish existing from nonexistent paths.
* Repeat assessments periodically and compare results over time.

These are general defensive recommendations; they are not claims that every listed weakness was confirmed.

## Limitations

* The work documents reconnaissance, not exploitation or authenticated testing.
* Directory enumeration was inconclusive because responses were consistently `403 Forbidden`.
* The findings reflect a historical, point-in-time educational assessment.
* The public repository omits the target domain, IP address, raw scan output, and screenshots.
* No claim is made that the target has been independently retested or that its current security posture is known.

## Skills Demonstrated

* Network and service reconnaissance
* Web technology fingerprinting
* HTTP methods and response-header inspection
* Directory-enumeration methodology
* Interpretation of inconclusive results
* Technical documentation
* Defensive security recommendations

## Project Documentation

* [Methodology and Command Reference](docs/methodology.md)
* [Findings Summary](docs/findings-summary.md)
* [Evidence and Disclosure Notes](evidence/README.md)

## Ethical Use

Use reconnaissance tools only on systems you own or have explicit permission to assess. Do not publish sensitive target information, credentials, personal data, or scan evidence without appropriate authorization.

# Web Reconnaissance Assessment

> CEH v12 practical project | Educational security assessment

## Overview
A structured web-reconnaissance exercise using **Nmap, WhatWeb, Gobuster, and cURL** from Kali Linux. The goal was to map the externally visible attack surface and document observations without attempting exploitation.

## Objectives
- Identify reachable services and exposed TCP ports.
- Fingerprint publicly visible web-server technologies.
- Enumerate supported HTTP methods.
- Review HTTP response headers and exposed application information.
- Attempt directory discovery and document limitations.
- Turn observations into defensive recommendations.

## Environment
- Platform: Kali Linux 2026.1
- Tools: Nmap, WhatWeb, Gobuster, cURL
- Scope: Authorized educational assessment. Target identifiers and raw evidence are intentionally omitted from this public version.

## Methodology
1. Discover reachable services and ports.
2. Fingerprint server technologies.
3. Enumerate reported HTTP methods.
4. Attempt wordlist-based directory discovery.
5. Review HTTP response headers.
6. Document observations, limitations, and recommendations.

## Selected observations from the coursework report
- FTP, HTTP, HTTPS, and MySQL ports were reported reachable during the assessment.
- LiteSpeed and hosting-platform information appeared in HTTP responses.
- `GET`, `HEAD`, `POST`, and `OPTIONS` were reported as supported methods.
- Directory enumeration returned consistent HTTP 403 responses, preventing reliable differentiation between existing and non-existing paths.
- HTTPS redirection and a Content Security Policy indicator were observed.

These are point-in-time observations, not proof that a service is currently exposed or exploitable. Port reachability alone does not establish a vulnerability.

## Recommendations considered
- Verify the business need for externally reachable services and restrict access where appropriate.
- Minimize unnecessary server-version disclosure.
- Enforce HTTPS and review security headers.
- Treat directory enumeration as inconclusive when responses are indistinguishable.
- Repeat assessments periodically and compare results.

## Limitations
- Reconnaissance only; exploitation and authenticated testing are not claimed.
- Directory enumeration was inconclusive because of consistent `403 Forbidden` responses.
- Results reflect the assessment date.
- This public version excludes the target domain, IP, raw output, and screenshots. Add them only with explicit disclosure permission.

## Ethics
Test only systems you own or are explicitly authorized to assess.

## Skills demonstrated
Nmap · WhatWeb · Gobuster · cURL · HTTP fundamentals · Attack-surface mapping · Evidence documentation · Security recommendations

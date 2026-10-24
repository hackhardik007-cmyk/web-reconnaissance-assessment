# Methodology and Command Reference

Run commands only against a target you own or are explicitly authorized to assess.

## Port discovery
```bash
nmap <AUTHORIZED_TARGET>
```

## Technology fingerprinting
```bash
whatweb <AUTHORIZED_TARGET>
```

## HTTP-method enumeration
```bash
nmap --script http-methods <AUTHORIZED_TARGET>
```

## Directory enumeration
```bash
gobuster dir -u https://<AUTHORIZED_TARGET>/ -w /usr/share/wordlists/dirb/common.txt
```

## Header review
```bash
curl -I https://<AUTHORIZED_TARGET>/
```

## Reporting checklist
Record date/time, tool version, exact command, output, interpretation, and limitations. Redact credentials, tokens, personal data, internal hostnames, and target identifiers that you are not permitted to disclose. A scanner observation is not automatically a confirmed vulnerability.

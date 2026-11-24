# 🦉 OMailSec

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMailSec** — Email-Domain Authentication Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OMailSec audits email-domain authentication posture across SPF, DKIM, DMARC, MTA-STS, TLS-RPT, DANE/TLSA, and BIMI. It works offline from published or pasted records, or with optional read-only dig/nslookup lookups, and produces a spoofability verdict, grade, remediation, and multi-format reports including SARIF.

---

## ✨ Features

- Offline-first audit of published records (zone file, dig output, key:value, or JSON) plus optional dig/nslookup
- Analysers for SPF (lookup budget), DKIM (DER key size), DMARC, MTA-STS, TLS-RPT, DANE/TLSA, and BIMI
- Spoofability verdict and A+…F grade with recommended hardened records (`--records`)
- Live domain mode (`--domain`) or fully offline `--parse` / per-record flags
- Min-severity, fail-on, and min-grade CI gates
- Export TXT / MD / JSON / CSV / SARIF; `--demo` self-test and rule catalogue

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMailSec -d example.com
./OMailSec --offline --spf "v=spf1 -all" --dmarc "v=DMARC1; p=reject" --json -o mailsec.json
./OMailSec --demo --grade
./OMailSec --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OMailSec --help   # watch every network call
firejail --net=none ./OMailSec --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)

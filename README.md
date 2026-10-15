# 🦉 OMailSec

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMailSec** — Email-Domain Authentication Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Email-domain authentication auditor (SPF / DKIM / DMARC / MTA-STS / TLS-RPT / DANE / BIMI)

---

## ✨ Features

- Offline-first audit of PUBLISHED records (zone, dig, key: value or JSON) + optional read-only dig/nslookup
- SPF (lookup budget), DKIM (DER key size), DMARC, MTA-STS, TLS-RPT, DANE/TLSA and BIMI analysers
- Spoofability verdict, A+…F grade, record generator
- Export TXT / MD / JSON / CSV / SARIF, --demo self-test

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMailSec
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*

# Learn-SecByte-CTF-Labs-Collection-Static-PE-Header-Analysis-Entropy-UPX-Unpacking
A curated collection of hands-on static malware analysis CTF labs covering PE Headers, Section Entropy, Import/Export Tables (IAT/EAT), UPX &amp; Custom Packers, Digital Signatures, and Metadata Forensics from Learn SecByte.
# Learn SecByte CTF & Cybersecurity Labs Collection

Welcome to the **Learn SecByte CTF & Cybersecurity Labs Collection**. This repository is a structured, searchable index of hands-on static malware analysis, Portable Executable (PE) header forensics, packer identification, entropy calculation, and structural binary investigation labs designed for cybersecurity students, CTF players, malware analysts, SOC engineers, and reverse engineers.

---

## Table of Contents
- [Introduction](#introduction)
- [Lab Collection & Index](#lab-collection--index)
- [Categories](#categories)
- [Learning Path](#learning-path)
- [How to Use the Labs](#how-to-use-the-labs)
- [Disclaimer](#disclaimer)

---

## Introduction

Static binary analysis allows security practitioners to extract critical threat intelligence without executing potentially dangerous code. Hosted on [Learn SecByte](https://learn.secbyte.org/), this collection of CTF challenge labs focuses on inspecting Portable Executable structures and identifying obfuscation markers.

From auditing DOS/NT headers, Section Headers, and Import/Export Address Tables (IAT/EAT) to calculating Shannon entropy for detecting packed/encrypted sections, verifying digital signature authenticity, analyzing resource sections, detecting UPX and custom binary packers, and extracting file metadata artifacts, these exercises establish a strong foundation in binary triage.

---

## Lab Collection & Index

Below is the complete, searchable index of all static analysis, PE header, and packer challenges in this collection:

| # | Lab / Challenge Name | Category | Focus / Key Topics | Lab Link |
|---|----------------------|----------|---------------------|----------|
| 1 | **Custom Packers Analysis** | Packer Analysis & Unpacking | Custom compression routines, stub analysis, manual OEP identification | [Access Lab](https://learn.secbyte.org/ctf/custom-packers-analysis) |
| 2 | **UPX Unpacked: Reverse Engineering Packed Binaries** | Packer Analysis & Unpacking | UPX header modifications, section restoration (`UPX0`/`UPX1`), manual decompression | [Access Lab](https://learn.secbyte.org/ctf/upx-unpacked-reverse-engineering-packed-binaries) |
| 3 | **Packer Detection Fundamentals** | Packer Analysis & Unpacking | PEiD, Detect It Easy (DIE), YARA packer signatures, overlay inspection | [Access Lab](https://learn.secbyte.org/ctf/packer-detection-fundamentals) |
| 4 | **Malware Classification Techniques: From Triage to Attribution** | Triage & Attribution | Fuzzy hashing (ssdeep), imphash comparison, section hashing, campaign clustering | [Access Lab](https://learn.secbyte.org/ctf/malware-classification-techniques-from-triage-to-attribution) |
| 5 | **Entropy Analysis: Finding Order in Randomness** | Static Analysis | Shannon entropy calculations, packed/encrypted data detection, visualization | [Access Lab](https://learn.secbyte.org/ctf/entropy-analysis-finding-order-in-randomness) |
| 6 | **Digital Signature Analysis: Trust & Tamper Verification** | Certificate Forensics | Authenticode signature parsing, stolen/invalid certificates, certificate append attacks | [Access Lab](https://learn.secbyte.org/ctf/digital-signature-analysis-trust-tamper-verification) |
| 7 | **Resource Recon: Analysis of Public Assets** | PE Structure Analysis | `.rsrc` section extraction, embedded ICO/BMP files, hidden payload storage, manifest auditing | [Access Lab](https://learn.secbyte.org/ctf/resource-recon-analysis-of-public-assets) |
| 8 | **Export Address Table Sleuthing** | PE Structure Analysis | EAT parsing, exported functions, DLL forwarding, ordinal function identification | [Access Lab](https://learn.secbyte.org/ctf/export-address-table-sleuthing) |
| 9 | **IAT Sleuth: Import Table Analysis** | PE Structure Analysis | Import Address Table (IAT) parsing, delayed loading, suspicious API imports (imphash) | [Access Lab](https://learn.secbyte.org/ctf/iat-sleuth-import-table-analysis) |
| 10 | **Section Analysis: Finding the Weak Link** | PE Structure Analysis | Section permissions (executable/writable), non-standard section names, raw vs. virtual size | [Access Lab](https://learn.secbyte.org/ctf/section-analysis-finding-the-weak-link) |
| 11 | **PE Header Sleuthing** | PE Structure Analysis | DOS Header, e_lfanew pointer, COFF Header, Optional Header, Data Directories | [Access Lab](https://learn.secbyte.org/ctf/pe-header-sleuthing) |
| 12 | **File Metadata Forensics Lab** | Metadata & Artifacts | Compilation timestamps, compiler identification, ExifTool metadata, language IDs | [Access Lab](https://learn.secbyte.org/ctf/file-metadata-forensics-lab) |

---

## Categories

### 1. PE Header & Structural Analysis
Examine lower-level structures of Portable Executables, including headers, section characteristics, imports, exports, and resource sections.
- [PE Header Sleuthing](https://learn.secbyte.org/ctf/pe-header-sleuthing)
- [Section Analysis: Finding the Weak Link](https://learn.secbyte.org/ctf/section-analysis-finding-the-weak-link)
- [IAT Sleuth: Import Table Analysis](https://learn.secbyte.org/ctf/iat-sleuth-import-table-analysis)
- [Export Address Table Sleuthing](https://learn.secbyte.org/ctf/export-address-table-sleuthing)
- [Resource Recon: Analysis of Public Assets](https://learn.secbyte.org/ctf/resource-recon-analysis-of-public-assets)

### 2. Packer Identification & Unpacking
Detect executable packing, reverse-engineer UPX-compressed binaries, and analyze custom packing routines.
- [Packer Detection Fundamentals](https://learn.secbyte.org/ctf/packer-detection-fundamentals)
- [UPX Unpacked: Reverse Engineering Packed Binaries](https://learn.secbyte.org/ctf/upx-unpacked-reverse-engineering-packed-binaries)
- [Custom Packers Analysis](https://learn.secbyte.org/ctf/custom-packers-analysis)

### 3. Entropy, Hashes & Malware Classification
Measure randomness across binary sections, generate fuzzy/import hashes, and classify samples for campaign attribution.
- [Entropy Analysis: Finding Order in Randomness](https://learn.secbyte.org/ctf/entropy-analysis-finding-order-in-randomness)
- [Malware Classification Techniques: From Triage to Attribution](https://learn.secbyte.org/ctf/malware-classification-techniques-from-triage-to-attribution)

### 4. File Metadata & Certificate Forensics
Inspect embedded file metadata, compilation flags, timestamp anomalies, and Authenticode digital signatures.
- [File Metadata Forensics Lab](https://learn.secbyte.org/ctf/file-metadata-forensics-lab)
- [Digital Signature Analysis: Trust & Tamper Verification](https://learn.secbyte.org/ctf/digital-signature-analysis-trust-tamper-verification)

---

## Learning Path

Follow this structured progression path to master static malware triage and PE binary analysis:

1. **Phase 1: Binary Headers & Metadata Inspection** — Learn PE structural components and compiler artifacts:
   - [File Metadata Forensics Lab](https://learn.secbyte.org/ctf/file-metadata-forensics-lab)
   - [PE Header Sleuthing](https://learn.secbyte.org/ctf/pe-header-sleuthing)
   - [Section Analysis: Finding the Weak Link](https://learn.secbyte.org/ctf/section-analysis-finding-the-weak-link)
   - [Digital Signature Analysis: Trust & Tamper Verification](https://learn.secbyte.org/ctf/digital-signature-analysis-trust-tamper-verification)

2. **Phase 2: Imports, Exports & Resources** — Analyze API dependencies, exported functions, and embedded assets:
   - [IAT Sleuth: Import Table Analysis](https://learn.secbyte.org/ctf/iat-sleuth-import-table-analysis)
   - [Export Address Table Sleuthing](https://learn.secbyte.org/ctf/export-address-table-sleuthing)
   - [Resource Recon: Analysis of Public Assets](https://learn.secbyte.org/ctf/resource-recon-analysis-of-public-assets)

3. **Phase 3: Entropy Measurement & Classification** — Detect encrypted/compressed code sections and calculate similarity hashes:
   - [Entropy Analysis: Finding Order in Randomness](https://learn.secbyte.org/ctf/entropy-analysis-finding-order-in-randomness)
   - [Malware Classification Techniques: From Triage to Attribution](https://learn.secbyte.org/ctf/malware-classification-techniques-from-triage-to-attribution)

4. **Phase 4: Packer Detection & Decompression** — Detect packed binaries and unpack UPX/custom loaders:
   - [Packer Detection Fundamentals](https://learn.secbyte.org/ctf/packer-detection-fundamentals)
   - [UPX Unpacked: Reverse Engineering Packed Binaries](https://learn.secbyte.org/ctf/upx-unpacked-reverse-engineering-packed-binaries)
   - [Custom Packers Analysis](https://learn.secbyte.org/ctf/custom-packers-analysis)

---

## How to Use the Labs

1. Select a challenge link from the index or category sections above.
2. Read the scenario directives and target files provided on [Learn SecByte](https://learn.secbyte.org/).
3. Use static inspection tools (e.g., PEStudio, CFF Explorer, Detect It Easy, Ghidra, ssdeep, SignTool) within an isolated analysis VM.
4. Inspect binary headers, calculate entropy scores, parse import/export tables, decompress packed sections, and submit target flags.

---

## Disclaimer

This repository and its linked challenge resources are strictly intended for educational, threat research, and authorized technical training purposes. Never analyze or manipulate malicious executables outside an isolated environment.

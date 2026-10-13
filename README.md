# Audit-file-Integrity-verification
A GRC audit project that uses SHA-256 hashing to verify the integrity of audit evidence, detect unauthorized modifications, and support reliable, tamper-evident compliance documentation.

## Project Overview
This project demonstrates how SHA-256 hashing can be used to verify the integrity of audit evidence. The workflow simulates receiving an employee access review document and its corresponding hash record, calculating the document's hash, and comparing hash values to identify potential changes.

The project also demonstrates how modifying a copy of an audit document changes its SHA-256 hash, highlighting the importance of maintaining the integrity of audit evidence during the audit process.

## Tools and Technologies

- **PowerShell:** Calculated SHA-256 hashes using `Get-FileHash`.
- **Command Prompt (CMD):** Calculated SHA-256 hashes using `certutil`.
- **SHA-256:** Cryptographic hash algorithm used to check file integrity.
- **Microsoft Word:** Created the sample audit evidence and HR hash record.
- **GitHub:** Stored the project files, verification screenshots, and project documentation.

- ## Testing Procedure

1. Created a sample employee access review document as audit evidence.
2. Generated a SHA-256 hash of the original document using PowerShell.
3. Generated the same document's SHA-256 hash using Command Prompt and confirmed that both values matched.
4. Created a copy of the original document and added a test line without changing the original.
5. Generated a SHA-256 hash of the modified copy and compared it with the original hash.

## Results

- **Original document:** PowerShell and Command Prompt produced matching SHA-256 hashes.
- **Modified document:** Its SHA-256 hash differed from the original document's hash.
- **Finding:** The test demonstrated that modifying the document changed its hash, allowing the change to be detected through hash comparison.

## Evidence

Verification screenshots are available in the `verification-screenshots` folder.

## Scope and Limitations

This is a simulated GRC portfolio project using sample audit evidence. A matching hash supports file-integrity verification against a trusted reference hash; it does not prove that the document's contents are accurate or that the reference hash came from an authentic source.

## Project Structure

- `sample-evidence/` — Contains the sample employee access review document and HR SHA-256 hash record.
- `verification-screenshots/` — Contains screenshots documenting the original and modified document hash calculations.
- `README.md` — Explains the project's purpose, testing procedure, results, and limitations.

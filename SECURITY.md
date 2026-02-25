# Security Policy

## Overview

This repository is a community-curated registry of TON blockchain assets including verified addresses, jettons (tokens), and NFT collections. Because the data in this registry is used by wallets and applications to display asset information to end users, the integrity and accuracy of these listings is critical to user safety.

## Scope

Security concerns in this repository fall into two categories:

### 1. Malicious or Fraudulent Asset Listings
- Scam tokens or collections impersonating legitimate projects
- Phishing addresses disguised as known wallets or services
- Listings with misleading names, symbols, or metadata designed to deceive users

### 2. Vulnerabilities in Repository Tooling
- Security issues in the Python scripts (`generator.py`, `parser.py`, `dexes.py`, `utlis.py`)
- Vulnerabilities in GitHub Actions workflows
- Any issue that could allow unauthorized modification of generated `.json` files

## Reporting a Security Issue

**Do not open a public GitHub issue for security vulnerabilities.**

### Reporting a Fraudulent Listing
If you discover a scam, phishing address, or fraudulent token/collection already listed in this registry:

1. Email the Tonkeeper security team at **security@tonkeeper.com**
2. Include the asset address, the relevant file path (e.g. `jettons/$TOKEN.yaml`), and a description of why it is fraudulent
3. If you have evidence (e.g. links to scam reports, on-chain data), please attach it

We aim to respond to listing fraud reports within **48 hours** and remove confirmed fraudulent entries promptly.

### Reporting a Tooling Vulnerability
If you discover a vulnerability in the repository's scripts or workflows:

1. Email **security@tonkeeper.com** with the subject line: `[ton-assets] Security Vulnerability`
2. Provide a clear description of the vulnerability and steps to reproduce
3. If possible, include the potential impact and a suggested fix

We follow responsible disclosure practices and will acknowledge reports within **72 hours**.

## Important Reminder

> **The Tonkeeper team does NOT charge any fees for reviewing, verifying, or listing tokens or collections. This process is completely FREE.**
>
> Ignore any messages in pull request comments or commits claiming that payment is required to expedite or approve a review. These are scams. Stay safe.

## Supported Versions

This repository does not have versioned releases. The `main` branch always reflects the current canonical asset list.

## Pull Request Safety Guidelines

When reviewing or submitting pull requests, be aware of the following risks:

- **Do not submit** addresses that impersonate existing well-known projects
- **Do not use** `ton.api` links for images — only direct image file links with valid extensions (`.jpg`, `.png`, etc.) are accepted
- **Do not modify** auto-generated files (`accounts.json`, `jettons.json`, `collections.json`, `README.md`) — changes should only be made to `.yaml` files in the `accounts/`, `collections/`, or `jettons/` directories
- All pull requests are reviewed by the Tonkeeper team before merging

## Contact

For non-security-related questions, open a GitHub issue or pull request. For security matters, contact **security@tonkeeper.com**.

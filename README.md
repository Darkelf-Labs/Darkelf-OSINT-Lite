# Darkelf OSINT Lite

Darkelf OSINT Lite is a lightweight, terminal-first Open Source Intelligence (OSINT) toolkit inspired by the Darkelf project.

Designed for ethical security research, digital forensics, Capture the Flag (CTF) competitions, and investigative workflows, Darkelf OSINT Lite emphasizes privacy, safer defaults, modular architecture, and a streamlined command-line experience.

The toolkit includes:

* Tor-aware networking
* OSINT search and dorking
* Safe web content retrieval
* Indicator extraction
* WHOIS and DNS lookups
* Local AI-assisted report drafting (optional)
* Structured report exporting

> **Important:** This software is intended solely for lawful and authorized OSINT activities. Users are responsible for complying with all applicable laws and regulations.

---

# Installation

## Install from PyPI (Recommended)

```bash
pip install darkelf-osint-lite
```

Launch the application:

```bash
darkelf-osint-lite
```

---

## Install from Source

Clone the repository:

```bash
git clone https://github.com/Darkelf-Labs/darkelf-osint-lite.git
cd darkelf-osint-lite
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run:

```bash
python main.py
```

---

# Features

* Privacy-focused command-line interface
* Tor-aware networking
* Multi-engine OSINT search
* DuckDuckGo dork helper
* Safe web page retrieval
* Automatic indicator extraction

  * Email addresses
  * Domains
  * IPv4 addresses
  * Usernames
  * Cryptographic hashes
  * Phone numbers
* WHOIS lookups

  * Domain WHOIS
  * IP WHOIS
* DNS lookups

  * A
  * AAAA
  * MX
  * TXT
  * NS
  * CNAME
  * SOA
  * Reverse DNS (PTR)
  * Bulk DNS lookups
* Darkelf Scribe local AI report drafting (optional)
* Offline Progressive Web App (PWA) report viewer
* JSON and Markdown report exports
* Rich terminal interface
* Automatic activity logging

Reports are saved to:

```
~/Documents/Darkelf/
```

---

# Requirements

* Python 3.10 or newer
* Tor (recommended)
* Ollama (optional for Darkelf Scribe)

Install dependencies manually if needed:

```bash
pip install rich requests beautifulsoup4 tldextract phonenumbers dnspython python-whois stem psutil pysocks
```

> **Note:** Install **python-whois**, not the unrelated **whois** package.

---

# Tor Setup

Darkelf OSINT Lite automatically detects Tor if available.

Typical SOCKS ports:

* 9050
* 9052
* 9150

Verify Tor:

```bash
curl --socks5-hostname 127.0.0.1:9052 https://check.torproject.org/api/ip
```

---

# Usage

Launch:

```bash
darkelf-osint-lite
```

The startup banner displays the current status:

```
Stealth: ON · Tor: enabled · DNS: available · WHOIS: available
```

Main capabilities include:

* Scan
* Dork
* Fetch
* Indicators
* WHOIS / DNS
* Darkelf Scribe
* Report Viewer

---

# Darkelf Scribe (Optional)

Darkelf Scribe integrates with Ollama to generate structured OSINT investigation drafts entirely on your local machine.

Supported capabilities include:

* Draft investigation summaries
* Evidence organization
* Markdown export
* JSON export
* Offline PWA report viewing

Install Ollama separately:

https://ollama.com

---

# Security

Darkelf OSINT Lite emphasizes privacy-first defaults.

Features include:

* Tor-aware networking
* Safe subprocess execution
* URL normalization and validation
* Tracker blocking
* Structured logging
* Local AI processing (no cloud dependency)

This Lite edition intentionally excludes destructive or anti-forensic functionality.

---

# Troubleshooting

**Tor unavailable**

* Ensure Tor is running.
* Verify the SOCKS port.
* Install `pysocks`.

**WHOIS errors**

* Install `python-whois`.
* Remove the incorrect `whois` package if installed.

**DNS lookup errors**

* Install `dnspython`.

---

# Contributing

Contributions are welcome.

Please:

* Fork the repository
* Create a feature branch
* Submit a pull request with a clear description

Security improvements, bug fixes, documentation, and usability enhancements are encouraged.

---

# License

Licensed under the **GNU Lesser General Public License v3.0 or later (LGPL-3.0-or-later).**

See the LICENSE file for details.

---

# Author

**Dr. Kevin Moore**

Creator of the Darkelf project and the Darkelf family of privacy-focused security and research tools.

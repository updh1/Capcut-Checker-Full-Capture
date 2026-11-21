# CapCut Account Checker

A fast, multi-threaded CapCut account checker that validates email/password combos and detects active premium (VIP/Pro) subscriptions.

## Features

- Multi-threaded checking (configurable thread count)
- Proxy support (HTTP / HTTP with auth: `host:port:user:pass` or `host:port`)
- Automatic retry logic (up to 3 attempts per account)
- Detects **PREMIUM** (active Pro/VIP subscription), **FREE**, **BAD** (invalid credentials) and **ERROR** statuses
- Live console output — hits are printed in color as they are found
- Saves results to separate files:
  - `premium_hits.txt` — accounts with active premium subscription
  - `free_hits.txt` — valid accounts without a subscription
- Live statistics in the console title (Windows)
- Clean, colorized terminal UI

## Requirements

- Python 3.8+
- Dependencies listed in `requirements.txt`

## Installation

```bash
git clone https://github.com/yourusername/capcut-checker.git
```
```bash
cd capcut-checker
```
```bash
pip install -r requirements.txt
```
## Usage
Prepare a combo file (one account per line):
```bash
email1@example.com:password1
email2@example.com:password2
```
(Optional) Prepare a proxy file (one proxy per line):
```bash
127.0.0.1:8080
127.0.0.1:8080:username:password
```
Run the checker:
```bash
python main.py
```

## Output
```bash
PREMIUM hits are printed in green and saved to premium_hits.txt
FREE hits are printed in yellow and saved to free_hits.txt
Format: email:password | Name: <name> | Plan: <plan> | Exp: <date>
```



## Disclaimer
- This tool is provided for educational and research purposes only. The author is not responsible for any misuse. Use at your own risk. Do not use against accounts you do not own.

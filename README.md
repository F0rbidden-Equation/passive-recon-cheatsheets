# passive-recon-cheatsheets
 Collection of passive information gathering cheat sheets for cybersecurity students. Includes Google Dorks, OSINT tools, crawler techniques, and more. Ideal for beginners and CTF players.

# 🔍 Passive Information Gathering – Cheat Sheet

## 📌 Definition
**Passive information gathering** is the process of collecting data about a target **without directly interacting** with it. Unlike active scans (like Nmap), passive techniques usually leave **no trace** on the target server.

---

## 🔎 Techniques & Tools

### 📂 Google Dorks (useful examples)
```
inurl:admin
filetype:pdf site:example.com
intitle:"index of"
site:example.com inurl:login
```

### 🕷️ Crawlers & Collection Tools
- `wget --mirror https://target.com`
- `httrack https://target.com`
- `wayback_machine_downloader https://target.com`
- `theHarvester -d target.com -b google`
- `Photon` (OSINT crawler with API/JS support)

### 🔍 Specialized Search Engines
- [Shodan](https://www.shodan.io/)
- [Censys](https://search.censys.io/)
- [ZoomEye](https://www.zoomeye.org/)

### 📚 Archives & Cache
- [Wayback Machine](https://web.archive.org/)
- [CachedView](https://cachedview.com/)
- Google Cache: `cache:example.com`

### 🧠 WHOIS & DNS
- `whois example.com`
- `dig example.com any`
- `nslookup -type=any example.com`
- [who.is](https://who.is/)
- [dnsdumpster.com](https://dnsdumpster.com/)

### 📱 Social Media & Data Leak Databases
- [intelx.io](https://intelx.io/)
- [HaveIBeenPwned](https://haveibeenpwned.com/)
- `site:linkedin.com company`
- `site:pastebin.com keyword`

---

## ✅ Best Practices
- Use a VPN or Tor
- Browse in incognito/private mode
- Avoid any direct interaction with the target
- Store your findings in a well-organized report

---

## 🚫 What Passive Recon is NOT:
- Network scanning (e.g., `nmap`, `masscan`)
- Brute-force or fuzzing
- Exploiting vulnerabilities
- Submitting data to forms

---

## ✍️ Author
Created by Amadeus for cybersecurity students 🧠💻  
📁 Ready to publish on [GitHub](https://github.com) and share with the class!

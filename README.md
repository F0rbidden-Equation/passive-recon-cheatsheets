# passive-recon-cheatsheets
 Collection of passive information gathering cheat sheets for cybersecurity students. Includes Google Dorks, OSINT tools, crawler techniques, and more. Ideal for beginners and CTF players.

# 🔍 Passive Information Gathering – Cheat Sheet

## 📌 Definition
**Passive information gathering** is the process of collecting data about a target **without directly interacting** with it. Unlike active scans (like Nmap), passive techniques usually leave **no trace** on the target server.

---

## 🔎 Techniques & Tools

### 📂 Google Dorks (useful examples)
#### 🔐 Admin panels & login pages
```
inurl:admin
inurl:admin/login
inurl:cpanel
inurl:dashboard
intitle:"admin login"
site:example.com inurl:login
```

#### 📁 Exposed directories & file listings
```
intitle:"index of /"
intitle:"index of" site:example.com
intitle:"index of" backup
intitle:"index of" .git
intitle:"index of" db
```

#### 📄 Sensitive file types
```
filetype:env DB_PASSWORD
filetype:log password
filetype:sql "insert into"
filetype:pdf site:example.com
filetype:xls site:example.com
filetype:conf "passwd"
```

#### 🧠 Information disclosure
```
intext:"Welcome to phpMyAdmin"
intitle:"Apache2 Ubuntu Default Page"
inurl:wp-content
inurl:.env
inurl:config
intext:"Index of /" "parent directory"
```

#### 🔑 Password leaks & credentials
```
filetype:txt "password"
filetype:xls "username password email"
"DB_PASSWORD" filetype:env
"ftp" "upload file" site:example.com
"login" "password" site:pastebin.com
```

#### 💬 Emails and user info
```
intext:@example.com
intext:"your password is"
"email *.*.*.*.*" filetype:xls
```

#### 🎯 Targeted reconnaissance
```
site:example.com filetype:pdf
site:example.com inurl:admin
site:example.com intext:"confidential"
site:example.com intitle:"index of"
```

#### ⚙️ Devices and camera interfaces
```
inurl:"/view/view.shtml"
inurl:"/video.cgi"
intitle:"Live View / - AXIS"
inurl:"webcamXP"
```


---

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

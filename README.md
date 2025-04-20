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



#### 🔓 Login portals & control panels
```
inurl:login.asp
inurl:signin
inurl:auth
inurl:adminpanel
inurl:backend
inurl:secure
intitle:"Admin Console"
```

#### 🔎 Backup files & config leaks
```
filetype:bak
filetype:old
filetype:backup
filetype:cfg
filetype:ini
filetype:db site:example.com
inurl:backup
inurl:wp-content/uploads/backup
```

#### 💾 Database dumps
```
filetype:sql
filetype:db
filetype:mdb
inurl:/dump.sql
intitle:"index of" "database"
```

#### 🛜 Network device panels
```
intitle:"Router Configuration"
intitle:"D-Link Configuration"
intitle:"Netgear Router"
inurl:":8080"
inurl:":8443"
```

#### 🔧 Development & environment files
```
filetype:env
filetype:yaml
filetype:gitignore
filetype:log
intitle:"index of" .env
intitle:"index of" config.yaml
```

#### 🧬 Security camera feeds
```
inurl:view/index.shtml
inurl:control/userimage.html
intitle:"IP Camera"
inurl:liveview.cgi
inurl:video.mjpg
```

#### 💰 E-commerce & payment panels
```
inurl:cart
inurl:checkout
inurl:payment
intitle:"Order Confirmation"
filetype:xls "transaction"
```

#### 🧪 Debug & test pages
```
intitle:"Test Page for Apache"
intitle:"PHP Info"
intitle:"Server at"
inurl:test
inurl:debug
```

#### 🔍 Search boxes (injection points)
```
inurl:search.php?q=
inurl:query=
inurl:key=
inurl:s=search
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

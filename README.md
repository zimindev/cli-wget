Звичайно! Ось повний вміст гайду по `wget` у Markdown-форматі — ти можеш просто скопіювати його в файл `wget_guide.md`:

```markdown
# 🌐 `wget` — Non-Interactive Network Downloader

`wget` is a command-line utility for downloading files from the web. It supports HTTP, HTTPS, and FTP protocols and is ideal for downloading files or mirroring entire websites.

---

## ✅ Features

- Supports HTTP, HTTPS, FTP  
- Resume downloads  
- Recursive download (mirror websites)  
- Supports proxies  
- Robust retry and timeout features  
- Works in the background (non-interactive)  

---

## 🔧 Installation

### On Debian/Ubuntu:
sudo apt update && sudo apt install wget
```

### On Red Hat/CentOS/Fedora:
```bash
sudo dnf install wget
```

### On Arch Linux:
```bash
sudo pacman -S wget
```

---

## 🚀 Basic Usage

### 📥 Download a single file:
```bash
wget https://example.com/file.zip
```

### 📂 Download and save with a custom filename:
```bash
wget -O newname.zip https://example.com/file.zip
```

### 🔁 Resume a partially downloaded file:
```bash
wget -c https://example.com/largefile.iso
```

---

## 🌐 Downloading Websites

### 🕸️ Mirror a complete website (recursive download):
```bash
wget --mirror --convert-links --adjust-extension --page-requisites --no-parent https://example.com
```

### Explanation:
- `--mirror`: Enables options suitable for mirroring  
- `--convert-links`: Converts links for offline viewing  
- `--adjust-extension`: Saves files with proper extensions  
- `--page-requisites`: Downloads all assets (CSS, JS, images)  
- `--no-parent`: Avoid downloading parent directories  

### 📁 Example — Save a whole website to your PC:
```bash
wget -P ~/websites --mirror --convert-links --adjust-extension --page-requisites --no-parent https://example.org
```

---

## ⚙️ Useful Options

| Option                     | Description                             |
|----------------------------|-----------------------------------------|
| `-r`                       | Recursive download                      |
| `-l <number>`              | Set recursion level                     |
| `-np`                      | No parent (stay within the directory)   |
| `-c`                       | Resume downloads                        |
| `--limit-rate=200k`        | Limit download speed                    |
| `--user-agent="..."`       | Set custom User-Agent                   |
| `--no-check-certificate`   | Skip SSL certificate checks             |

---

## 🔐 Authenticated Downloads

### Download from a password-protected site:
```bash
wget --user=USERNAME --password=PASSWORD https://example.com/securefile.zip
```

---

## 🔄 Download Files from a List

### With a file containing URLs:
```bash
wget -i urls.txt
```

---

## 📚 More Info

- Website: [https://www.gnu.org/software/wget/](https://www.gnu.org/software/wget/)  
- Man Page: `man wget`

---

## 🧩 Alternatives

- `curl` — More flexible for sending HTTP requests  
- `aria2` — Lightweight multi-protocol & multi-source downloader
```

# 🔍 DeathEye WHOIS CLI

```
██████╗ ███████╗ █████╗ ████████╗██╗  ██╗███████╗██╗   ██╗███████╗
██╔══██╗██╔════╝██╔══██╗╚══██╔══╝██║  ██║██╔════╝██║   ██║██╔════╝
██████╔╝█████╗  ███████║   ██║   ███████║█████╗  ██║   ██║███████╗
██╔══██╗██╔══╝  ██╔══██║   ██║   ██╔══██║██╔══╝  ╚██╗ ██╔╝╚════██║
██║  ██║███████╗██║  ██║   ██║   ██║  ██║███████╗ ╚████╔╝ ███████║
╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝╚══════╝  ╚═══╝  ╚══════╝
                        WHOIS CLI by g0d150ne
====================================================================
```

## 📌 Description

**DeathEye WHOIS CLI** is a fast, lightweight, and flexible command-line tool for performing **WHOIS** domain lookups. It supports both raw socket mode (no external dependencies) and **python-whois** if installed. Works on Linux, macOS, or Windows with Python 3.



## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔎 WHOIS Lookup | Single domain or batch from file |
| ⚡ Auto-detect Server | Automatic detection based on TLD |
| 🌐 Referral Follow | Supports advanced WHOIS referral following |
| 🧩 Output Format | `text` or `json` |
| 🔒 Offline Mode | Works without `python-whois` dependency |
| 🧠 Timeout Config | Adjustable connection timeout |
| 🛠️ Server Override | Manual WHOIS server override |
| 🚫 No Referral | Option to disable referral following |



## 📦 Installation

### 1. Prerequisites
```bash
python3 --version  # Minimum Python 3.6
```

### 2. Clone or Download
```bash
git clone https://github.com/g0d150ne/REATHEVS
cd REATHEVS
chmod +x whois_cli.py
```

### 3. (Optional) Install python-whois
```bash
pip install python-whois
```


## 🚀 Usage

### Basic
```bash
python3 whois_cli.py example.com
```

### JSON Output
```bash
python3 whois_cli.py -o json example.com
```

### Batch Mode (domain list file)
```bash
python3 whois_cli.py -b domains.txt
```

### Override WHOIS Server
```bash
python3 whois_cli.py -s whois.crsnic.net example.com
```

### Disable Referral
```bash
python3 whois_cli.py --no-referral example.com
```

### Quiet Mode (raw output only)
```bash
python3 whois_cli.py -q example.com
```



## 🧾 Example Output

```bash
$ python3 whois_cli.py example.com

====================================================================
Domain: example.com
Server used: whois.verisign-grs.com

--- RAW WHOIS ---

Domain Name: EXAMPLE.COM
Registry Domain ID: 2336799_DOMAIN_COM-VRSN
Registrar WHOIS Server: whois.iana.org
Registrar URL: http://res-dom.iana.org
...
====================================================================
```

### JSON Output
```json
{
  "domain": "example.com",
  "server": "whois.verisign-grs.com",
  "raw": "Domain Name: EXAMPLE.COM\n..."
}
```


## ⚙️ Full Options

| Option | Description | Default |
|--------|-------------|---------|
| `-s, --server` | Manual WHOIS server | (auto) |
| `-p, --port` | WHOIS server port | 43 |
| `-t, --timeout` | Connection timeout (seconds) | 8 |
| `-o, --output` | Output format: `text` / `json` | text |
| `-b, --batch` | File with domain list | - |
| `-q, --quiet` | Quiet mode (raw only) | false |
| `--no-referral` | Disable referral following | false |


## 📁 Project Structure

```
DeathEye-Whois/
├── whois_cli.py      # Main program
├── README.md         # Documentation
├── domains.txt       # (Optional) Domain list
└── LICENSE           # MIT License
```



## 🧠 How It Works

1. **TLD Detection** → Find appropriate WHOIS server
2. **WHOIS Query** → Send request to server
3. **Follow Referral** → If referral exists, continue to new server
4. **Parse & Display** → Output in selected format



## 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| `Connection timeout` | Try `--timeout 15` |
| `No WHOIS server found` | Use `-s` for manual override |
| `Referral loop` | Use `--no-referral` |
| `Permission denied` | `chmod +x whois_cli.py` |



## 📋 Dependencies

- **Python 3.6+** (required)
- **python-whois** (optional, for fallback)



## 🧑‍💻 Author

**g0d150ne** — Cyber Security & Automation Enthusiast 🕶️  
- GitHub: [github.com/g0d150ne](https://github.com/g0d150ne)  
- License: MIT



## ⚠️ Disclaimer

> This tool is for **educational and system administration purposes only**.  
> Usage against third-party domains without permission is the **user's responsibility**.



```
💀 "Watch the Net. See everything. Fear nothing." — g0d150ne

## 📄 License

MIT License - Free to use and modify.
```

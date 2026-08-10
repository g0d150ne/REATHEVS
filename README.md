# 🔍 DeathEye WHOIS CLI

```
██████╗ ███████╗ █████╗ ████████╗██╗  ██╗███████╗██╗   ██╗███████╗
██╔══██╗██╔════╝██╔══██╗╚══██╔══╝██║  ██║██╔════╝██║   ██║██╔════╝
██████╔╝█████╗  ███████║   ██║   ███████║█████╗  ██║   ██║███████╗
██╔══██╗██╔══╝  ██╔══██║   ██║   ██╔══██║██╔══╝  ╚██╗ ██╔╝╚════██║
██║  ██║███████╗██║  ██║   ██║   ██║  ██║███████╗ ╚████╔╝ ███████║
╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝╚══════╝  ╚═══╝  ╚══════╝
                        Whois CLI by g0d150ne
====================================================================
```

## 📖 Deskripsi

**DeathEye WHOIS CLI** adalah alat baris perintah (command-line tool) untuk melakukan pencarian **WHOIS** domain dengan cepat, ringan, dan fleksibel.

Mendukung mode socket mentah (tanpa dependensi eksternal) maupun **python-whois** jika terpasang.  
Dapat dijalankan di Linux, macOS, atau Windows dengan Python 3.

## ✨ Fitur

- 🔎 WHOIS lookup untuk domain tunggal atau batch file  
- ⚡ Auto-detect WHOIS server berdasarkan TLD  
- 🌐 Mendukung referensi WHOIS lanjutan (referral follow)  
- 🧩 Output format `text` atau `json`  
- 🔒 Dapat dijalankan offline (tanpa python-whois)  
- 🧠 Timeout dan server override opsional  
- 🛠️ ASCII banner "DeathEye" bawaan

## 📦 Instalasi

1. Pastikan Python 3 terinstal:
   ```bash
   python3 --version
   ```

2. (Opsional) Instal dependensi `python-whois`:
   ```bash
   pip install python-whois
   ```

3. Simpan file sebagai `whois_cli.py`  
   Pastikan file bisa dieksekusi:
   ```bash
   chmod +x whois_cli.py
   ```

## 🚀 Penggunaan

### 🔹 WHOIS domain tunggal
```bash
python3 whois_cli.py example.com
```

### 🔹 Output JSON
```bash
python3 whois_cli.py -o json example.com
```

### 🔹 Batch mode (list domain dari file)
```bash
python3 whois_cli.py -b domains.txt
```

### 🔹 Override server
```bash
python3 whois_cli.py -s whois.crsnic.net example.com
```

### 🔹 Nonaktifkan referral WHOIS
```bash
python3 whois_cli.py --no-referral example.com
```

## 🧾 Contoh Output

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

## 🧠 Struktur Proyek

```
DeathEye-Whois/
├── whois_cli.py     # Main program
├── README.md         # Dokumentasi ini
└── domains.txt       # (Opsional) daftar domain untuk batch
```

## ⚙️ Opsi Lengkap

| Opsi | Deskripsi |
|------|------------|
| `-s`, `--server` | Tentukan WHOIS server manual |
| `-p`, `--port` | Port WHOIS server (default 43) |
| `-t`, `--timeout` | Timeout koneksi (default 8 detik) |
| `-o`, `--output` | Format output: `text` atau `json` |
| `-b`, `--batch` | File berisi daftar domain |
| `-q`, `--quiet` | Mode tenang (raw WHOIS saja) |
| `--no-referral` | Nonaktifkan follow WHOIS referral |

## 🧑‍💻 Author
**DeathEye** — Cyber Security & Automation Enthusiast 🕶️  
GitHub: [github.com/g0d150ne](https://github.com/g0d150ne)  
License: MIT  

## 🧩 Catatan
> Tools ini dibuat untuk tujuan edukasi dan administrasi sistem.  
> Penggunaan terhadap domain pihak ketiga tanpa izin adalah tanggung jawab pengguna.

```
💀 "Watch the Net. See everything. Fear nothing." — g0d150ne
```

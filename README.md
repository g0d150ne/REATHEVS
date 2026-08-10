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

## 📌 Deskripsi

**DeathEye WHOIS CLI** adalah command-line tool untuk pencarian WHOIS domain yang cepat, ringan, dan fleksibel. Mendukung mode socket mentah (tanpa dependensi eksternal) maupun `python-whois` jika terpasang.


## ✨ Fitur

| Fitur | Keterangan |
|-------|------------|
| 🔎 WHOIS Lookup | Domain tunggal atau batch dari file |
| ⚡ Auto-detect Server | Deteksi otomatis berdasarkan TLD |
| 🌐 Referral Follow | Dukungan follow referral WHOIS |
| 🧩 Output Format | `text` atau `json` |
| 🔒 Offline Mode | Berjalan tanpa `python-whois` |
| 🧠 Timeout Config | Timeout koneksi bisa diatur |
| 🛠️ Server Override | Manual override WHOIS server |
| 🚫 No Referral | Opsi nonaktifkan referral |


## 📦 Instalasi

### 1. Prasyarat
```bash
python3 --version  # Minimal Python 3.6
```

### 2. Clone atau Download
```bash
git clone https://github.com/g0d150ne/DeathEye-Whois
cd DeathEye-Whois
chmod +x whois_cli.py
```

### 3. (Opsional) Install python-whois
```bash
pip install python-whois
```


## 🚀 Penggunaan

### Dasar
```bash
python3 whois_cli.py example.com
```

### Output JSON
```bash
python3 whois_cli.py -o json example.com
```

### Batch Mode (file domain list)
```bash
python3 whois_cli.py -b domains.txt
```

### Override WHOIS Server
```bash
python3 whois_cli.py -s whois.crsnic.net example.com
```

### Nonaktifkan Referral
```bash
python3 whois_cli.py --no-referral example.com
```

### Mode Tenang (raw output)
```bash
python3 whois_cli.py -q example.com
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

### Output JSON
```json
{
  "domain": "example.com",
  "server": "whois.verisign-grs.com",
  "raw": "Domain Name: EXAMPLE.COM\n..."
}
```


## ⚙️ Opsi Lengkap

| Opsi | Deskripsi | Default |
|------|-----------|---------|
| `-s, --server` | WHOIS server manual | (auto) |
| `-p, --port` | Port WHOIS server | 43 |
| `-t, --timeout` | Timeout koneksi (detik) | 8 |
| `-o, --output` | Format: `text` / `json` | text |
| `-b, --batch` | File daftar domain | - |
| `-q, --quiet` | Mode tenang (raw only) | false |
| `--no-referral` | Nonaktifkan follow referral | false |


## 📁 Struktur Proyek

```
DeathEye-Whois/
├── whois_cli.py      # Main program
├── README.md         # Dokumentasi
├── domains.txt       # (Opsional) Daftar domain
└── LICENSE           # MIT License
```


## 🧠 Cara Kerja

1. **Deteksi TLD** → Cari WHOIS server yang sesuai
2. **Query WHOIS** → Kirim request ke server
3. **Follow Referral** → Jika ada referral, lanjutkan ke server baru
4. **Parse & Tampilkan** → Output sesuai format yang dipilih


## 🛠️ Troubleshooting

| Masalah | Solusi |
|---------|--------|
| `Connection timeout` | Coba `--timeout 15` |
| `No WHOIS server found` | Gunakan `-s` untuk manual override |
| `Referral loop` | Gunakan `--no-referral` |
| `Permission denied` | `chmod +x whois_cli.py` |


## 📋 Dependencies

- **Python 3.6+** (wajib)
- **python-whois** (opsional, untuk fallback)


## 🧑‍💻 Author

**g0d150ne** — Cyber Security & Automation Enthusiast 🕶️  
- GitHub: [github.com/g0d150ne](https://github.com/g0d150ne)  
- License: MIT


## ⚠️ Disclaimer

> Tools ini dibuat untuk **tujuan edukasi dan administrasi sistem**.  
> Penggunaan terhadap domain pihak ketiga tanpa izin adalah **tanggung jawab pengguna**.


```
💀 "Watch the Net. See everything. Fear nothing." — g0d150ne
```

## 📄 License

MIT License - Free to use and modify.
```

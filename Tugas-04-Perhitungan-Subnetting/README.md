# TUGAS KONSEP JARINGAN
## Tugas 4: Perhitungan Subnetting IPv4 & FLSM

**Identitas Mahasiswa:**
- **Nama:** Melodia Bunga Chantika
- **NRP:** 3125600038
- **Mata Kuliah:** Konsep Jaringan (Praktikum Minggu 3 — IPv4 Addressing & Subnetting)
- **Dosen Pengajar:** Dr. Ferry Astika Saputra, ST, M.Sc
- **Program Studi:** D4 Teknik Informatika, Politeknik Elektronika Negeri Surabaya (PENS)
- **Tahun:** 2026

---

## 1. Landasan Teori Subnetting (FLSM)

*Fixed Length Subnet Mask* (FLSM) adalah teknik pembagian jaringan IP di mana seluruh subnet hasil pembagian memiliki panjang prefix (/n) dan jumlah host yang sama.

### Rumus Dasar Subnetting:
1. **Jumlah Subnet:**
   $$\text{Jumlah Subnet} = 2^s$$
   *(di mana $s$ adalah jumlah bit yang dipinjam dari host portion).*
2. **Jumlah Alamat Total per Subnet (*Block Size*):**
   $$\text{Block Size} = 2^h$$
   *(di mana $h$ adalah sisa bit host, $h = 32 - \text{prefix baru}$).*
3. **Jumlah Host Valid (*Usable Hosts*):**
   $$\text{Usable Hosts} = 2^h - 2$$
   *(-2 untuk Network Address dan Broadcast Address).*

---

## 2. Soal Kasus Subnetting

### Soal 1: Pembagian 4 Subnet Sama Besar
**Diberikan blok IP:** `192.168.20.0/24`  
**Kebutuhan:** Bagilah blok tersebut menjadi **4 subnet** dengan ukuran yang sama besar.

#### Langkah Penyelesaian:
1. **Menentukan Bit yang Dipinjam ($s$):**
   $$2^s \ge 4 \implies s = 2\text{ bit}$$
2. **Menentukan Prefix Baru:**
   $$\text{Prefix Baru} = 24 + 2 = /26$$
3. **Subnet Mask Baru:**
   - 26 bit bernilai biner `1`: `11111111.11111111.11111111.11000000`
   - Dalam notasi desimal: **`255.255.255.192`**
4. **Menentukan Block Size (Ukuran Blok Tiap Subnet):**
   $$\text{Sisa bit host } (h) = 32 - 26 = 6\text{ bit}$$
   $$\text{Block Size} = 2^6 = 64\text{ alamat (atau } 256 - 192 = 64\text{)}$$
   $$\text{Usable Hosts} = 2^6 - 2 = 62\text{ host per subnet}$$

#### Tabel Hasil Pembagian 4 Subnet:

| Subnet Ke- | Network Address | Subnet Mask | Usable Host Range | Broadcast Address | Total Alamat / Usable |
|:---:|:---|:---|:---|:---|:---:|
| **Subnet 1** | `192.168.20.0/26` | `255.255.255.192` | `192.168.20.1` – `192.168.20.62` | `192.168.20.63` | 64 / 62 |
| **Subnet 2** | `192.168.20.64/26` | `255.255.255.192` | `192.168.20.65` – `192.168.20.126` | `192.168.20.127` | 64 / 62 |
| **Subnet 3** | `192.168.20.128/26` | `255.255.255.192` | `192.168.20.129` – `192.168.20.190` | `192.168.20.191` | 64 / 62 |
| **Subnet 4** | `192.168.20.192/26` | `255.255.255.192` | `192.168.20.193` – `192.168.20.254` | `192.168.20.255` | 64 / 62 |

---

### Soal 2: Penentuan Parameter IP Tertentu
**Diberikan IP Host:** `192.168.10.130/26`  
**Pertanyaan:** Tentukan Network Address, Subnet Mask, Host Pertama, Host Terakhir, dan Broadcast Address.

#### Analisis:
1. **Prefix:** `/26` $\implies$ Subnet Mask: `255.255.255.192`
2. **Block size:** $256 - 192 = 64$.
3. Kelipatan blok subnet pada oktet ke-4: $0, 64, 128, 192$.
4. Karena nilai host adalah $130$, maka $130$ berada di rentang blok **$128$ hingga $191$**.

#### Hasil:
- **Network Address:** `192.168.10.128`
- **Subnet Mask:** `255.255.255.192`
- **Host Pertama (*First Usable*):** `192.168.10.129`
- **Host Terakhir (*Last Usable*):** `192.168.10.190`
- **Broadcast Address:** `192.168.10.191`

---

## 3. Kesimpulan
Dengan teknik subnetting (FLSM), ruang alamat `192.168.20.0/24` berhasil dipecah menjadi 4 *broadcast domain* independen yang masing-masing mampu menampung hingga 62 perangkat host, sehingga membatasi penyebaran trafik broadcast dan meningkatkan efisiensi serta keamanan jaringan.

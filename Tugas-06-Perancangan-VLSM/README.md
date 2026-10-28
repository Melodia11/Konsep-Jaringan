# TUGAS KONSEP JARINGAN
## Tugas 6: Perancangan Variable Length Subnet Mask (VLSM)

**Identitas Mahasiswa:**
- **Nama:** Melodia Bunga Chantika
- **NRP:** 3125600038
- **Mata Kuliah:** Konsep Jaringan (Praktikum Minggu 6 — VLSM & Routing)
- **Dosen Pengajar:** Dr. Ferry Astika Saputra, ST, M.Sc
- **Program Studi:** D4 Teknik Informatika, Politeknik Elektronika Negeri Surabaya (PENS)
- **Tahun:** 2026

---

## 1. Deskripsi Penugasan
Rancanglah pengalamatan jaringan menggunakan metode **VLSM (*Variable Length Subnet Mask*)** dengan parameter acuan berikut:
- **Parent Network:** `10.252.108.0/24` (Total 256 alamat IP)
- **Kebutuhan Subnet:**
  1. **Lab A:** 90 host
  2. **Lab B:** 60 host
  3. **Administrasi:** 14 host
  4. **End-point (Tautan Point-to-Point):** 2 host

---

## 2. Prinsip & Metodologi Perancangan VLSM

Dalam perancangan VLSM, alokasi blok subnet wajib diurutkan **dari kebutuhan host terbesar ke terkecil** untuk menghindari terjadinya fragmentasi ruang alamat dan mencegah overlap (*overlapping subnet*).

### Rumus Penentuan Bit Host ($h$):
$$2^h - 2 \ge \text{Kebutuhan Host}$$
$$\text{Prefix Baru} = 32 - h$$
$$\text{Block Size (Ukuran Blok)} = 2^h$$

---

## 3. Langkah-Langkah Perhitungan per Segmen

### 3.1 Segmen 1: Lab A (90 Host)
1. **Perhitungan Bit Host ($h$):**
   $$2^h - 2 \ge 90 \implies 2^7 - 2 = 126 \ge 90 \implies h = 7\text{ bit}$$
2. **Panjang Prefix & Subnet Mask:**
   - Prefix: $32 - 7 = \mathbf{/25}$
   - Subnet Mask: **`255.255.255.128`**
   - *Block Size*: $2^7 = 128$ alamat.
3. **Alokasi Alamat:**
   - **Network Address:** `10.252.108.0/25`
   - **Usable Host Range:** `10.252.108.1` s/d `10.252.108.126` (Kapasitas: 126 host)
   - **Default Gateway (Direkomendasikan IP Pertama):** `10.252.108.1`
   - **Broadcast Address:** `10.252.108.127`
   - *Rentang Alamat Terpakai:* `10.252.108.0` – `10.252.108.127`

---

### 3.2 Segmen 2: Lab B (60 Host)
1. **Perhitungan Bit Host ($h$):**
   $$2^h - 2 \ge 60 \implies 2^6 - 2 = 62 \ge 60 \implies h = 6\text{ bit}$$
2. **Panjang Prefix & Subnet Mask:**
   - Prefix: $32 - 6 = \mathbf{/26}$
   - Subnet Mask: **`255.255.255.192`**
   - *Block Size*: $2^6 = 64$ alamat.
3. **Alokasi Alamat (Melanjutkan dari `.128`):**
   - **Network Address:** `10.252.108.128/26`
   - **Usable Host Range:** `10.252.108.129` s/d `10.252.108.190` (Kapasitas: 62 host)
   - **Default Gateway:** `10.252.108.129`
   - **Broadcast Address:** `10.252.108.191`
   - *Rentang Alamat Terpakai:* `10.252.108.128` – `10.252.108.191`

---

### 3.3 Segmen 3: Administrasi (14 Host)
1. **Perhitungan Bit Host ($h$):**
   $$2^h - 2 \ge 14 \implies 2^4 - 2 = 14 \ge 14 \implies h = 4\text{ bit}$$
2. **Panjang Prefix & Subnet Mask:**
   - Prefix: $32 - 4 = \mathbf{/28}$
   - Subnet Mask: **`255.255.255.240`**
   - *Block Size*: $2^4 = 16$ alamat.
3. **Alokasi Alamat (Melanjutkan dari `.192`):**
   - **Network Address:** `10.252.108.192/28`
   - **Usable Host Range:** `10.252.108.193` s/d `10.252.108.206` (Kapasitas: 14 host)
   - **Default Gateway:** `10.252.108.193`
   - **Broadcast Address:** `10.252.108.207`
   - *Rentang Alamat Terpakai:* `10.252.108.192` – `10.252.108.207`

---

### 3.4 Segmen 4: End-point / Link Point-to-Point (2 Host)
1. **Perhitungan Bit Host ($h$):**
   $$2^h - 2 \ge 2 \implies 2^2 - 2 = 2 \ge 2 \implies h = 2\text{ bit}$$
2. **Panjang Prefix & Subnet Mask:**
   - Prefix: $32 - 2 = \mathbf{/30}$
   - Subnet Mask: **`255.255.255.252`**
   - *Block Size*: $2^2 = 4$ alamat.
3. **Alokasi Alamat (Melanjutkan dari `.208`):**
   - **Network Address:** `10.252.108.208/30`
   - **Usable Host Range:** `10.252.108.209` s/d `10.252.108.210` (Kapasitas: 2 host/ujung tautan)
   - **Broadcast Address:** `10.252.108.211`
   - *Rentang Alamat Terpakai:* `10.252.108.208` – `10.252.108.211`

---

## 4. Tabel Ringkasan Alokasi VLSM

| Segmen Jaringan | Kebutuhan Host | Prefix | Subnet Mask | Network Address | Usable Host Range | Broadcast Address | Alamat Tersedia |
| :--- | :---: | :---: | :--- | :--- | :--- | :--- | :---: |
| **Lab A** | 90 | `/25` | `255.255.255.128` | `10.252.108.0` | `10.252.108.1` – `10.252.108.126` | `10.252.108.127` | 126 host |
| **Lab B** | 60 | `/26` | `255.255.255.192` | `10.252.108.128` | `10.252.108.129` – `10.252.108.190` | `10.252.108.191` | 62 host |
| **Administrasi** | 14 | `/28` | `255.255.255.240` | `10.252.108.192` | `10.252.108.193` – `10.252.108.206` | `10.252.108.207` | 14 host |
| **End-point (P2P)**| 2 | `/30` | `255.255.255.252` | `10.252.108.208` | `10.252.108.209` – `10.252.108.210` | `10.252.108.211` | 2 host |
| **Unallocated (Sisa)**| - | - | - | `10.252.108.212` s/d `10.252.108.255` | - | - | 44 alamat |

---

## 5. Analisis Efisiensi & Ruang Alamat Bebas

1. **Total Alokasi Alamat:**
   $$\text{Total Terpakai} = 128 + 64 + 16 + 4 = 212\text{ alamat IP}$$
2. **Efisiensi Penggunaan Blok `/24`:**
   $$\text{Efisiensi} = \frac{212}{256} \times 100\% = 82,81\%$$
3. **Analisis Ruang Bebas (*Unassigned Space*):**
   Terdapat **44 alamat** tersisa dari `10.252.108.212` hingga `10.252.108.255`. Ruang ini dapat dialokasikan lebih lanjut secara rapi mengikuti aturan *power-of-two alignment*:
   - 1 blok `/27` (32 alamat): `10.252.108.224/27` (memerlukan buffer sebelum offset 224)
   - ATAU kombinasi 2 blok `/28` (16 alamat) dan blok `/29` atau `/30` untuk tautan titik ke titik baru.

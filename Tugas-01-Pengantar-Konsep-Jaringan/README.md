# TUGAS 01: PENGANTAR KONSEP JARINGAN & STANDAR WI-FI

**Identitas Mahasiswa:**
- **Nama:** Melodia Bunga Chantika
- **NRP:** 3125600038
- **Kelas:** 2 D4 Teknik Informatika A
- **Dosen Pengajar:** Dr. Ferry Astika Saputra, ST, M.Sc
- **Mata Kuliah:** Konsep Jaringan (Minggu 1)
- **Institusi:** Politeknik Elektronika Negeri Surabaya (PENS) - 2026

---

## A. Tugas Bab 1

### Level A – Ingatan dan Pemahaman

#### 1. Jelaskan pengertian jaringan komputer dengan menyebutkan empat unsur pokoknya.
> **Jawaban:** *(Berada di Subbab 1.2)*

Jaringan komputer adalah sekumpulan perangkat otonom yang saling terhubung melalui satu atau lebih media komunikasi untuk bertukar data dan berbagi sumber daya berdasarkan aturan komunikasi yang disepakati. 

Empat unsur pokoknya:
- **Perangkat akhir (*end system* atau *host*):** Sumber atau tujuan data (seperti laptop, server web, telepon IP, dan sensor suhu).
- **Media komunikasi:** Pembawa sinyal dari satu titik ke titik lain (kabel tembaga, serat optik, gelombang radio, gelombang mikro, atau satelit).
- **Perangkat perantara:** Penerus, pengendali, atau pelindung lalu lintas data (switch, router, firewall).
- **Protokol:** Aturan komunikasi yang menentukan format pesan, urutan pertukaran, cara mengenali pengirim/penerima, dan tindakan saat terjadi kesalahan.

---

#### 2. Apa yang dimaksud dengan perangkat otonom dalam definisi jaringan?
> **Jawaban:** *(Berada di Subbab 1.2)*

Perangkat otonom berarti setiap perangkat tetap memiliki fungsi dan kendali komputasinya sendiri, serta tidak kehilangan identitasnya ketika bergabung ke dalam jaringan. Komunikasi terjadi antarsistem yang masing-masing memiliki sumber daya, status, dan kemungkinan kegagalan sendiri (bukan berada di bawah kendali kaku sebagai satu mesin tunggal).

---

#### 3. Bedakan data, sinyal, dan paket.
> **Jawaban:** *(Berada di Subbab 1.2.2)*

- **Data:** Representasi informasi (teks, citra, suara, dan video) yang diubah menjadi bit.
- **Sinyal:** Bentuk fisik yang membawa bit representasi informasi tersebut melalui media transmisi (berupa perubahan tegangan listrik, pulsa cahaya, atau gelombang radio).
- **Paket:** Unit-unit pecahan data aplikasi yang lebih kecil dan diberi tambahan informasi kendali (seperti alamat, nomor urut, atau penanda integritas) agar dapat diteruskan secara fleksibel dan berbagi infrastruktur dengan pengguna lain.

---

#### 4. Jelaskan perbedaan PAN, LAN, MAN, dan WAN tanpa hanya menggunakan ukuran jarak.
> **Jawaban:** *(Berada di Subbab 1.4)*

- **PAN (*Personal Area Network*):** Jaringan di sekitar individu yang berorientasi pada perangkat personal (seperti Bluetooth dan NFC), berdaya pancar rendah, dan dikelola secara mandiri oleh individu.
- **LAN (*Local Area Network*):** Jaringan pada area lokal (rumah, gedung, kampus) yang memiliki kendali administratif terpadu di bawah satu organisasi/rumah tangga, serta umumnya menawarkan kapasitas tinggi dan latensi rendah.
- **MAN (*Metropolitan Area Network*):** Jaringan yang menghubungkan beberapa lokasi dalam satu kawasan perkotaan, biasanya disediakan oleh operator (misal Metro Ethernet atau jaringan serat) dengan batas tanggung jawab yang jelas antara pelanggan dan penyedia.
- **WAN (*Wide Area Network*):** Jaringan yang menghubungkan lokasi-lokasi yang berjauhan (antarkota/antarnegara) dan melibatkan infrastruktur milik satu atau banyak operator telekomunikasi (seperti tautan sewa, MPLS, atau satelit).

---

#### 5. Apa perbedaan intranet, ekstranet, dan Internet publik?
> **Jawaban:** *(Berada di Subbab 1.5)*

- **Intranet:** Lingkungan jaringan dan layanan internal yang berbasis teknologi Internet, tetapi hak aksesnya dibatasi ketat hanya bagi anggota internal organisasi (contoh: portal pegawai).
- **Ekstranet:** Perluasan sebagian layanan internal yang dibuka secara terbatas kepada pihak eksternal terpilih yang telah memiliki otorisasi (contoh: portal pemasok atau mitra riset).
- **Internet publik:** Keterhubungan terbuka antarbanyak jaringan secara global yang dapat diakses oleh masyarakat umum, di mana setiap server/layanan tetap dapat menerapkan perlindungan dan keamanannya sendiri.

---

#### 6. Mengapa Wi-Fi tidak dapat disamakan dengan Internet?
> **Jawaban:** *(Berada di Subbab 1.19)*

Karena Wi-Fi hanya menyediakan media transmisi untuk jaringan akses lokal secara nirkabel (LAN nirkabel). Perangkat pengguna dapat terhubung dengan baik ke sinyal Wi-Fi lokal tanpa otomatis memiliki jalur keluar atau konektivitas yang tersambung ke jaringan Internet global.

---

#### 7. Jelaskan perbedaan client, server, dan peer.
> **Jawaban:** *(Berada di Subbab 1.6.1)*

- **Client:** Pihak atau aplikasi pada sistem akhir yang bertindak meminta layanan.
- **Server:** Pihak atau sistem yang menyediakan layanan, dirancang untuk melayani banyak client, beroperasi secara terus-menerus, dan dikelola secara terpusat.
- **Peer:** Node atau perangkat yang memiliki kedudukan setara, di mana setiap node dapat bertindak sebagai peminta sekaligus penyedia sumber daya secara langsung tanpa harus bergantung mutlak pada satu server pusat.

---

#### 8. Apa perbedaan bandwidth, throughput, dan goodput?
> **Jawaban:** *(Berada di Subbab 1.10)*

- **Bandwidth:** Kapasitas nominal atau laju data maksimum yang secara teoritis tersedia pada suatu kanal/tautan.
- **Throughput:** Laju data aktual yang benar-benar berhasil dipindahkan melintasi jaringan, yang di dalamnya masih mencakup beban tambahan (*overhead*) protokol.
- **Goodput:** Laju muatan data aplikasi yang benar-benar berguna yang diterima oleh pengguna, murni tanpa menghitung header protokol maupun paket pengiriman ulang (*retransmission*).

---

#### 9. Sebutkan empat komponen nodal delay.
> **Jawaban:** *(Berada di Subbab 1.10.2)*

- **Processing delay ($d_{proc}$):** Waktu untuk memeriksa header paket, memvalidasi data/kesalahan, dan menentukan antarmuka tujuan.
- **Queuing delay ($d_{queue}$):** Waktu menunggu paket di dalam antrean buffer sebelum diteruskan ke media.
- **Transmission delay ($d_{trans}$):** Waktu yang dibutuhkan untuk menempatkan seluruh bit paket ke media transmisi ($L/R$).
- **Propagation delay ($d_{prop}$):** Waktu yang dibutuhkan sinyal untuk merambat secara fisik melintasi media dari satu titik ke titik tujuan ($d/s$).

---

#### 10. Mengapa Web tidak sama dengan Internet?
> **Jawaban:** *(Berada di Subbab 1.14.5)*

Internet adalah infrastruktur jaringan fisik beserta keluarga protokol komunikasi yang menghubungkan komputer secara global, sedangkan World Wide Web (Web) hanyalah salah satu bentuk layanan aplikasi di atas infrastruktur Internet tersebut (bersama dengan aplikasi lain seperti email, DNS, dan SSH).

---

### Level B – Penerapan dan Analisis

#### 1. Sebuah paket berukuran 1.000 byte dikirim melalui tautan 10 Mbps. Hitung transmission delay ideal paket tersebut. Jelaskan komponen delay yang belum tercakup.

- Ukuran paket ($L$) = $1.000\text{ byte} \times 8\text{ bit/byte} = 8.000\text{ bit}$.
- Kecepatan tautan ($R$) = $10\text{ Mbps} = 10.000.000\text{ bit/detik}$.
- **Rumus transmisi ideal:**
  $$d_{trans} = \frac{L}{R} = \frac{8.000}{10.000.000} = 0,0008\text{ detik} = 0,8\text{ ms}$$

Komponen yang belum masuk ke dalam perhitungan total meliputi:
1. *Processing delay* ($d_{proc}$)
2. *Queuing delay* ($d_{queue}$)
3. *Propagation delay* ($d_{prop}$)

---

#### 2. Sebuah kampus memiliki koneksi Internet 2 Gbps, tetapi pengguna di satu lantai hanya memperoleh throughput rendah. Susun sedikitnya lima hipotesis yang tidak langsung menyalahkan koneksi ISP.

**Hipotesis Masalah:**
1. **Kepadatan pengguna access point:** Terlalu banyak perangkat mahasiswa/staf yang terhubung ke satu titik pancar Wi-Fi di lantai tersebut, sehingga terjadi perebutan alokasi frekuensi.
2. **Interferensi sinyal radio:** Adanya gangguan gelombang radio di sekitar lantai tersebut (seperti benturan sinyal antar-pemancar atau dinding penghalang yang tebal) yang memperburuk jaringan sinyal.
3. **Kabel jaringan lokal bermasalah:** Kabel tembaga penghubung switch atau access point di lantai itu berkualitas buruk, rusak, atau terpasang longgar.
4. **Kapasitas tautan keluar (*uplink*) terbatas:** Kabel atau port jaringan yang menghubungkan switch di lantai tersebut ke switch utama kampus berkapasitas terlalu kecil (*bottleneck*).
5. **Kesalahan konfigurasi atau pembatasan lalu lintas:** Adanya aturan pembatasan akses (*traffic policy*) atau terjadinya perputaran data tanpa henti (*looping*) pada lapisan switch di lantai tersebut.

---

#### 3. Bandingkan kebutuhan jaringan untuk transfer berkas cadangan dan panggilan video. Metrik apa yang paling penting bagi masing-masing aplikasi?

1. **Transfer Berkas Cadangan:**  
   Membutuhkan kapasitas (*throughput*) yang besar dan keutuhan data yang mutlak (data tidak boleh hilang atau korup sama sekali), tetapi sangat longgar terhadap jeda waktu (*latency*) dan keteraturan waktu tiba paket (*jitter*).
2. **Panggilan Video:**  
   Sangat bergantung pada kecepatan respons dan keteraturan pengiriman data agar suara dan gambar tidak patah-patah. Kehilangan sebagian kecil data masih bisa ditoleransi oleh sistem aplikasi.

---

#### 4. Sebuah organisasi mempunyai dua koneksi Internet dari dua operator. Keduanya melewati tiang dan jalur ducting yang sama. Evaluasi kualitas redundansinya.

**Evaluasi:**  
Kualitas redundansinya tergolong buruk, karena meskipun secara kontrak dan sistem logis organisasi tersebut memiliki dua penyedia Internet yang berbeda, keduanya masih bertumpu pada satu jalur infrastruktur fisik yang sama (*single point of failure*). Jika tiang tersebut roboh atau saluran pipa kabel bawah tanah terputus akibat galian, kedua koneksi akan mati secara serentak.

---

#### 5. Jelaskan mengapa penambahan bandwidth tidak selalu mengurangi waktu akses ke server yang sangat jauh.

**Jawaban:**  
Penambahan *bandwidth* hanya memperlebar kapasitas atau pipa pengiriman data, tetapi tidak dapat mempercepat rambatan sinyal fisik di media kabel atau serat optik (*propagation delay*). Waktu tempuh paket ke server yang sangat jauh sangat dipengaruhi oleh jarak geografis ($d/s$) dan banyaknya persimpangan router yang harus dilewati. Jika masalah utamanya adalah jarak jauh, server tujuan yang sibuk, atau waktu tunggu bolak-balik (RTT), memperbesar kapasitas data tidak akan mempersingkat waktu respon secara signifikan.

---

#### 6. Sebuah layanan tersedia 99,9% selama satu tahun. Hitung perkiraan maksimum durasi ketidaktersediaannya. Bandingkan dengan target 99,99%.

**Jawaban:**

1. **Perhitungan layanan 99,9%:**
   - Waktu padam maksimum = $100\% - 99,9\% = 0,1\%$ dalam satu tahun.
   - $1\text{ tahun} = 365\text{ hari} \times 24\text{ jam} = 8.760\text{ jam}$.
   - Durasi henti = $0,001 \times 8.760\text{ jam} = 8,76\text{ jam}$.

2. **Perbandingan dengan Target 99,99%:**
   - Waktu padam maksimum = $100\% - 99,99\% = 0,01\%$ dalam setahun.
   - Durasi henti = $0,0001 \times 8.760\text{ jam} = 0,876\text{ jam}$ (atau sekitar $52\text{ menit per tahun}$).
   - **Perbandingan:** Menaikkan keandalan satu angka sembilan (dari 99,9% ke 99,99%) secara drastis memangkas toleransi gangguan dari hampir 9 jam menjadi hanya sekitar 52 menit dalam kurun waktu satu tahun penuh.

---

#### 7. Analisis kelebihan dan kelemahan client–server serta P2P untuk distribusi berkas berukuran besar kepada ribuan pengguna.

1. **Model Client-Server:**
   - **Kelebihan:** Pengendalian terpusat, pengawasan hak akses sangat mudah diatur, dan pembaruan versi berkas tetap seragam.
   - **Kelemahan:** Server pusat dapat menjadi titik kemacetan beban (*bottleneck*) serta rentan menjadi titik tunggal kegagalan (*single point of failure*); biaya kapasitas server dan jaringan melonjak drastis saat diakses ribuan pengguna bersamaan.

2. **Model Peer-to-Peer (P2P):**
   - **Kelebihan:** Kemampuan melayani beban bertambah seiring bertambahnya pengguna karena tiap komputer yang mengunduh berkas sekaligus membagikannya ke komputer lain (skalabilitas tinggi), serta tidak bergantung mutlak pada satu server pusat.
   - **Kelemahan:** Pengaturan keamanan dan keaslian berkas lebih sulit dikendalikan, serta sulit memastikan konsistensi ketersediaan data jika pengguna yang memegang berkas sering keluar-masuk jaringan.

---

#### 8. Berikan contoh ketika topologi fisik dan topologi logis pada jaringan kampus berbeda.

**Contoh Kasus:**
1. **Topologi Fisik Bintang (*Star*):** Di dalam sebuah gedung kampus, semua kabel jaringan dari komputer laboratorium, komputer dosen, dan kamera keamanan ditarik dan ditancapkan ke perangkat *switch* yang sama di ruang server.
2. **Topologi Logis Terpisah (*Segmented/VLAN*):** Secara aliran data sebenarnya, komputer laboratorium, komputer staf dosen, dan kamera keamanan tersebut dipisahkan jalurnya menggunakan jaringan virtual (VLAN) dan subnet yang berbeda.
3. **Penjelasan:** Bentuk fisik pemasangan kabelnya terlihat menyatu ke satu titik pusat (bintang), tetapi alur komunikasi datanya diatur secara logis agar tidak saling bercampur dan harus melewati router bila ingin saling berkirim data.

---

## B. Tugas Tambahan: Standar Protokol & Teknologi Jaringan

### A. Soal Penugasan
1. Mencatat tentang kabel UTP cat 1-9.
2. Standard Wi-Fi yang ada kemudian cari tahu berapa a/b/g/n-nya.
3. Mencari detail sejarah dan timeline internet.
4. Menginterpretasikan detail internet yang muncul pada fast.com.

---

### B. Jawaban Penugasan

#### 1. Kategori Kabel UTP (Cat 1 sampai Cat 9)
Kabel *twisted-pair* dirancang berdasarkan batas frekuensi dan laju data yang dapat dilewatkan. Berikut rincian tiap kategorinya:

1. **Cat 1:** Bandwidth < 1 MHz, kecepatan hingga 1 Mbps. Digunakan untuk komunikasi suara analog (telepon klasik).
2. **Cat 2:** Bandwidth 4 MHz, kecepatan hingga 4 Mbps. Digunakan untuk sistem terminal awal dan jaringan Token Ring dasar.
3. **Cat 3:** Bandwidth 16 MHz, kecepatan hingga 10 Mbps (standar awal 10BASE-T Ethernet).
4. **Cat 4:** Bandwidth 20 MHz, kecepatan hingga 16 Mbps. Digunakan pada jaringan Token Ring 16 Mbps.
5. **Cat 5:** Bandwidth 100 MHz, kecepatan hingga 100 Mbps (Fast Ethernet 100BASE-TX).
6. **Cat 5e (Enhanced):** Bandwidth 100 MHz, kecepatan hingga 1 Gbps (1000BASE-T Gigabit Ethernet) dengan pengurangan crosstalk yang lebih baik.
7. **Cat 6:** Bandwidth 250 MHz, kecepatan hingga 1 Gbps (mendukung 10 Gbps hingga jarak terbatas $\pm$37–55 meter).
8. **Cat 6a (Augmented):** Bandwidth 500 MHz, kecepatan hingga 10 Gbps secara penuh hingga jarak 100 meter.
9. **Cat 7:** Bandwidth 600 MHz, kecepatan hingga 10 Gbps (pada praktiknya menggunakan pelindung *shielded individual*/S-FTP, bukan UTP murni).
10. **Cat 8:** Bandwidth 2000 MHz (2 GHz), kecepatan 25 Gbps hingga 40 Gbps untuk jarak pendek (hingga 30 meter di pusat data, umumnya berpelindung *shielded*).
11. **Cat 9:** Belum diakui secara resmi oleh badan standardisasi resmi (seperti TIA/EIA atau ISO/IEC). Istilah ini biasanya hanya penamaan pemasaran untuk kabel eksperimental di atas Cat 8.

---

#### 2. Standar Wi-Fi dan Keluarga IEEE 802.11 (a/b/g/n/ac/ax/be)

| Standar Wi-Fi | Generasi | Frekuensi | Kecepatan Puncak Teoretis | Modulasi / Teknologi Kunci |
| :--- | :--- | :--- | :--- | :--- |
| **802.11b** | Wi-Fi 1 | 2.4 GHz | 11 Mbps | DSSS, CCK |
| **802.11a** | Wi-Fi 2 | 5 GHz | 54 Mbps | OFDM |
| **802.11g** | Wi-Fi 3 | 2.4 GHz | 54 Mbps | OFDM, DSSS |
| **802.11n** | Wi-Fi 4 | 2.4 GHz & 5 GHz | Hingga 600 Mbps | MIMO, Channel Bonding (40 MHz) |
| **802.11ac** | Wi-Fi 5 | Khusus 5 GHz | Hingga 6.9 Gbps | 256-QAM, MU-MIMO (downlink), kanal 80/160 MHz |
| **802.11ax** | Wi-Fi 6 / 6E | 2.4 GHz, 5 GHz, 6 GHz (6E) | Hingga 9.6 Gbps | 1024-QAM, OFDMA, TWT |
| **802.11be** | Wi-Fi 7 | 2.4 GHz, 5 GHz, 6 GHz | Hingga 46 Gbps | 4096-QAM, MLO (*Multi-Link Operation*), kanal 320 MHz |

---

#### 3. Detail Sejarah dan Garis Waktu (*Timeline*) Internet
Internet berkembang dari proyek riset komunikasi paket menjadi interkoneksi global yang terdistribusi:

1. **1960-an (Awal Mula Pengiriman Data Berbasis Paket)**  
   Muncul ide untuk memecah data menjadi potongan-potongan kecil agar saluran komunikasi bisa dipakai bersama secara bergantian, tidak dimonopoli oleh satu panggilan seperti pada jaringan telepon lama.
2. **1969 (Uji Coba Jaringan ARPANET)**  
   ARPANET mulai berjalan dengan menghubungkan empat lokasi komputer pertama di Amerika Serikat untuk menguji pengiriman data jarak jauh antar-perangkat yang berbeda.
3. **1970-an (Penyusunan Aturan Komunikasi TCP/IP)**  
   Vinton Cerf dan Robert Kahn merancang aturan dasar komunikasi (protokol) agar berbagai jaringan yang berbeda sistem bisa saling memahami dan bertukar informasi.
4. **1 Januari 1983 (Kelahiran Internet Modern)**  
   ARPANET resmi beralih menggunakan aturan standar TCP/IP secara serentak, momen ini dianggap sebagai awal mula berdirinya Internet modern.
5. **1984 (Sistem Nama Domain / DNS)**  
   Sistem penamaan DNS mulai diterapkan agar pengguna cukup mengingat nama situs (seperti alamat web) alih-alih menghafal deretan angka alamat komputer.
6. **1989–1991 (Penemuan World Wide Web)**  
   Tim Berners-Lee menciptakan Web (URL, HTTP, dan halaman web) di laboratorium CERN, inovasi ini membuat informasi mudah ditelusuri dan menjadi aplikasi populer yang berjalan di atas jaringan Internet.
7. **1990-an (Internet Terbuka untuk Umum)**  
   Penggunaan Internet tidak lagi terbatas pada lingkungan militer atau riset kampus, melainkan mulai dibuka bebas untuk bisnis dan masyarakat luas.
8. **2000-an (Era Internet Cepat dan Nirkabel)**  
   Sambungan kabel berkecepatan tinggi (*broadband*) serta Wi-Fi mulai umum digunakan, membuat orang bisa terhubung ke Internet tanpa repot menyambung kabel telepon.
9. **2010-an (Era Ponsel Pintar dan Layanan Awan)**  
   Penggunaan Internet melonjak tajam karena hadirnya ponsel pintar, media sosial, penyimpanan online (*cloud*), dan perangkat pintar yang terhubung ke jaringan.
10. **2020-an (Peningkatan Kinerja dan Jangkauan Baru)**  
    Teknologi jaringan disempurnakan agar transmisi lebih cepat dan aman, jangkauan diperluas lewat satelit orbit rendah, serta pengelolaan jaringan mulai dibantu sistem otomatis.

---

#### 4. Interpretasi Metrik pada Fast.com
Fast.com mengukur metrik kinerja jaringan pada lapisan transportasi dan aplikasi sebagai berikut:

1. **Download speed:**  
   Mengukur *throughput* unduhan aktual, yaitu laju perpindahan data yang berhasil diterima perangkat dari server pengujian (dinyatakan dalam Mbps atau Gbps), bukan sekadar kapasitas fisik tautan (*bandwidth*).
2. **Upload speed:**  
   Mengukur *throughput* unggahan aktual, yaitu laju data yang berhasil dikirim dari perangkat pengguna kembali ke server pengujian.
3. **Latency (Unloaded & Loaded):**  
   - **Latency Unloaded:** Mengukur *Round-Trip Time* (RTT) atau waktu perjalanan pergi-pulang paket ketika kondisi jaringan sedang tenang tanpa adanya beban lalu lintas data lain, yang utamanya mencerminkan *propagation delay* dan waktu pemrosesan normal.
   - **Latency Loaded:** Mengukur RTT ketika jaringan sedang aktif melakukan transfer data besar secara simultan; kenaikan nilai ini menunjukkan adanya penambahan waktu antrean (*queuing delay*) pada buffer perangkat perantara (*bufferbloat*).
4. **Client info (IP & ISP):**  
   Menunjukkan alamat IP publik perangkat di sisi *network edge* serta penyelenggara jasa Internet (ISP) yang menyediakan jaringan akses menuju *network core*.
5. **Server location:**  
   Menunjukkan lokasi geografis atau titik server penyedia pengujian tempat data dipertukarkan, yang berpengaruh langsung terhadap jarak tempuh sinyal (*propagation delay*).

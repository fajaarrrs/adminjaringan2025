**Nama** : Muhammad Fajar Siddiq  
**Kelas** : D4 Teknik Informatika A  
**NRP** : 3123600004  
**Judul** : Rangkuman Sistem Kerja Email (User A ke User B)  

#  Rangkuman Lengkap Sistem Kerja Email

##  Pendahuluan

Email adalah salah satu cara komunikasi digital paling populer. Meskipun terlihat simpel saat kita klik "Send", sebenarnya ada proses kompleks yang melibatkan banyak komponen di balik layar. Proses ini memastikan pesan kita bisa dikirim, diterima, dan dibaca oleh orang yang tepat.

---

##  Komponen-Komponen Utama

### 1. User Agent (UA)
Antarmuka tempat pengguna menulis dan membaca email, seperti Gmail atau Outlook. Fungsinya:
- Mengirim dan menerima email
- Menyimpan draft, kontak, dan folder

### 2. Spool
Tempat penampungan email yang sedang menunggu giliran untuk dikirim. Email yang kita kirim masuk ke sini dulu.

### 3. Alias Expander
Komponen yang bertugas memeriksa apakah alamat email tujuan adalah alias (misalnya grup), lalu menggantinya dengan daftar alamat asli.

### 4. Database
Menyimpan informasi penting seperti:
- Data pengguna
- Data alias dan grup
- Informasi routing (jalur pengiriman)

### 5. Mail Transfer Agent (MTA)
Bagian yang benar-benar mengirim email:
- **Client MTA**: mengirim email keluar
- **Server MTA**: menerima email yang masuk

### 6. Internet
Jalur komunikasi utama. Email berpindah dari satu server ke server lain melalui protokol internet.

### 7. Mailboxes
Tempat email yang sudah sampai disimpan untuk dibaca oleh penerima.

---

##  Alur Lengkap Email dari User A ke User B

1. **User A** menulis email di Gmail/Outlook → klik Send.
2. Email masuk ke **Spool** untuk antrian pengiriman.
3. **Alias Expander** memeriksa apakah alamat penerima adalah grup.
4. Jika ya, data diperiksa di **Database** dan alamat diubah ke alamat asli.
5. Email diteruskan ke **Client MTA**, lalu dikirim lewat **Internet**.
6. **Server MTA** User B menerima email.
7. Jika diperlukan, **Alias Expander** dan **Database** dipanggil ulang.
8. Email masuk ke **Mailboxes**.
9. **User B** membuka email melalui aplikasi UA.

---

##  Catatan Tambahan

- Protokol yang digunakan: **SMTP** untuk pengiriman, **POP3/IMAP** untuk penerimaan.
- Email bisa gagal terkirim dan dikembalikan ke pengirim (bounce).
- Sistem autentikasi dan enkripsi penting untuk keamanan.
- Spool membantu manajemen trafik pengiriman email.

---

##  Contoh Studi Kasus Mini

Misalnya Fajar kirim email ke `dosen@if.com`. 
- `dosen@if.com` ternyata alias grup.
- **Alias Expander** mencari daftar anggota grup di **Database**.
- Email dikirim satu per satu ke anggota grup via **MTA**.
- Jika salah satu alamat tidak valid, sistem akan mengembalikan notifikasi ke Fajar.

---

##  Kesimpulan

Walaupun email terlihat mudah digunakan, sistem di baliknya cukup kompleks dan melibatkan banyak komponen yang bekerja sama. Dengan memahami proses ini, kita jadi lebih mengerti bagaimana data dikirim secara digital, pentingnya protokol jaringan, serta bagaimana keamanan dan efisiensi komunikasi tetap terjaga.

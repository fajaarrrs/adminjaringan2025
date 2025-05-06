**Nama** : Muhammad Fajar Siddiq  
**Kelas** : D4 Teknik Informatika A  
**NRP** : 3123600004  
**Judul** : Rangkuman Sistem Kerja Email (User A ke User B)  

# Rangkuman Sistem Kerja Email

Gambar ini ngejelasin gimana sih alur kerja email dari satu pengguna (User A) ke pengguna lain (User B). Jadi, waktu kita kirim email, ternyata ada banyak komponen yang kerja di belakang layar biar email bisa nyampe dengan lancar.

---

## Komponen yang Terlibat

| Komponen            | Penjelasan Singkat |
|---------------------|--------------------|
| **User Agent (UA)** | Aplikasi yang kita pake buat baca & kirim email (kayak Gmail, Outlook, dsb). |
| **Spool**           | Tempat nunggu email yang siap dikirim. |
| **Mailboxes**       | Tempat nyimpan email yang udah masuk. |
| **Alias Expander**  | Buat nyari alamat tujuan sebenarnya dari alias (nama pendek atau grup). |
| **Database**        | Tempat nyimpen data alias & alamat tujuan. |
| **MTA (Mail Transfer Agent)** | Yang ngurus pengiriman email antar server. Ada dua jenis: <br>• **Client MTA**: ngirim email keluar <br>• **Server MTA**: nerima email masuk |
| **Internet**        | Jalur utama buat kirim email dari satu server ke server lain. |

---

##  Alur Email dari User A ke User B

1. **User A** nulis email di aplikasi (UA).
2. Email disimpen dulu di **Spool**, terus dikirim ke **Alias Expander**.
3. **Alias Expander** cari alamat asli email tujuan lewat **Database**.
4. Email dikirim keluar lewat **MTA Client** ke jaringan **Internet**.
5. Di sisi **User B**, **MTA Server** nerima email dari Internet.
6. Email dicek lagi sama **Alias Expander**, terus disimpen di **Mailboxes**.
7. Akhirnya, **User B** bisa buka email itu lewat aplikasinya (UA).

---

##  Kesimpulan

Jadi, waktu kita kirim email, ada banyak proses dan sistem yang kerja supaya pesan kita bisa nyampe ke penerima dengan aman dan cepat. Gak cuma kirim langsung, tapi lewat sistem ekspansi alamat, antrian email, dan transfer lewat server-server.

---

##  Catatan Tambahan

- Sistem ini biasanya dipakai di email server beneran yang pakai protokol kayak **SMTP**, **POP3**, atau **IMAP**.
- Alias itu kayak shortcut atau nama grup email yang bisa dikirim ke banyak orang sekaligus.

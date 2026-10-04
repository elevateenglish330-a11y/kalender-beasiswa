# Kalender Beasiswa

Kalender tenggat beasiswa luar negeri untuk pelamar Indonesia. Situs statis, gratis selamanya di GitHub Pages.

## Isi folder

| File | Fungsi |
|---|---|
| `index.html` | Seluruh halaman. Jarang perlu disentuh. |
| `data.json` | **Satu-satunya file yang kamu update rutin.** Semua beasiswa ada di sini. |
| `.nojekyll` | Mematikan pemrosesan Jekyll di GitHub Pages. Biarkan saja. |
| `README.md` | File ini. Tidak tampil di situs. |

## Cara menerbitkan pertama kali

1. Pakai akun GitHub yang terpisah dari akun risetmu (R1-AK). Jangan pernah mendorong repo bisnis ke sana.
2. **Rapikan username dulu, sebelum repo dibuat.** Username masuk ke alamat situs dan tampil di setiap link yang kamu bagikan. Akhiran acak seperti `-a11y` yang disarankan GitHub membuat alamatnya terbaca seperti akun asal jadi. Ganti di Settings, Account, Change username. Gratis. Lakukan sekarang, karena setelah link tersebar penggantian akan merusak semua link lama.
3. Buat repository baru bernama `kalender-beasiswa`. Set **Public**. Jangan centang "Add a README".
4. Di halaman repo kosong itu, klik **uploading an existing file**. Seret keempat file dari folder ini. Klik **Commit changes**.
5. Masuk ke **Settings**, menu kiri **Pages**. Di bagian Source pilih **Deploy from a branch**, Branch `main`, folder `/ (root)`. Klik **Save**.
6. Tunggu satu sampai dua menit. Alamatnya jadi:

   ```
   https://<username>.github.io/kalender-beasiswa/
   ```

7. Buka alamat itu. Kalau masih 404, tunggu semenit lagi dan refresh.

## Cara update isi kalender

Jangan mengetik JSON dengan tangan. Satu koma salah dan seluruh halaman kosong.

1. Buka situsmu dengan menambahkan `#edit` di belakang alamatnya:

   ```
   https://<username>.github.io/kalender-beasiswa/#edit
   ```

   Simpan alamat ini sebagai bookmark. Pengunjung biasa tidak melihat tombol edit apa pun.

2. Klik **Edit kalender**. Ubah, tambah, atau hapus beasiswa lewat formulir.
3. Klik **Salin data.json**. Seluruh data tersalin ke clipboard.
4. Buka repo GitHub, klik file `data.json`, klik ikon pensil di kanan atas.
5. Pilih semua isi file (Ctrl+A), tempel (Ctrl+V), lalu **Commit changes**.
6. Tunggu sekitar satu menit. Situs terbit ulang otomatis.

Kalau clipboard gagal, tombol **Unduh** memberi file `data.json` yang bisa kamu unggah menggantikan yang lama di repo.

## Soal label Perkiraan

Setiap beasiswa punya penanda `pasti`:

- `"pasti": true` berarti tanggalnya sudah diumumkan resmi oleh penyelenggara.
- `"pasti": false` memunculkan label **Perkiraan** di halaman.

Isi `false` untuk apa pun yang belum diumumkan. Kredibilitas halaman ini bergantung pada pembaca bisa membedakan mana yang pasti dan mana yang tebakan. Satu orang yang kelewatan deadline karena percaya tanggal karangan akan merusak reputasimu lebih lama daripada manfaat sepuluh orang yang terbantu.

Field `presisi` mengatur tampilan tanggal: `"hari"` menampilkan tanggal penuh, `"bulan"` hanya menampilkan bulan dan tahun.

## Yang masih perlu kamu kerjakan

- **Isi nomor WhatsApp.** Buka mode edit, klik **Kontak**. Selama kosong, halaman ini tidak punya jalur menghubungi siapa pun.
- **Verifikasi Gates Cambridge dan Clarendon.** Dua entri itu ditandai BELUM DIVERIFIKASI di catatannya. Tanggalnya mengikuti deadline kursus per departemen, bukan satu tanggal tunggal.
- **Jangan tambahkan angka IPK atau batas usia ke LPDP** sampai buku panduan 2027 terbit.

## Domain sendiri (opsional, nanti)

Domain `.my.id` sekitar Rp 50 sampai 100 ribu per tahun di registrar lokal. Setelah beli:

1. Di DNS registrar, buat 4 record A ke `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
2. Di repo, Settings, Pages, isi Custom domain, lalu centang Enforce HTTPS.

Hosting tetap gratis. Yang kamu bayar hanya nama domainnya.

## Catatan jujur soal SEO

Kalender sepuluh baris tidak akan mengalahkan Kobi atau Schoters di hasil pencarian. Mereka punya ratusan artikel yang sudah bertahun-tahun terindeks. Nilai nyata memindahkan ini ke domain sendiri ada di tiga hal: link yang kamu miliki sendiri, pratinjau yang rapi saat dibagikan di WhatsApp, dan fondasi kalau suatu saat kamu benar-benar menulis artikel per beasiswa. Peringkat pencarian datang dari tulisan, bukan dari tabel tanggal.

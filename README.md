# Website JO Interior — Siap Hosting

Website statis (HTML, CSS, dan JavaScript murni). Tidak butuh database, PHP, atau Node.js. Cukup unggah **semua isi folder ini** ke hosting.

## Isi folder

| File / Folder | Fungsi |
|---|---|
| `index.html` | Halaman utama website |
| `lang.js` | Kamus Bahasa Inggris. Ubah terjemahan di sini |
| `images/` | Logo dan 32 foto proyek (format WebP) |
| `404.html` | Halaman "tidak ditemukan" |
| `.htaccess` | Pengaturan untuk Hostinger / IDwebhost / cPanel |
| `.nojekyll` | Pengaturan untuk GitHub Pages |
| `robots.txt` | Izin agar Google bisa mengindeks website |

> File `.htaccess` dan `.nojekyll` diawali titik, jadi mungkin tersembunyi di Windows Explorer. Aktifkan **View → Hidden items** agar terlihat dan ikut terunggah.

## Pilihan bahasa

- Tombol **ID / EN** ada di kanan atas. Pilihan pengunjung diingat di browsernya.
- Link khusus Bahasa Inggris: `https://domainanda.com/?lang=en`
- Untuk mengubah terjemahan, buka `lang.js`. Teks kiri adalah Bahasa Indonesia, teks kanan adalah Bahasa Inggris.

---

## Cara 1 — Hostinger

1. Login ke **hPanel** → **Websites** → pilih domain → **File Manager**.
2. Buka folder **`public_html`**. Hapus file bawaan seperti `default.php` bila ada.
3. Klik **Upload**, lalu unggah semua isi folder `Deploy` (bukan foldernya). Hasilnya: `public_html/index.html`, `public_html/images/...`, dan seterusnya.
   - Lebih cepat: kompres isi folder jadi `.zip`, unggah, lalu klik kanan → **Extract**.
4. Aktifkan SSL: hPanel → **Security → SSL** → Install.
5. Buka domain Anda di browser.

## Cara 2 — IDwebhost / Niagahoster / hosting cPanel lain

1. Login ke **cPanel** → **File Manager** → buka **`public_html`**.
2. **Upload** file `.zip` berisi semua isi folder `Deploy`, lalu klik kanan → **Extract**.
3. Pastikan `index.html` berada langsung di dalam `public_html`, bukan di `public_html/Deploy/`.
4. Aktifkan SSL lewat **SSL/TLS Status** atau **AutoSSL**.

## Cara 3 — GitHub Pages (gratis)

1. Buat repository baru di GitHub, misalnya `jo-interior`.
2. Klik **Add file → Upload files**, lalu seret semua isi folder `Deploy`. Klik **Commit changes**.
3. Buka **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → **Save**.
4. Tunggu 1–2 menit. Website tampil di `https://NAMA-AKUN.github.io/jo-interior/`.
5. Domain sendiri (opsional): isi **Custom domain** di halaman yang sama, lalu arahkan DNS domain ke GitHub sesuai petunjuknya.

## Cara 4 — Netlify (gratis, paling cepat)

Buka https://app.netlify.com/drop, lalu seret folder `Deploy` ke halaman itu. Selesai.

---

## Setelah online (disarankan)

1. **Gambar saat link dibagikan (WhatsApp, Facebook):** di `index.html`, ganti
   `<meta property="og:image" content="images/og-image.jpg">`
   menjadi alamat lengkap, misalnya `content="https://domainanda.com/images/og-image.jpg"`.
2. **HTTPS otomatis (Hostinger/cPanel):** buka `.htaccess`, lalu hapus tanda `#` di 3 baris "Paksa HTTPS" setelah SSL aktif.
3. **Daftarkan ke Google:** tambahkan domain di https://search.google.com/search-console.

## Mengganti foto atau teks

- **Foto:** ganti file di `images/` dengan nama yang sama.
- **Teks Bahasa Indonesia:** ubah di `index.html`.
- **Teks Bahasa Inggris:** ubah di `lang.js`.

Bila teks Indonesia di `index.html` diubah, ubah juga kunci yang sama (teks sebelah kiri) di `lang.js`. Kalau tidak, versi Inggris akan menampilkan teks Indonesia untuk bagian itu.

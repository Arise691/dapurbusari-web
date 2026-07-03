# Dapur Bu Sari — Template Landing Page UMKM

Template landing page khusus UMKM (contoh: kuliner rumahan), fokus ke **pemesanan
lewat WhatsApp**, bukan form kontak formal. Cocok dijadikan starting point buat
tiap klien jasa website-mu — tinggal ganti isi & warna.

## Struktur

```
dapurbusari/
├── index.html
├── style.css
├── script.js
├── manifest.json
├── service-worker.js
└── assets/icons/
```

## Cara pakai buat klien baru (checklist ganti konten)

1. **Nomor WhatsApp** — cari-ganti semua `6281234567890` di `index.html` jadi
   nomor WA klien (pakai format `62` tanpa angka 0 di depan, tanpa spasi/strip).
2. **Nama usaha & logo** — ganti "Dapur Bu Sari" di semua tempat (title, brand,
   footer), dan ganti SVG logo sederhana di navbar/footer sesuai usaha klien.
3. **Menu/produk** — edit bagian `<section id="menu">`, ganti nama produk,
   deskripsi, harga, dan warna gradient tiap `.menu-thumb`.
4. **Cerita "Tentang"** — ganti narasi di `<section id="tentang">` sesuai
   cerita usaha klien.
5. **Testimoni** — ganti isi `.note-card` dengan testimoni asli klien (kalau
   belum ada, bisa dikosongkan dulu section-nya).
6. **Lokasi & jam buka** — edit `<section id="lokasi">`.
7. **Warna brand** (opsional) — kalau klien punya warna khas usaha, ganti
   4 variabel warna di baris atas `style.css`:
   `--wine`, `--marigold`, `--sage`, `--cream`.
8. **Ikon** — generate ulang ikon PWA dengan warna baru kalau perlu (atau pakai
   logo asli klien kalau ada).

## Deploy

Sama seperti Orbitly sebelumnya — upload ke GitHub, aktifkan GitHub Pages di
Settings → Pages, pilih branch `main`, folder root. Tidak perlu perbaikan path
tambahan karena semua path di sini **sudah relatif dari awal**.

## Kenapa beda dari Orbitly

- Tidak ada login/dashboard — UMKM biasanya tidak butuh itu, cuma butuh
  "kartu nama digital" yang meyakinkan + jalur pemesanan cepat.
- CTA utama adalah tombol WhatsApp (mengambang + di banyak tempat), karena
  itu cara UMKM Indonesia biasa terima order.
- Desain hangat (bukan dark mode SaaS) supaya terasa personal dan related
  ke usaha rumahan/lokal, bukan produk teknologi.

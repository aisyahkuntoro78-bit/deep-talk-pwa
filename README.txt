# DEEP TALK. — PWA

Paket ini mempertahankan `index.html` dan `capybara.webp` dari file yang diberikan, lalu menambahkan dukungan Progressive Web App.

## Isi
- `index.html` — halaman dan mekanisme permainan asli, ditambah tautan manifest dan registrasi service worker.
- `capybara.webp` — maskot asli.
- `manifest.json` — metadata instalasi aplikasi.
- `sw.js` — cache app shell agar halaman dapat dibuka kembali saat offline setelah kunjungan pertama.
- `icons/` — ikon aplikasi 192px dan 512px yang dibuat dari maskot.

## Deploy ke Vercel
Unggah/commit seluruh isi folder ini ke root project `deep-talk-game`, lalu lakukan deployment baru. Jangan hanya mengunggah `index.html`; semua file dan folder harus ikut.

Setelah deployment:
1. Buka domain HTTPS project.
2. Pastikan `/manifest.json`, `/sw.js`, dan `/capybara.webp` dapat dibuka.
3. Di Android Chrome, buka menu browser lalu pilih **Install app** atau **Add to Home screen**.

Catatan: service worker dan instalasi PWA memerlukan HTTPS (Vercel sudah menyediakannya). Cache offline mencakup app shell dan aset lokal; font serta aset pihak ketiga tetap memerlukan internet jika belum tersimpan browser.

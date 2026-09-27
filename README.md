# VIPT CUP IV 2026 — Mobile Sports Game

Game mobile turnamen olahraga antar-RT. **Sport • Friendship • Together**

Status build: **TAHAP 1 / 5** — Struktur project, navigasi, dan layar-layar utama sebelum gameplay.

---

## Yang sudah selesai di TAHAP 1

- Struktur folder lengkap
- Splash Screen (logo asli + animasi)
- Home (profil pemain, menu olahraga, bottom navigation)
- Pilih Olahraga (Badminton aktif, Voli & Futsal terkunci)
- Pilih Tim (RT 08–RT 13, RT 08 default)
- Pilih Pemain (roster RT 08 lengkap dengan stats)
- Persiapan Pertandingan (VS screen + roster)
- Sistem localStorage (progress tidak hilang saat refresh)
- Mode DEBUG_MODE (tombol RESET DATA muncul di kanan atas)

Belum dibuat (menyusul di tahap berikutnya): gameplay badminton, hasil pertandingan, road to champion, champion screen, profil pemain, hadiah, ranking penuh, PWA (manifest/service worker penuh), audio, polish akhir.

---

## Cara memasukkan asset LOGO VIPT CUP

1. Simpan file logo resmi (PNG, background transparan jika ada) dengan nama persis:
   ```
   assets/images/vipt-cup-logo.png
   ```
2. Logo ini otomatis dipakai di Splash Screen, Home, dan favicon.
3. **Jangan** mengubah bentuk, warna, atau tulisan logo — cukup timpa file dengan logo asli Anda.

Logo yang Anda upload sudah disalin ke path tersebut oleh Claude.

## Cara memasukkan asset ARENA VIPT

1. Foto lapangan asli disimpan sebagai referensi di:
   ```
   assets/images/arena-reference.jpg
   ```
2. Asset arena versi *game* (2.5D/CSS/Canvas) akan dibangun di TAHAP 2 saat gameplay badminton dibuat, menggunakan foto ini sebagai acuan warna & bentuk (lantai orange, perimeter biru, garis putih, pagar, gawang, tribun, banner).

---

## Menjalankan secara lokal

Karena semua path bersifat *relative* dan tidak butuh backend, cukup buka `index.html` langsung di browser, atau gunakan live server sederhana (opsional, hanya untuk kenyamanan development):

```bash
npx serve .
```

---

## Cara menjalankan di GitHub

1. Buat repository baru di GitHub, misalnya `vipt-cup-iv-2026`.
2. Upload seluruh isi folder project ini (jangan upload folder pembungkus tambahan — `index.html` harus berada di root repo).
3. Commit & push ke branch `main`.

## Cara mengaktifkan GitHub Pages

1. Buka repository di GitHub.
2. Masuk ke **Settings → Pages**.
3. Pada **Build and deployment**, pilih **Deploy from a branch**.
4. Pilih branch `main` dan folder `/root`.
5. Klik **Save**.
6. Tunggu beberapa menit, lalu game akan LIVE di:
   ```
   https://<username>.github.io/<nama-repo>/
   ```

---

## Struktur folder

```
/
├── index.html
├── README.md
├── manifest.json
├── assets/
│   ├── images/
│   │   ├── vipt-cup-logo.png
│   │   ├── arena-reference.jpg
│   │   ├── background/
│   │   ├── teams/
│   │   └── players/
│   ├── icons/
│   └── audio/
├── css/
│   ├── style.css
│   └── menu.css
└── js/
    ├── app.js
    ├── data.js
    ├── navigation.js
    ├── storage.js
    └── ui.js
```

## Dependency

Tidak ada dependency eksternal selain Google Fonts (Rajdhani + Inter) yang dimuat via CDN. Semua logika game murni HTML5 + CSS3 + JavaScript vanilla — 100% kompatibel dengan GitHub Pages tanpa backend.

---

Ketik **"NEXT TAHAP 2"** untuk melanjutkan ke gameplay Badminton (arena, pemain, shuttlecock, AI, dan skor).

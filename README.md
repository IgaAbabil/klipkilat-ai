# 🎬 KlipKilat AI — Pemotong Klip Video Otomatis (15, 30 & 60 Detik)

Aplikasi web berbasis HTML5 Single-File untuk mengubah video panjang (YouTube maupun file video lokal **MP4/MOV/WebM**) menjadi klip vertikal viral siap unggah ke **TikTok, YouTube Shorts, dan Instagram Reels** — tanpa perlu proses *build* atau instalasi dependensi rumit.

---

## ✨ Fitur Utama

- **Input Link YouTube & Upload Video Asli (MP4/MOV/WebM):** Mendukung berbagai format tautan YouTube maupun unggah file lokal langsung (*drag & drop* atau klik tombol pilih file).
- **Generator Klip Otomatis 15, 30 & 60 Detik:** Mendeteksi segmen terbaik lengkap dengan skor viralitas, judul *hook*, dan alasan retensi penonton.
- **3 Mode Rasio Aspek Studio:**
  - `📱 9:16 Crop` — Potong vertikal penuh dengan pelacak pembicara.
  - `🖼️ 9:16 Full+BG` — Menampilkan video utuh 100% tanpa terpotong dengan latar belakang potret blur sinematik.
  - `🖥️ 16:9` — Rasio asli layar lebar.
- **AI Auto-Reframe & Editor Framing Manual:** Kamera otomatis mengikuti pembicara aktif atau geser/zoom manual langsung pada layar pratinjau.
- **Subtitle TikTok Sesuai Suara & Editor Timestamp:** Transkripsi otomatis sesuai ucapan asli pembicara (Audio AI / Live Speech-to-Text), dapat diedit per baris, serta diekspor ke `.SRT`.
- **Unduh Video 1-Klik + Pratinjau Hasil:** Merender video HD beserta audio dan subtitle tertanam langsung di browser.

---

## 📁 Struktur Repositori GitHub

Cukup unggah dua file berikut ke repositori GitHub Anda:

```text
klipkilat-ai/
├── index.html      # Aplikasi web utama (HTML + Tailwind + JavaScript lengkap)
└── README.md       # Dokumentasi proyek & panduan menjalankan lokal
```

---

## 💻 Cara Menjalankan di Komputer Lokal

Karena aplikasi ini tidak membutuhkan *bundler* (`npm install` / Webpack / Vite), Anda bisa langsung menjalankannya menggunakan salah satu cara di bawah ini:

### Cara 1: Menggunakan VS Code Live Server (Paling Mudah)
1. Buka folder proyek `klipkilat-ai` di **Visual Studio Code**.
2. Pasang ekstensi **Live Server** (oleh Ritwick Dey).
3. Klik kanan pada `index.html` lalu pilih **Open with Live Server**.
4. Browser akan terbuka otomatis di `http://127.0.0.1:5500`.

### Cara 2: Menggunakan Python (Bawaan macOS / Linux / Windows)
Buka terminal di dalam folder proyek, lalu jalankan:
```bash
python -m http.server 8000
```
Buka browser dan kunjungi: **`http://localhost:8000`**

### Cara 3: Menggunakan Node.js (`npx serve`)
Buka terminal di dalam folder proyek, lalu jalankan:
```bash
npx serve .
```
Buka alamat `http://localhost:3000` yang muncul di terminal.

> **Catatan:** Menjalankan lewat `http://localhost` sangat disarankan agar pemutar embed **YouTube IFrame API** berjalan penuh tanpa pembatasan protokol `file://`.

---

## 🚀 Cara Upload ke GitHub & Hosting Gratis (GitHub Pages)

1. **Buat Repositori Baru di GitHub:**
   - Masuk ke [github.com](https://github.com) &rarr; klik **New Repository** (misalnya bernama `klipkilat-ai`).
2. **Upload File ke GitHub:**
   - Lewat web GitHub: Klik **Add file &rarr; Upload files**, seret `index.html` dan `README.md`, lalu klik **Commit changes**.
   - Atau lewat Git CLI:
     ```bash
     git init
     git add index.html README.md
     git commit -m "Initial commit: KlipKilat AI Video Clipper"
     git branch -M main
     git remote add origin https://github.com/USERNAME_ANDA/klipkilat-ai.git
     git push -u origin main
     ```
3. **Aktifkan GitHub Pages (Opsional — Agar Bisa Diakses Online):**
   - Buka tab **Settings &rarr; Pages** di repositori GitHub Anda.
   - Pada bagian **Build and deployment &rarr; Branch**, pilih `main` dan folder `/ (root)`, lalu klik **Save**.
   - Dalam 1–2 menit, aplikasi Anda langsung aktif online di `https://USERNAME_ANDA.github.io/klipkilat-ai/`.

---

## 🔑 Pengaturan Gemini API Key (Opsional)

- Tanpa API Key pun aplikasi tetap berfungsi penuh menggunakan **Smart AI Engine** bawaan.
- Jika ingin menggunakan analisis AI & transkrip audio berbasis Google Gemini secara penuh, klik tombol **🔑 API Key** di pojok kanan atas aplikasi dan masukkan kunci dari [Google AI Studio](https://aistudio.google.com/) (disimpan aman di `localStorage` browser Anda sendiri, tidak pernah dikirim ke server pihak ketiga).
# 🎓 SMK Nusantara Teknologi — Website Profil Sekolah

Website profil sekolah SMK modern berbasis teknologi dan industri. Dibangun dengan **HTML murni**, **TailwindCSS CDN**, dan **Vanilla JavaScript** — tanpa framework tambahan, langsung siap jalan di browser.

![SMK Nusantara Teknologi](https://images.unsplash.com/photo-1571260899304-425eee4c7efc?w=1200&q=80)

---

## 📁 Struktur File

```
📦 smk-nusantara-teknologi/
├── index.html      # Halaman utama (landing page)
├── post.html       # Halaman daftar berita & pengumuman
└── README.md
```

---

## 🗂️ Halaman & Section

### `index.html` — Landing Page Utama

| # | Section | ID | Keterangan |
|---|---|---|---|
| 1 | **Navbar** | — | Fixed navbar responsif; menu **Tentang** dengan dropdown 6 item; hamburger accordion mobile |
| 2 | **Hero** | `#home` | Full-screen gradient merah, headline, 2 CTA button, quick stats sekolah |
| 3 | **Kenapa Kami** | `#kenapa` | 4 kartu keunggulan sekolah |
| 4 | **Tentang** | `#tentang` | Profil sekolah, visi & misi, 4 kartu statistik |
| 5 | **Jurusan** | `#jurusan` | 5 card program keahlian (RPL, TKJ, DKV, Akuntansi, TBSM) |
| 6 | **Fasilitas** | `#fasilitas` | 6 kartu fasilitas bergambar (Lab Komputer, Workshop, Perpustakaan, Studio Multimedia, Aula, WiFi Campus) |
| 7 | **Prestasi** | `#prestasi` | 4 kartu highlight + timeline prestasi terbaru |
| 8 | **PPDB** | `#ppdb` | Jadwal, persyaratan, alur pendaftaran, CTA daftar |
| 9 | **Galeri** | `#galeri` | Responsive image grid kegiatan sekolah |
| 10 | **Testimoni** | `#testimoni` | 3 kartu alumni dengan foto, posisi, rating bintang |
| 11 | **FAQ** | `#faq` | 7 item accordion buka/tutup |
| 12 | **Postingan** | `#postingan` | Preview berita/pengumuman terbaru dengan filter tab |
| 13 | **Mitra Industri** | `#mitra` | 6 kartu mitra utama + marquee logo strip + CTA |
| 14 | **Kontak** | `#kontak` | Form kontak, info alamat, WhatsApp, maps |
| 15 | **Footer** | — | Link navigasi, sosial media, copyright |

**Dropdown Navbar "Tentang"** berisi:
`Tentang Sekolah` · `Jurusan` · `Fasilitas` · `Prestasi` · `Galeri` · `Mitra Industri`

---

### `post.html` — Halaman Berita & Pengumuman

| Fitur | Keterangan |
|---|---|
| **Hero** | Page header gradient merah dengan breadcrumb & quick stats |
| **Search** | Pencarian real-time dengan debounce, tombol clear (×) |
| **Filter Kategori** | Pill button: Semua / Berita / Pengumuman / Kegiatan / Prestasi + counter |
| **Sort** | Urutkan: Terbaru, Terlama, A–Z, Z–A |
| **View Toggle** | Switch tampilan Grid (3 kolom) ↔ List (baris horizontal) |
| **Pagination** | Navigasi cerdas dengan elipsis `···`, 9 post per halaman |
| **Empty State** | Tampilan khusus saat hasil kosong + tombol reset filter |
| **Sidebar — Unggulan** | 3 postingan pilihan dengan thumbnail |
| **Sidebar — Statistik** | Progress bar per kategori |
| **Sidebar — Topik** | 12 tag klik-untuk-filter |
| **Sidebar — Arsip** | Filter per bulan (Jan–Mei 2025) |
| **Sidebar — CTA** | Notifikasi via WhatsApp |
| **Data posts** | 24 postingan dummy (3 Berita, 7 Pengumuman, 9 Kegiatan, 5 Prestasi) |

---

## 🛠️ Teknologi

| Teknologi | Keterangan |
|---|---|
| **HTML5** | Semantic markup, accessible structure |
| **TailwindCSS CDN** | Utility-first, custom theme merah di `tailwind.config` |
| **Vanilla JavaScript** | Tanpa framework, tanpa dependency |
| **Google Fonts** | Montserrat 300–900 |
| **Unsplash** | Placeholder images |
| **Pravatar** | Placeholder avatar foto alumni |

---

## 🎨 Design System

```
Primary Color  : #e01010  (Red 600)
Hover State    : #c00a0a  (Red 700)
Font           : Montserrat
Border Radius  : rounded-xl / rounded-2xl / rounded-3xl
```

**Utility class yang konsisten dipakai di kedua file:**

| Class | Fungsi |
|---|---|
| `.card-hover` | Naik + shadow saat hover |
| `.reveal` / `.reveal-left` / `.reveal-right` | Fade-up animation saat scroll (IntersectionObserver) |
| `.gradient-text` | Teks gradient merah |
| `.nav-link` | Underline animasi saat hover |
| `.stat-card` | Card putih dengan shadow halus |
| Scrollbar custom | Warna merah, lebar 6px |

---

## 🚀 Cara Menjalankan

### Lokal — tanpa server
```
Klik dua kali index.html
```

### Live Server (VS Code)
1. Install ekstensi **Live Server**
2. Klik kanan `index.html` → **Open with Live Server**

### Deploy ke GitHub Pages
1. Push semua file ke repository GitHub
2. Buka **Settings** → **Pages**
3. Source: branch `main`, folder `/ (root)`
4. Klik **Save**
5. Situs aktif di:
   ```
   https://<username>.github.io/<nama-repo>/
   ```

---

## 📱 Responsivitas

| Breakpoint | Tampilan |
|---|---|
| `< 640px` | Mobile — 1 kolom, hamburger menu, accordion Tentang |
| `640px–1023px` | Tablet — 2 kolom grid |
| `1024px+` | Desktop — navbar penuh dengan dropdown |
| `1280px+` | Wide — layout 3 kolom maksimal |

---

## ✏️ Panduan Kustomisasi

### Ganti identitas sekolah
Cari-dan-ganti teks berikut di `index.html`:

| Placeholder | Ganti dengan |
|---|---|
| `SMK Nusantara` | Nama sekolah |
| `Teknologi` | Tagline / jurusan utama |
| `Jl. Pendidikan No. 123...` | Alamat lengkap |
| `info@smknusantara.sch.id` | Email sekolah |
| `(0281) 234-567` | Nomor telepon |
| `0812-3456-7890` | Nomor WhatsApp (tampilan) |
| `6281234567890` | Nomor WA tanpa `+` untuk link `wa.me` |

### Tambah postingan baru (`post.html`)
Tambahkan objek ke array `allPosts` di bagian `<script>`:

```javascript
{
  id: 25,
  title: "Judul Postingan Baru",
  category: "berita",        // berita | pengumuman | kegiatan | prestasi
  date: "2025-06-01",        // YYYY-MM-DD
  month: "Juni 2025",        // untuk filter arsip sidebar
  img: "https://...",        // URL gambar
  excerpt: "Ringkasan singkat.",
  tags: ["RPL", "LKS"],      // opsional
  isNew: true,               // opsional — tampilkan badge "Baru"
}
```

### Ganti warna primary
Edit `tailwind.config` di `<script>` atas kedua file:

```javascript
colors: {
  primary: {
    600: "#e01010",   // warna utama — ubah sesuai identitas sekolah
    700: "#c00a0a",   // hover state
    50:  "#fff1f1",   // background sangat terang
    100: "#ffe1e1",   // background terang
  }
}
```

---

## 📋 Lisensi

Proyek ini dibuat untuk keperluan pendidikan dan dapat digunakan secara bebas.
Silakan modifikasi sesuai kebutuhan sekolah Anda.

---

## 🙌 Kredit

- CSS Framework: [TailwindCSS](https://tailwindcss.com)
- Foto placeholder: [Unsplash](https://unsplash.com)
- Font: [Google Fonts — Montserrat](https://fonts.google.com/specimen/Montserrat)
- Avatar: [Pravatar](https://pravatar.cc)

---

## 🤖 Kolaborasi Kecerdasan Buatan (AI Ecosystem)

Proyek website profil ini dirancang, dioptimalkan, dan disempurnakan melalui kolaborasi lintas ekosistem AI terkemuka. Masing-masing model memberikan kontribusi spesifik untuk menciptakan kode vanilla yang bersih, responsif, dan interaktif:

*   **🧠 Claude (Anthropic):** Bertanggung jawab atas perancangan arsitektur data struktural untuk 24 repositori postingan dummy di `post.html`, manajemen logika pemrograman state kontrol (pencarian, sorting, penanganan elipsis pagination), serta penulisan dokumentasi teknis ini.
*   **💡 ChatGPT (OpenAI):** Bertanggung jawab dalam sesi *brainstorming* ide dasar, merumuskan konsep kreatif, serta menyusun cetak biru (*blueprint*) fitur dan struktur 15 section utama agar sesuai dengan kebutuhan profil sekolah modern.
*   **✨ Gemini (Google):** Mengoptimalisasi estetika visual mikro, mengubah arsitektur layout grid statis menjadi layout dinamis yang aktif, menyuntikkan perilaku interaktif tingkat lanjut menggunakan utility class murni (`group-hover`, transformasi rotasi ikon, transisi elevasi bayangan ekstrem), serta memastikan konsistensi desain sistem warna primer.

Kombinasi dari ketiga AI ini memastikan proyek berjalan ringan tanpa dependensi eksternal, namun memiliki kualitas interaksi visual setara website modern masa kini.
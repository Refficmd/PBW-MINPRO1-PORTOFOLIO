# 🌐 Website Portfolio

Website portfolio pribadi yang dibuat untuk menampilkan profil, keahlian, proyek, sertifikat, dan pengalaman akademik. Project ini dikembangkan menggunakan HTML, CSS, Bootstrap 5, dan Vue.js dengan konsep desain modern (dark theme & glassmorphism).
Project ini dibuat untuk memenuhi tugas praktikum dengan ketentuan dokumentasi README yang menjelaskan setiap section serta teknologi yang digunakan.

---

# 🛠 Teknologi yang Digunakan
| Teknologi       | Keterangan                                |
| --------------- | ----------------------------------------- |
| HTML5           | Struktur utama halaman                    |
| CSS3            | Styling dan desain tampilan               |
| Bootstrap 5     | Layout responsif dan komponen UI          |
| Bootstrap Icons | Ikon pada bagian contact                  |
| Vue.js 3 (CDN)  | Interaktivitas dan pengolahan data        |
| JavaScript      | Logika tambahan (scroll highlight navbar) |

---
## 🖥 Struktur Section & Penjelasan Kode
---

## 1. Navbar

<img width="1899" height="74" alt="image" src="https://github.com/user-attachments/assets/f549e19b-5a8b-4ca2-86b6-24e67bc59c4d" />

Navbar berada pada bagian atas halaman dan tetap terlihat saat scroll (fixec-top). pada navbar terdapat menu: Home, About Portofolio dan Contact

## 💻 Penjelasan Kode

| Bagian           | Potongan Kode                                                               | Fungsi                                               |
| ---------------- | --------------------------------------------------------------------------- | ---------------------------------------------------- |
| Struktur Navbar  | `<nav class="navbar navbar-expand-lg navbar-dark fixed-top custom-navbar">` | Membuat navbar responsif dengan Bootstrap            |
| Toggle Button    | `data-bs-toggle="collapse"`                                                 | Mengatur menu collapse di layar kecil                |
| Nav Link         | `<a class="nav-link" href="#about">About</a>`                               | Navigasi antar section                               |
| Scroll Highlight | `window.addEventListener("scroll", updateActiveNav);`                       | Memberikan efek aktif pada menu sesuai posisi scroll |

Navbar aktif saat scroll dikontrol oleh JavaScript yang membaca posisi section dan menambahkan class .active.

---

## 2. Hero Section

<img width="1898" height="929" alt="image" src="https://github.com/user-attachments/assets/c3007af3-35a5-407f-995a-de06216ff122" />

Bagian Home website dengan efek typing text dan tombol navigasi ke project dan contact.

## 💻 Penjelasan Kode

| Bagian        | Potongan Kode                                         | Fungsi                        |
| ------------- | ----------------------------------------------------- | ----------------------------- |
| Vue Binding   | `{{ typedText }}`                                     | Menampilkan teks dinamis      |
| Data Teks     | `fullText: "Portfolio Website"`                       | Teks yang akan diketik        |
| Typing Effect | `setTimeout(() => this.typeEffect(), 80);`            | Mengatur kecepatan animasi    |
| Gradient Text | `.gradient-text { background: linear-gradient(...) }` | Memberikan efek warna gradasi |

Efek typing dijalankan saat Vue mounted menggunakan method typeEffect().

---

## 3. About Section

<img width="1897" height="927" alt="image" src="https://github.com/user-attachments/assets/b8f6e07a-8f79-4c4b-a2bc-cb20ac4977b6" />

Menampikan:
  - Foto profil
  - Deskripsi
  - Skils (Progress bar)
  - Statistik Pengalaman

## 💻 Penjelasan Kode

| Bagian        | Potongan Kode                                 | Fungsi                               |
| ------------- | --------------------------------------------- | ------------------------------------ |
| Loop Skills   | `v-for="skill in skills"`                     | Melakukan perulangan data            |
| Data Skills   | `{ name: "Communication", percent: 90 }`      | Menyimpan nilai skill                |
| Dynamic Width | `:style="{ width: skill.percent + '%' }"`     | Mengatur progress bar secara dinamis |
| Glass Card    | `.glass-card { backdrop-filter: blur(8px); }` | Efek transparan blur                 |

Skills diambil dari array Vue dan dirender otomatis menggunakan v-for.

---
## 4. Showcase Section

<img width="1899" height="928" alt="image" src="https://github.com/user-attachments/assets/df0e7408-38f5-4161-9e1e-7af02925c216" />

Memiliki 3 tab:
  - Projects
  - Certificate
  - Experience
Konten dapat berubah sesuai tab yang dipilih

## 💻 Penjelasan Kode

| Bagian             | Potongan Kode                       | Fungsi                              |
| ------------------ | ----------------------------------- | ----------------------------------- |
| Tab Button         | `@click="activeTab='project'"`      | Mengubah tab aktif                  |
| Conditional Render | `v-else-if="activeTab==='project'"` | Menampilkan konten sesuai tab       |
| Loop Data          | `v-for="project in projects"`       | Menampilkan daftar project          |
| Transition         | `<transition name="fade">`          | Memberikan animasi saat tab berubah |

Section ini menggunakan conditional rendering vue untum menampilkan isi konten.

---
## 5. Contact Section

Berisi:
  - Email
  - Link Github
  - Ikon Bootstrap

## 💻 Penjelasan Kode

| Bagian       | Potongan Kode                                          | Fungsi                      |
| ------------ | ------------------------------------------------------ | --------------------------- |
| Email Link   | `href="mailto:..."`                                    | Membuka email client        |
| GitHub Link  | `target="_blank"`                                      | Membuka link di tab baru    |
| Icon         | `<i class="bi bi-github"></i>`                         | Menggunakan Bootstrap Icons |
| Hover Effect | `.contact-item:hover { transform: translateY(-2px); }` | Animasi saat hover          |

---

# 🎨Konsep Design 
Website ini menggunakan konsep: 

- 🌙 Dark gradient background
- 🪟 Glassmorphism card
- 💜 Purple accent color
- ✨ Typing animation
- 🔁 Dynamic tab transition
- 🔗 Smooth scroll navigation

Scroll Smooth diatur di css menggunakan:

html {
  scroll-behavior: smooth;
}/>

# PANDUAN PEMISAHAN CSS - Explore Indonesia

## 📋 Struktur Folder CSS

```
src/styles/
├── README.md              # Dokumentasi ini
├── global.css            # CSS Global (sudah dibuat ✅)
├── header.css            # CSS untuk Header component
├── footer.css            # CSS untuk Footer component
├── index.css             # CSS halaman Home
├── product.css           # CSS halaman Product
├── gallery.css           # CSS halaman Gallery
├── about.css             # CSS halaman About
└── contact.css           # CSS halaman Contact
```

## 🚀 Cara Menggunakan CSS Terpisah

### Langkah 1: Import CSS di File Astro

Ganti bagian `<style>` di setiap file `.astro` dengan:

```astro
<!-- Di dalam <head> -->
<link rel="stylesheet" href="/styles/global.css" />
<link rel="stylesheet" href="/styles/nama-halaman.css" />
```

### Langkah 2: Copy CSS dari <style> ke File CSS

Contoh untuk **index.astro**:

**SEBELUM** (di index.astro):

```astro
<style>
  .hero {
    height: 100vh;
    /* ... css lainnya ... */
  }
</style>
```

**SESUDAH**:

**File: src/styles/index.css**

```css
.hero {
  height: 100vh;
  /* ... css lainnya ... */
}
```

**File: src/pages/index.astro**

```astro
<head>
  <!-- ... tags lainnya ... -->
  <link rel="stylesheet" href="/styles/global.css" />
  <link rel="stylesheet" href="/styles/index.css" />
</head>
```

## 📝 Checklist Pemisahan CSS

### Halaman yang Perlu Diproses:

- [ ] **index.astro** → `styles/index.css`
  - Hero section
  - Vehicle packages
  - About section
  - Testimonials
- [ ] **product.astro** → `styles/product.css`
  - Product cards
  - Speedboat sections
  - Rent car section
  - Modal styles
- [ ] **gallery.astro** → `styles/gallery.css`
  - Gallery grid
  - Modal gallery
  - Navigation buttons
- [ ] **about.astro** → `styles/about.css`
  - About content
  - Team section
- [ ] **contact.astro** → `styles/contact.css`
  - Contact form
  - Info section

### Components:

- [ ] **Header.astro** → `styles/header.css`
  - Navigation
  - Mobile menu
  - Scrolled state
- [ ] **Footer.astro** → `styles/footer.css`
  - Footer layout
  - Social links

## 🔧 Langkah-langkah Detail

### Untuk setiap file .astro:

1. **Buka file** (contoh: `src/pages/index.astro`)

2. **Cari tag `<style>`** (biasanya di dalam `<head>`)

3. **Copy semua CSS** dari dalam `<style>...</style>`

4. **Buat file CSS baru** di `src/styles/`
   - Nama file sesuai halaman (misal: `index.css`, `product.css`)

5. **Paste CSS** ke file baru tanpa tag `<style>`

6. **Hapus tag `<style>`** dari file .astro

7. **Tambahkan link CSS** di `<head>`:

   ```astro
   <link rel="stylesheet" href="/styles/global.css" />
   <link rel="stylesheet" href="/styles/nama-file.css" />
   ```

8. **Test di browser** - pastikan styling tetap sama

## ⚠️ PENTING - Hal yang Perlu Diperhatikan:

1. **Path CSS harus benar**: `/styles/nama-file.css` (dengan slash di depan)

2. **Urutan import penting**:
   - `global.css` harus di-load **pertama**
   - Kemudian CSS halaman spesifik

3. **Jangan hapus** bagian `<script>` - itu JavaScript, bukan CSS

4. **Media queries** tetap di file CSS yang sama

5. **File CSS harus di folder `public/styles/`** atau `src/styles/` tergantung setup Astro

## 📊 Estimasi Ukuran File CSS:

- `global.css`: ~100 baris ✅ (Sudah dibuat)
- `index.css`: ~800 baris
- `product.css`: ~1500 baris (file terbesar)
- `gallery.css`: ~400 baris
- `about.css`: ~300 baris
- `contact.css`: ~300 baris
- `header.css`: ~200 baris
- `footer.css`: ~150 baris

## 🎯 Keuntungan Pemisahan CSS:

✅ **Lebih mudah diedit** - tidak perlu scroll panjang
✅ **Tidak bingung** - CSS terpisah dari HTML/JavaScript
✅ **Reusable** - bisa digunakan di halaman lain
✅ **Faster loading** - browser bisa cache CSS
✅ **Team friendly** - developer lain lebih mudah memahami

## 🛠️ Tool Rekomendasi:

- **VS Code Extension**: "CSS Navigation" untuk navigasi cepat
- **Prettier**: untuk format CSS otomatis
- **Live Server**: untuk test perubahan langsung

## 📞 Bantuan:

Jika ada masalah setelah pemisahan:

1. Check browser console untuk error
2. Pastikan path CSS benar
3. Clear browser cache (Ctrl+Shift+R)
4. Check file CSS sudah tersimpan dengan encoding UTF-8

---

**Catatan**: File `global.css` sudah dibuat dan berisi styling dasar.
Anda bisa mulai dengan memindahkan CSS dari file yang paling kecil dulu (misal: about.astro atau contact.astro).

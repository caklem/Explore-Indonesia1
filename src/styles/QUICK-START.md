# 🚀 QUICK START - Cara Cepat Menggunakan CSS Terpisah

## ✅ File CSS Sudah Dibuat!

Semua file CSS template sudah tersedia di folder `src/styles/`:

```
✅ global.css        - CSS dasar (sudah terisi)
✅ header.css        - Template untuk Header
✅ footer.css        - Template untuk Footer
✅ index.css         - Template untuk Home page
✅ product.css       - Template untuk Product page
✅ gallery.css       - Template untuk Gallery page
✅ about.css         - Template untuk About page
✅ contact.css       - Template untuk Contact page
```

## 📝 3 LANGKAH MUDAH untuk Setiap Halaman:

### LANGKAH 1: Buka File Astro

Contoh: `src/pages/index.astro`

### LANGKAH 2: Copy CSS ke File Template

1. Cari tag `<style>` di file Astro
2. Copy **SEMUA ISI** dari dalam `<style>...</style>`
3. Paste ke file CSS yang sesuai di `src/styles/`
4. **JANGAN copy tag `<style>` nya**, hanya isinya saja

### LANGKAH 3: Ganti <style> dengan <link>

**HAPUS:**

```astro
<style>
  /* semua CSS di sini */
</style>
```

**GANTI DENGAN:**

```astro
<link rel="stylesheet" href="/src/styles/global.css" />
<link rel="stylesheet" href="/src/styles/nama-file.css" />
```

## 🎯 Contoh Lengkap untuk Gallery Page:

### SEBELUM (Gallery.astro):

```astro
<head>
  <title>Gallery</title>
  <style>
    .destinations-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
    }
    /* ... 500 baris CSS lainnya ... */
  </style>
</head>
```

### SESUDAH:

**File: src/pages/Gallery.astro**

```astro
<head>
  <title>Gallery</title>
  <link rel="stylesheet" href="/src/styles/global.css" />
  <link rel="stylesheet" href="/src/styles/gallery.css" />
</head>
```

**File: src/styles/gallery.css**

```css
.destinations-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
/* ... 500 baris CSS lainnya ... */
```

## 📋 Checklist Halaman:

Copy paste checklist ini dan centang setiap selesai:

```
[ ] index.astro      → Pindahkan CSS ke index.css
[ ] product.astro    → Pindahkan CSS ke product.css
[ ] Gallery.astro    → Pindahkan CSS ke gallery.css
[ ] about.astro      → Pindahkan CSS ke about.css
[ ] Contact.astro    → Pindahkan CSS ke contact.css
[ ] Header.astro     → Pindahkan CSS ke header.css
[ ] Footer.astro     → Pindahkan CSS ke footer.css
```

## ⚠️ PENTING:

1. **JANGAN hapus tag `<script>`** - itu JavaScript, biarkan di file Astro
2. **Path harus benar**: `/src/styles/nama-file.css`
3. **Test setelah pindah**: buka di browser, pastikan styling sama
4. **Save file dengan UTF-8 encoding**

## 🔍 Cara Test:

1. Pindahkan CSS dari satu halaman
2. Buka halaman tersebut di browser
3. Tekan `Ctrl+Shift+R` untuk hard refresh
4. Pastikan tampilan tetap sama
5. Jika ada yang rusak, cek browser console (F12)

## 🎨 Tips:

- Mulai dari halaman **paling kecil** dulu (about.astro atau contact.astro)
- Gunakan **VS Code Split View** untuk copy-paste lebih mudah
- Gunakan **Find & Replace** untuk update multiple files sekaligus
- **Backup dulu** sebelum mulai (git commit atau copy folder)

## 💡 Keuntungan Setelah Selesai:

✅ Code lebih rapi dan terorganisir
✅ Mudah dicari dan diedit
✅ User/developer lain tidak bingung
✅ File loading lebih cepat
✅ Bisa reuse CSS di halaman lain

## 🆘 Troubleshooting:

**Masalah: CSS tidak muncul**

- ✅ Cek path file: `/src/styles/nama-file.css`
- ✅ Cek file sudah di-save
- ✅ Hard refresh browser (Ctrl+Shift+R)

**Masalah: Styling berbeda**

- ✅ Pastikan SEMUA CSS sudah di-copy
- ✅ Cek tidak ada CSS yang tertinggal di file Astro
- ✅ Cek urutan import CSS (global.css harus pertama)

**Masalah: File tidak ketemu**

- ✅ Cek folder `src/styles/` ada
- ✅ Cek nama file sama dengan yang di-link
- ✅ Restart dev server (`npm run dev`)

---

## 🎉 Selamat Mengorganisir CSS!

Butuh bantuan? Baca file `PANDUAN-PEMISAHAN-CSS.md` untuk penjelasan lebih detail.

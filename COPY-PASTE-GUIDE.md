# 📋 PANDUAN COPY-PASTE CSS - Exact Line Numbers

## ⚠️ PENTING: Backup Dulu!

Sebelum mulai, commit git atau backup folder project Anda.

---

## 🎨 Gallery.astro → gallery.css

**File Source**: `src/pages/Gallery.astro`
**CSS Location**: Baris **21** sampai **718**
**Destination**: `src/styles/gallery.css`

**Cara:**

1. Buka `src/pages/Gallery.astro`
2. Select dari baris 21 (setelah `<style>`) sampai baris 718 (sebelum `</style>`)
3. Copy (Ctrl+C)
4. Buka `src/styles/gallery.css`
5. Hapus semua isi template
6. Paste (Ctrl+V)
7. Save

**Update Gallery.astro:**

- Hapus baris 20-719 (seluruh `<style>...</style>`)
- Tambahkan setelah tag fonts (sekitar baris 19):

```astro
<link rel="stylesheet" href="/src/styles/gallery.css" />
```

---

## 📄 Product.astro → product.css

**File Source**: `src/pages/product.astro`
**CSS Location**: Baris **21** sampai sekitar **2800**
**Destination**: `src/styles/product.css`

**Cara:**

1. Cari tag `<style>` di product.astro (sekitar baris 20)
2. Cari tag penutup `</style>` (gunakan Find: `</style>`)
3. Select semua CSS antara kedua tag tersebut
4. Copy & paste ke `src/styles/product.css`
5. Save

**Update product.astro:**

- Hapus seluruh `<style>...</style>`
- Tambahkan:

```astro
<link rel="stylesheet" href="/src/styles/product.css" />
```

---

## 🏠 index.astro → index.css

**File Source**: `src/pages/index.astro`
**CSS Location**: Baris **21** sampai sekitar **2500**
**Destination**: `src/styles/index.css`

**Cara Cepat dengan Find:**

1. Buka index.astro
2. Tekan Ctrl+F, cari: `<style>`
3. Tekan Ctrl+F lagi, cari: `</style>`
4. Select semua di antaranya
5. Copy ke `src/styles/index.css`

**Update index.astro:**

- Hapus `<style>...</style>`
- Tambahkan:

```astro
<link rel="stylesheet" href="/src/styles/index.css" />
```

---

## 📖 about.astro → about.css

**File Source**: `src/pages/about.astro`
**Destination**: `src/styles/about.css`

**Cara:**

1. Cari `<style>` di about.astro
2. Select sampai `</style>`
3. Copy ke about.css
4. Update about.astro dengan link CSS

---

## 📧 Contact.astro → contact.css

**File Source**: `src/pages/Contact.astro`
**Destination**: `src/styles/contact.css`

**Cara:**

1. Cari `<style>` di Contact.astro
2. Select sampai `</style>`
3. Copy ke contact.css
4. Update Contact.astro dengan link CSS

---

## 🔝 Header.astro → header.css

**File Source**: `src/components/Header.astro`
**Destination**: `src/styles/header.css`

**Cara:**

1. Cari `<style>` di Header.astro
2. Select sampai `</style>`
3. Copy ke header.css
4. Update Header.astro dengan link CSS

---

## 🔽 Footer.astro → footer.css

**File Source**: `src/components/Footer.astro`
**Destination**: `src/styles/footer.css`

**Cara:**

1. Cari `<style>` di Footer.astro
2. Select sampai `</style>`
3. Copy ke footer.css
4. Update Footer.astro dengan link CSS

---

## ✅ Testing Setelah Setiap File:

Setelah memindahkan CSS dari satu file:

1. **Save semua file** (Ctrl+K S di VS Code)
2. **Restart dev server**:
   ```bash
   # Stop server (Ctrl+C)
   npm run dev
   ```
3. **Buka halaman di browser**
4. **Hard refresh** (Ctrl+Shift+R)
5. **Cek apakah styling sama**

Jika ada masalah:

- Cek path CSS benar
- Cek tidak ada typo
- Cek file CSS sudah ter-save
- Cek browser console (F12)

---

## 📝 Urutan Yang Disarankan:

Mulai dari yang kecil ke besar:

1. ✅ Footer.astro (paling kecil)
2. ✅ Header.astro
3. ✅ about.astro
4. ✅ Contact.astro
5. ✅ Gallery.astro
6. ✅ index.astro
7. ✅ product.astro (paling besar, terakhir)

---

## 🆘 Jika Ada Error:

**"CSS not loading"**
→ Restart dev server

**"Styling berbeda"**
→ Cek apakah SEMUA CSS sudah di-copy (cek tidak ada yang tertinggal)

**"File not found"**
→ Cek path: `/src/styles/nama-file.css`

---

Selamat memisahkan CSS! 🎉

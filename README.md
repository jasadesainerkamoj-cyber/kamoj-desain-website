# 🎨 KamOj Desain Website

Website portofolio desain grafis untuk KamOj Desain - Timika. Platform interaktif untuk menampilkan dan menjual hasil desain Anda.

## ✨ Fitur

✅ **Galeri Karya Interaktif** - Tambah, edit, hapus karya langsung dari website  
✅ **Integrasi WhatsApp** - Tombol pesan otomatis ke nomor tujuan  
✅ **Responsive Design** - Tampilannya bagus di mobile, tablet, dan desktop  
✅ **Dark Theme Modern** - Desain profesional dengan warna gelap & aksen merah  
✅ **Penyimpanan Lokal** - Data karya tersimpan otomatis di browser Anda  

## 🚀 Cara Menggunakan

### 1. Deploy ke Cloudflare Pages (Gratis & Mudah)

1. Buka [https://dash.cloudflare.com](https://dash.cloudflare.com)
2. Klik **Workers & Pages** → **Pages** → **Connect to Git**
3. Pilih repository `kamoj-desain-website` Anda
4. Klik **Deploy** - selesai!
5. Akses website Anda di URL yang diberikan Cloudflare

### 2. Deploy ke GitHub Pages (Alternatif)

1. Buka Settings repository → Pages
2. Pilih source: `main` branch
3. Tunggu deployment selesai
4. Akses di `https://jasadesainerkamoj-cyber.github.io/kamoj-desain-website/`

## 📝 Cara Menambah Karya

### Metode 1: Melalui Website (Paling Mudah)
1. Buka website Anda
2. Scroll ke section **"Karya kami"**
3. Klik tombol **"+ Tambah Karya Baru"**
4. Isi form:
   - **Judul Karya** - Nama proyek (contoh: "Desain Kaos SATGAS")
   - **Spesifikasi** - Deskripsi singkat (contoh: "Desain grafis untuk sablon, siap pisah warna")
   - **Harga** - Harga jual (contoh: "Rp50.000")
   - **URL Foto** - Link gambar (opsional, bisa ditambah nanti)
   - **Nomor WhatsApp** - Nomor tujuan (opsional, kosongkan untuk pakai nomor default)
5. Klik **"Simpan Karya"** ✅

### Metode 2: Edit File HTML Langsung
1. Buka `index.html` di repository
2. Cari bagian `const KARYA = [` (di bagian script paling bawah)
3. Edit atau tambah data karya (lihat contoh di bawah)
4. Commit perubahan

### Contoh Format Data Karya

```javascript
{ 
  gambar: "https://example.com/karya.jpg", // link foto
  judul: "Desain Kaos SATGAS",             // nama karya
  spek: "Desain grafis untuk sablon, siap pisah warna", // deskripsi
  harga: "Rp50.000",                       // harga
  wa: ""                                   // nomor WA (kosong = pakai default)
}
```

## 🖼️ Upload Foto Karya

Pilih salah satu tempat untuk upload foto:

### Opsi 1: Imgur (Paling Mudah)
1. Buka [https://imgur.com](https://imgur.com)
2. Upload foto → Copy link
3. Paste link di field "URL Foto Karya"

### Opsi 2: GitHub (Gratis, Terpercaya)
1. Upload foto ke folder di repository ini
2. Buka file di GitHub → klik "Raw" → copy URL
3. Paste di field "URL Foto Karya"

### Opsi 3: Google Drive / OneDrive
1. Upload foto
2. Set sharing ke "Public"
3. Copy link publik → paste di form

## 📞 Ubah Nomor WhatsApp

### Default nomor: `0813-4595-671`

Untuk mengubah:
- **Per karya**: Isi field "Nomor WhatsApp" di form tambah karya
- **Global (semua karya)**: Edit variable `DEFAULT_WA` di `index.html`

```javascript
const DEFAULT_WA = "628134595671"; // ganti angka ini
```

## 🎨 Customize Warna & Desain

Edit bagian `:root` di CSS (baris ~25):

```css
:root{
  --bg:        #0d0d0d;    /* warna latar gelap */
  --red:       #c81d25;    /* warna accent (merah) */
  --ink:       #ede8e2;    /* warna teks */
  --muted:     #948d87;    /* warna teks gelap */
}
```

## 💾 Backup Data

Data karya Anda tersimpan di **Local Storage** browser. Untuk backup:

1. Buka Developer Tools (F12) → Console
2. Ketik: `console.log(JSON.parse(localStorage.getItem('karyaList')))`
3. Copy hasil → simpan di file `.txt` atau `.json` untuk backup

## 🐛 Troubleshooting

**Q: Foto tidak muncul?**  
A: Pastikan URL link foto benar dan bisa diakses publik. Coba test link di browser baru.

**Q: Karya tidak tersimpan?**  
A: Clear cache browser atau coba di incognito mode. Pastikan Local Storage tidak diblokir.

**Q: Tombol WhatsApp tidak bekerja?**  
A: Cek nomor WA format: bisa `0813...` atau `628134...` (tanpa +)

## 📋 Checklist Sebelum Go Live

- [ ] Deploy ke Cloudflare Pages / GitHub Pages
- [ ] Test di mobile & desktop
- [ ] Upload minimal 3-4 foto karya
- [ ] Cek semua link WhatsApp berfungsi
- [ ] Customize warna & teks sesuai brand Anda
- [ ] Bagikan link ke customer

## 📚 Resources

- [Cloudflare Pages Docs](https://developers.cloudflare.com/pages/)
- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [Imgur Upload](https://imgur.com)
- [Font Google](https://fonts.google.com)

---

**Dibuat dengan ❤️ untuk KamOj Desain**  
© 2026 - Timika

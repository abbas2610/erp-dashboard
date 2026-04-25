# Blackjack & DGA — ERPNext Project Dashboard

Dashboard project management untuk implementasi dan inject data ERPNext.

## 🚀 Deploy ke GitHub Pages

### Langkah-langkah:

**1. Buat repository baru di GitHub**
- Buka https://github.com/new
- Repository name: `erp-dashboard` (atau nama lain)
- Visibility: **Private** (recommended, karena ini data internal)
- Klik **Create repository**

**2. Upload file**

Cara termudah lewat browser:
- Buka repo yang baru dibuat
- Klik **"uploading an existing file"**
- Drag & drop file `index.html` ke area upload
- Commit message: `Initial dashboard`
- Klik **Commit changes**

Atau via Git (jika sudah install Git):
```bash
git init
git add index.html
git commit -m "Initial dashboard"
git remote add origin https://github.com/USERNAME/erp-dashboard.git
git push -u origin main
```

**3. Aktifkan GitHub Pages**
- Di repo, buka **Settings** → **Pages** (sidebar kiri)
- Source: **Deploy from a branch**
- Branch: `main` → folder: `/ (root)`
- Klik **Save**

**4. Akses dashboard**

Setelah 1–2 menit, dashboard bisa diakses di:
```
https://USERNAME.github.io/erp-dashboard
```
Ganti `USERNAME` dengan username GitHub Abbas.

---

## ⚠️ Penting: Data tidak tersimpan otomatis

Dashboard ini adalah **single HTML file** — data yang diinput (status, deadline) hanya tersimpan selama browser tab terbuka. Kalau tab ditutup, data reset.

### Opsi untuk menyimpan data permanen:

| Opsi | Kesulitan | Biaya |
|------|-----------|-------|
| Tambah localStorage (simpan di browser lokal) | Mudah | Gratis |
| Google Sheets sebagai backend via API | Sedang | Gratis |
| Supabase (database cloud) | Sedang | Gratis s/d batas tertentu |
| Airtable integration | Mudah | Gratis s/d batas tertentu |

Rekomendasinya: **localStorage dulu** supaya paling cepat — data tersimpan di browser masing-masing user. Kalau butuh shared/sync antar user, baru naik ke Supabase atau Google Sheets.

---

## 📁 Struktur File

```
erp-dashboard/
└── index.html    ← satu file ini sudah cukup
```

---

## 🔄 Update Dashboard

Kalau ada perubahan (tambah item, update status default, dll):
1. Edit `index.html`
2. Upload ulang ke GitHub (replace file lama)
3. GitHub Pages otomatis update dalam ~1 menit

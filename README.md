# Dashboard Rencana Aksi KSP Kawasan Perbatasan
**Dinas PUPR Provinsi Banten – TA 2026**

Dashboard interaktif untuk memantau 512 Rencana Aksi Kawasan Strategis Provinsi (KSP) Kawasan Perbatasan Banten, terintegrasi lintas WKP I, WKP II, WKP III, dan Provinsi.

---

## Struktur Project

```
ksp-dashboard/
├── index.html          ← Entry point utama
├── vercel.json         ← Konfigurasi Vercel
├── README.md
└── src/
    ├── app.js          ← Entry JS, boot & state management
    ├── charts.js       ← Semua visualisasi Chart.js
    ├── table.js        ← Tabel, filter, sort, pagination
    ├── modal.js        ← Detail popup per rencana aksi
    ├── styles.css      ← Semua styling
    └── data.js         ← Data rencana aksi (auto-generated dari Excel)
```

---

## Cara Deploy ke Vercel via GitHub

### Langkah 1 – Upload ke GitHub
1. Buka [github.com](https://github.com) → Login → **New repository**
2. Nama repo: `ksp-dashboard-perbatasan` → **Create repository**
3. Upload semua file ini ke repo (drag & drop atau git push)

### Langkah 2 – Connect ke Vercel
1. Buka [vercel.com](https://vercel.com) → Login (bisa pakai akun GitHub)
2. Klik **Add New Project**
3. Pilih repo `ksp-dashboard-perbatasan`
4. Klik **Deploy** (tidak perlu setting apapun – otomatis terdeteksi sebagai static site)
5. ✅ Selesai! Dapat URL publik seperti: `https://ksp-dashboard-perbatasan.vercel.app`

### Update Data
Setiap kali push ke GitHub → Vercel otomatis re-deploy (CI/CD otomatis).

---

## Fitur Dashboard

| Fitur | Keterangan |
|---|---|
| KPI Cards | Total RA, Isu, Program, RA Lintas WKP |
| 6 Charts | WKP, Sumber Dana, Program, Isu, Tahun, Instansi |
| Filter | Cari teks, WKP, Sumber Dana, Tahun, Instansi |
| Sort | Klik header kolom |
| Pagination | 25 baris/halaman |
| Detail Modal | Klik baris untuk info lengkap |
| Baris kuning | RA yang sudah dikonsolidasi lintas WKP |

---

## Data

Bersumber dari:
- `MATRIKS_RENCANA_AKSI_KAWASAN_PERBATASAN.xlsx`
- Sheet: PROV, WKP I, WKP II, WKP III
- Dikonsolidasi: 1.211 → 512 baris unik
- Regulasi: Perda Banten No. 1/2023, RTRW 2023–2043

---

*Dinas PUPR Provinsi Banten · Penyempurnaan Ranpergub KSP TA 2026*

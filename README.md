# Tugas 05: Transfer Learning untuk Klasifikasi Citra dengan Data Terbatas

Rizky Mirzaviandy Priambodo (2802549041)

Perbandingan pelatihan dari nol, feature extraction, fine tuning layer4, uji augmentasi, dan EfficientNet-B0 pada 10 kelas Oxford-IIIT Pet (5 ras kucing, 5 ras anjing).

## Isi repositori

| File | Isi |
|---|---|
| `Tugas05_Transfer_Learning.ipynb` | Notebook lengkap dengan semua output |
| `Laporan_Tugas05.pdf` | Laporan analisis (Bagian A, B, C) |
| `history.csv` | Log per epoch untuk setiap run |
| `summary.json` | Konfigurasi dan metrik akhir setiap run |
| `requirements.txt` | Library Python yang dipakai |

## Cara menjalankan

```bash
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute Tugas05_Transfer_Learning.ipynb
```

Dataset diunduh otomatis ke folder `data/` (sekitar 800 MB). Notebook memakai GPU jika ada dan CPU jika tidak. Seed 42.

## Hasil (Test Macro F1)

| B1 scratch | B2 feature extraction | B3 fine tuning + aug | B4 tanpa aug | B5 EfficientNet-B0 |
|---|---|---|---|---|
| 0,410 | 0,851 | 0,862 | 0,873 | 0,937 |

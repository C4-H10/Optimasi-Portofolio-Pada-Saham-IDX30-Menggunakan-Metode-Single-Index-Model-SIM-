# Analisis Optimasi Portofolio Menggunakan Single Index Model pada Indeks IDX30

## Deskripsi Proyek
Proyek ini bertujuan untuk membentuk portofolio investasi optimal dari saham-saham yang terdaftar dalam indeks IDX30 di Bursa Efek Indonesia. Analisis dilakukan menggunakan metode Single Index Model (SIM) untuk mengukur hubungan antara imbal hasil saham individu dengan imbal hasil pasar (IHSG) serta menentukan alokasi aset yang paling efisien berdasarkan parameter risiko dan return.

## Metodologi
Penelitian ini menggunakan data harga penutupan harian periode 26 Maret 2025 hingga 26 Maret 2026. Langkah-langkah analisis meliputi:
* Penghitungan imbal hasil harian (log return) saham dan IHSG.
* Estimasi parameter model yang meliputi Alfa, Beta, dan Varians Residual.
* Penghitungan Excess Return to Beta (ERB) untuk melakukan pemeringkatan saham.
* Penentuan titik pembatas (Cut-off Point) untuk memilih saham kandidat portofolio.
* Penentuan bobot investasi untuk masing-masing saham terpilih.
* Evaluasi kinerja portofolio menggunakan Indeks Treynor.

## Penjelasan Variabel
Berdasarkan model yang diimplementasikan, berikut adalah definisi variabel yang digunakan:
* **E(Ri)**: Tingkat pengembalian yang diharapkan dari saham individu.
* **Beta**: Ukuran sensitivitas imbal hasil saham terhadap fluktuasi pasar.
* **Alfa**: Komponen imbal hasil yang tidak dipengaruhi oleh pergerakan pasar.
* **Varians Residual**: Risiko tidak sistematis atau risiko unik perusahaan.
* **ERB (Excess Return to Beta)**: Kelebihan imbal hasil di atas suku bunga bebas risiko per unit risiko sistematis.
* **Ci (Cut-off Point)**: Nilai ambang batas kumulatif untuk seleksi saham.
* **Bobot (Wi)**: Proporsi dana yang dialokasikan pada setiap saham dalam portofolio.

## Hasil Analisis
Hasil pengolahan data menunjukkan poin-poin sebagai berikut:
* **Seleksi Saham**: Dari 30 saham indeks IDX30, sebanyak 22 saham dinyatakan layak masuk ke dalam portofolio optimal karena memiliki nilai ERB yang lebih besar dari nilai Cut-off Point (Ci).
* **Alokasi Terbesar**: Saham PTBA.JK memiliki bobot tertinggi sebesar 12,54%, diikuti oleh ADRO.JK sebesar 6,70% dan ASII.JK sebesar 6,18%.
* **Kinerja Pasar**: Imbal hasil harian IHSG tercatat sebesar 0,000524 dengan Indeks Treynor sebesar 0,000306.
* **Kinerja Portofolio**: Portofolio bentukan menghasilkan imbal hasil harian sebesar 0,002342 dengan Indeks Treynor sebesar 0,002142.
* **Kesimpulan**: Portofolio yang disusun dinyatakan optimal karena memiliki Indeks Treynor yang lebih tinggi dibandingkan dengan pasar.

## Teknologi yang Digunakan
* Bahasa Pemrograman: Python.
* Library Utama: Pandas, NumPy, yfinance.
* Platform Analisis: Google Colaboratory.

## Cara Penggunaan
1. Pastikan telah menginstal library yang diperlukan melalui perintah `pip install yfinance pandas numpy`.
2. Unggah file notebook ke Google Colaboratory atau Jupyter Notebook.
3. Konfigurasikan rentang tanggal dan daftar ticker saham pada bagian konfigurasi.
4. Jalankan seluruh sel kode untuk mendapatkan laporan ringkasan alokasi aset dan uji optimalitas.

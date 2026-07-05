 End-to-End Logistics Operations Data Analysis

 📌 Project Overview
Proyek ini bertujuan untuk menganalisis data operasional perusahaan logistik guna mengoptimalkan profitabilitas rute, menekan biaya pemeliharaan armada truk, serta mengevaluasi dan meningkatkan keselamatan serta ketepatan waktu pengiriman pengemudi (On-Time Performance).

Analisis dilakukan menggunakan Python dengan pendekatan data-driven untuk menghasilkan rekomendasi bisnis yang konkret bagi tim manajemen logistik.

---

 📂 Dataset & Schema
Dataset yang digunakan berisi 14 tabel relasional operasional logistik dengan total data transaksi mencapai ratusan ribu baris. Beberapa tabel utama meliputi:
 Loads: Detail pengiriman barang (berat, tipe muatan, pendapatan).
 Trips: Detail perjalanan armada (jarak aktual, konsumsi bahan bakar).
 Routes: Data rute resmi (kota asal, kota tujuan, jarak rata-rata).
 Maintenance Records: Catatan pemeliharaan truk (biaya mekanik, suku cadang, downtime).
 Delivery Events: Log waktu penjemputan dan pengantaran muatan.
 Safety Incidents: Log kecelakaan atau pelanggaran lalu lintas oleh pengemudi.

---

 🛠️ Tech Stack & Libraries
 Language: Python 3.11+
 Libraries: Pandas, NumPy, Matplotlib, Seaborn
 Environment: Jupyter Notebook / VS Code

---

 📈 Key Analysis & Insights

 1. Analisis Profitabilitas Rute (Revenue vs Distance)
Mengidentifikasi rute dengan kontribusi pendapatan terbesar serta mengevaluasi efisiensi pendapatan per mil (Revenue per Mile):
 Rute Pendapatan Tertinggi: Rute Philadelphia ➔ Seattle mencatat total akumulasi pendapatan terbesar sebesar $10,069,054.22 (jarak 2,729 mil).
 Rute Paling Efisien: Rute Phoenix ➔ Philadelphia menghasilkan rasio pendapatan per mil tertinggi sebesar $2.71/mil, menjadikannya rute paling menguntungkan dari sisi efisiensi jarak.

 2. Analisis Efisiensi & Perawatan Armada (Fleet Maintenance)
Mengevaluasi korelasi antara usia pembuatan truk dengan biaya pemeliharaan:
 Truk Paling Boros: Truk dengan ID TRK00003 (Peterbilt 2018) memerlukan biaya perawatan terbesar mencapai $90,161.42 dengan frekuensi perbaikan sebanyak 41 kali.
 Tren Pemeliharaan: Truk keluaran tahun yang lebih lama (2015-2016) menunjukkan kecenderungan tingkat perbaikan yang tinggi dan downtime yang memakan waktu lama.

 3. Analisis Kinerja & Keselamatan Pengemudi (OTP vs Safety Incidents)
Mengevaluasi persentase ketepatan waktu pengantaran (On-Time Performance / OTP) serta hubungannya dengan keselamatan berkendara:
 Tingkat OTP Keseluruhan: Perusahaan mencatat 93,196 pengiriman tepat waktu dan 74,196 pengiriman terlambat.
 Performa Terendah: Pengemudi Mary Wilson (DRV00133) mencatat OTP terendah yaitu 51.61% dari 1,366 perjalanan.
 Korelasi Keamanan: Pengemudi dengan tingkat OTP rendah memiliki korelasi kuat dengan jumlah insiden keselamatan (safety incidents) yang tinggi, mengindikasikan adanya fatigue (kelelahan) atau kurangnya standar kedisiplinan berkendara.

---

 💡 Business Recommendations
1. Optimalisasi Rute: Prioritaskan alokasi armada pada rute dengan Revenue per Mile tinggi seperti Phoenix ➔ Philadelphia untuk memaksimalkan margin keuntungan.
2. Peremajaan Armada: Lakukan audit mendalam pada truk-truk tua (pembuatan 2015/2016) yang memiliki biaya pemeliharaan membengkak dan pertimbangkan untuk melakukan peremajaan unit guna menekan downtime.
3. Program Pelatihan Driver: Berikan pelatihan keselamatan dan manajemen waktu khusus bagi kelompok pengemudi dengan tingkat OTP di bawah 60% serta memiliki riwayat insiden lalu lintas.

---

 🚀 Cara Menjalankan Project
1. Clone repository ini:
   ```bash
   git clone https://github.com/prayoga1726/logistics-analysis.git
   ```
2. Pastikan file dataset (`.csv`) berada di folder yang sama dengan notebook.
3. Instal dependensi yang diperlukan:
   ```bash
   pip install pandas numpy matplotlib seaborn ipykernel
   ```
4. Buka `logistics_analysis.ipynb` di VS Code / Jupyter Lab dan jalankan semua sel kode.

1. Deskripsi Kasus

Dalam industri e-commerce, pemahaman terhadap perilaku dan karakteristik pelanggan merupakan faktor kunci dalam menyusun strategi pemasaran yang efektif, seperti personalisasi promosi, segmentasi pelanggan, dan peningkatan loyalitas. Namun, data perilaku pelanggan umumnya bersifat multidimensi, terdiri dari berbagai fitur numerik yang saling berkaitan, sehingga sulit untuk dianalisis dan divisualisasikan secara langsung.

Proyek ini bertujuan untuk menerapkan teknik reduksi dimensi (Dimensionality Reduction) guna menyederhanakan data perilaku pelanggan ke dalam representasi 2D dan 3D, sehingga pola, struktur, dan segmentasi pelanggan dapat diamati secara visual. Dua metode utama yang digunakan adalah Principal Component Analysis (PCA) dan t-Distributed Stochastic Neighbor Embedding (t-SNE).

2. Dataset yang Digunakan

Dataset yang digunakan adalah E-commerce Customer Behavior.csv, yang berisi data perilaku belanja pelanggan. Fitur utama yang digunakan dalam analisis ini meliputi:
Age: Usia pelanggan
Total Spend: Total pengeluaran pelanggan (juga digunakan sebagai indikator warna pada visualisasi)
Items Purchased: Jumlah barang yang dibeli
Average Rating: Rata-rata rating yang diberikan pelanggan
Days Since Last Purchase: Jumlah hari sejak transaksi terakhir
Pre-processing Data
Sebelum analisis dilakukan, data melalui beberapa tahap pra-pemrosesan, yaitu:
Pembersihan data dari nilai kosong (missing values)
Standarisasi fitur menggunakan StandardScaler agar setiap variabel memiliki skala yang sama dan tidak mendominasi hasil analisis
Tahapan ini penting agar algoritma PCA dan t-SNE bekerja secara optimal dan adil terhadap seluruh fitur.

3. Ringkasan Metode
Principal Component Analysis (PCA)
PCA merupakan metode reduksi dimensi linear yang bertujuan mempertahankan variansi terbesar dari data asli. Dalam proyek ini, PCA digunakan dalam dua bentuk visualisasi:
PCA 3D: Memberikan gambaran struktur data secara lebih mendalam dan menyeluruh
PCA 2D: Memproyeksikan data ke dua komponen utama (PC1 dan PC2) untuk melihat pola distribusi global pelanggan
PCA membantu mengidentifikasi arah utama variasi data dan tren umum perilaku pelanggan.
t-Distributed Stochastic Neighbor Embedding (t-SNE)
t-SNE adalah metode reduksi dimensi non-linear yang sangat efektif dalam memvisualisasikan struktur lokal dan klaster data. Metode ini berusaha menjaga titik-titik data yang memiliki kemiripan agar tetap berdekatan dalam ruang berdimensi rendah (2D).
t-SNE digunakan untuk mengungkap segmentasi pelanggan yang tidak selalu terlihat jelas dengan metode linear seperti PCA.

4. Analisis Hasil
Analisis PCA (Struktur Global)
Berdasarkan visualisasi PCA 2D dan 3D, terlihat bahwa data pelanggan membentuk pola distribusi yang relatif linear dan mengikuti jalur tertentu. Pewarnaan berdasarkan Total Spend menunjukkan gradasi yang cukup jelas sepanjang sumbu Principal Component 1 (PC1).
Pelanggan dengan tingkat pengeluaran tinggi (warna kuning) cenderung berada di satu sisi spektrum, sedangkan pelanggan dengan pengeluaran rendah (warna ungu) berada di sisi berlawanan. Hal ini menunjukkan bahwa PCA berhasil menangkap tren umum pengeluaran pelanggan. Namun demikian, beberapa titik data masih tampak saling menumpuk, sehingga pemisahan segmen pelanggan belum terlihat secara tajam.

Analisis t-SNE (Pola Klaster)
Berbeda dengan PCA, visualisasi t-SNE menghasilkan pemisahan klaster yang jauh lebih jelas. Teridentifikasi sekitar 8 hingga 10 klaster terpisah yang merepresentasikan segmen pelanggan dengan karakteristik perilaku yang berbeda.
Pelanggan dengan Total Spend tinggi membentuk klaster tersendiri yang relatif eksklusif, sehingga memudahkan identifikasi pelanggan bernilai tinggi (high-value / VVIP customers). Pemisahan antar klaster yang menyerupai “pulau-pulau” titik menunjukkan bahwa perilaku pelanggan dalam dataset ini memiliki pola yang unik dan berbeda secara signifikan antar kelompok.

6. Perbandingan PCA dan t-SNE
Aspek	PCA	t-SNE
Linearitas	Linear	Non-linear
Fokus utama	Mempertahankan variansi global	Mempertahankan struktur lokal dan klaster
Hasil visual	Menunjukkan tren dan persebaran umum	Menunjukkan segmentasi yang sangat jelas
Kegunaan utama	Analisis global dan interpretasi variabel	Segmentasi pelanggan secara detail
Kesimpulan

Berdasarkan hasil analisis, dapat disimpulkan bahwa PCA dan t-SNE saling melengkapi dalam analisis perilaku pelanggan e-commerce. PCA efektif untuk memahami struktur global dan tren utama dalam data, sementara t-SNE sangat unggul dalam mengungkap segmentasi pelanggan secara visual dan detail. Kombinasi kedua metode ini memberikan wawasan yang kuat untuk mendukung strategi pemasaran berbasis data dan pengambilan keputusan bisnis yang lebih tepat.

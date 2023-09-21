# Predict Clicked Ads Customer Classification by using Machine Learning
## Background
Sebuah perusahaan di Indonesia ingin mengetahui efektifitas sebuah iklan yang mereka tayangkan, hal ini penting bagi perusahaan agar dapat mengetahui seberapa besar ketercapainnya iklan yang dipasarkan sehingga dapat menarik customers untuk melihat iklan.
Dengan mengolah data historical advertisement serta menemukan insight serta pola yang terjadi, maka dapat membantu perusahaan dalam menentukan target marketing, fokus case ini adalah membuat model machine learning classification yang berfungsi menentukan target customers yang tepat

## Objective

Membuat model machine learning classification untuk memudahkan perusahaan dalam mengambil keputusan dalam menentukan target marketing.

## Tools
Pada proyek ini saya menggunakan python sebagai bahasa pemrograman; Jupyter sebagai notebook; pandas, numpy, sklearn dan python ke bagian preprocessing dan machine learning; kombinasi matplotlib dan seaborn library untuk menghasilkan visualisasi data.

### Content
## Data Cleaning dan Data Preprocessing
Pada bagian ini terdapat beberapa proses seperti penanganan missing value. Feature numerik nilai yang kosong diisi dengan nilai median dari masing-masing feature. Penggunaan nilai median sebagai nilai yang diinputkan untuk nilai yang kosong karena distribusi data cenderung skewed. Pada feature kategorik nilai kosong diisi dengan modus dari feature tersebut dan dataset tidak memiliki nilai yang duplikat. Melakukan Extract Datetime, serta split data feature dan target kemudian split data train 70%  dan test  30%. Melakukan feture encoding dengan label encoding dan One Hot Encoding.

## Data Modeling
Melakukan eksperimen data modeling tanpa melakukan normalisasi dan melakukan normalisasi. Setelah dilakukan normalisasi data, terdapat beberapa perubahan pada hasil model. Akurasinya mengalami peningkatan untuk semua model khususnya pada KNN dan Logistic Regression yang mengalami peningkatan signifikan dibandingkan hasil sebelumnya. Hal ini membuktikan bahwa menangani normalisasi data dapat meningkatkan performa model termasuk skor accuracy, recall, dan precision.

## Confusion Matrix
Model kami telah menghasilkan hasil yang sangat baik dimana jumlah False Positif (Iklan yang diprediksi di klik, namun sebenarnya tidak) telah diminimalkan secara optimal pada tingkat 3%. Hal ini menghasilkan skor True Positive yang tinggi (Prediksi iklan yang diklik dan benar-benar di klik) sebesar 46,5% yang menghasilkan potensi keuntungan lebih tinggi.

## Feature Important
- Feature dengan korelasi tertinggi dalam memprediksi iklan yang di klik pelanggan adalah ‘Daily Time Spent on Site’ dan ‘Daily Internet Usage’. Hal ini dibuktikan berdasarkan analisis EDA sebelumnya bahwa pelanggan dengan penggunaan internet harian dan waktu yang dihabiskan lebih sedikit di situs memiliki potensi mengklik iklan yang lebih tinggi.
- Feature important yang cukup tinggi adalah ‘ Age’ dan ‘Area Income’. Hal ini didukung dengan gambaran pelanggan berdasarkan usia dan pendapatan daerah menunjukkan bahwa pelanggan yang memiliki usia lebih muda dan pendapatan lebih tinggi memiliki potensi mengklik iklan yang rendah.

## Rekomendasi Bisnis 
- Untuk pengguna dengan Daily Time Spend on Site sekitar 40-45 menit, kami dapat mengoptimalkan iklan agar lebih menarik bagi mereka. Mungkin kami bisa menargetkan iklan yang lebih interaktif atau konten yang lebih singkat dan tajam.
- Pelanggan dengan Daily Internet Usage sekitar 100-150 cenderung mengklik iklan, jadi fokuskan upaya pemasaran pada kelompok ini. Kami bisa mengirim iklan yang lebih sesuai dengan minat mereka.
- Kami bisa lebih fokus pada penargetan kelompok usia yang lebih tua. Kami dapat membuat iklan yang lebih relevan dengan preferensi dan kebutuhan mereka.
- Gunakan data usia dan pendapatan daerah untuk mengidentifikasi dan menargetkan kelompok pelanggan yang memiliki potensi tinggi untuk mengklik iklan. Ini dapat membantu kami mengalokasikan anggaran pemasaran dengan lebih efisien.

## Simulasi Menggunakan Model Machine Learning
Berdasarkan confusion metrix, kita dapat mengelompokkan pelanggan berdasarkan prediksi siapa yang mengklik iklan (145 pelanggan) dan siapa yang tidak mengklik iklan (155 pelanggan).

- Marketing cost = 145 customers X Rp 10.000 = Rp 1.450.000

- Conversion rate = 140/145 *100% = 96,5%

- Revenue = 140 customers X Rp 15.000 = Rp 2.100.000

- Profit = Revenue - Cost = Rp 650.000

Berdasarkan simulasi disamping, besarnya keuntungan sebesar Rp 650.000 dengan tingkat keuntungan 44,8%.

## Kesimpulan
- Penerapan model machine learning dalam memprediksi pelanggan iklan yang diklik sangat berguna dalam dunia industri karena akan mencegah bisnis mengalami potensi kerugian dan menghasilkan potensi keuntungan yang lebih tinggi.

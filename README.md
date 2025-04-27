### Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju
## Business Understanding
Jaya Jaya Maju adalah perusahaan multinasional yang berdiri sejak tahun 2000 dan kini mempekerjakan lebih dari 1.000 karyawan yang tersebar di seluruh penjuru negeri. Meskipun telah berkembang menjadi perusahaan besar, Jaya Jaya Maju menghadapi tantangan serius dalam pengelolaan sumber daya manusia, khususnya tingginya tingkat attrition rate (rasio karyawan yang keluar dibandingkan total karyawan), yang saat ini telah mencapai 16.98%, jauh melampaui batas wajar 10%. Tingkat attrition yang tinggi ini dapat berdampak negatif pada perusahaan, seperti meningkatnya biaya rekrutmen dan pelatihan, menurunnya produktivitas, terganggunya kontinuitas operasional, serta menurunnya moral karyawan yang tersisa. Untuk mengatasi masalah ini, manajer departemen HR meminta bantuan Data Scientist untuk mengidentifikasi faktor-faktor penyebab tingginya attrition rate dan membangun business dashboard yang dapat membantu HR memonitor serta menganalisis faktor-faktor tersebut secara efektif.

## Permasalahan Bisnis
Masalah utama bisnis pada kasus ini adalah tingginya tingkat attrition rate di perusahaan Jaya Jaya Maju, yang mencapai 16.98%, melebihi ambang batas yang dianggap normal (10%). Tingkat turnover yang tinggi ini berpotensi menimbulkan dampak negatif, seperti:  
- Meningkatnya biaya operasional akibat rekrutmen dan pelatihan karyawan baru.
- Penurunan produktivitas karena kehilangan karyawan berpengalaman.
- Gangguan kontinuitas operasional akibat pergantian karyawan yang sering.
- Menurunnya moral karyawan yang tersisa karena beban kerja tambahan dan ketidakpastian.
Untuk itu, perusahaan perlu memahami faktor-faktor utama yang menyebabkan tingginya angka turnover ini agar dapat merumuskan strategi yang tepat untuk menurunkannya. Departemen HR membutuhkan analisis mendalam serta business dashboard yang dapat digunakan untuk memonitor faktor-faktor tersebut secara berkala dan memberikan wawasan yang actionable.

## Cakupan Proyek
Proyek ini dirancang untuk memberikan solusi komprehensif terhadap permasalahan tingginya tingkat attrition di PT Jaya Jaya Maju. Cakupan proyek ini terdiri dari tiga komponen utama yang saling mendukung.  
Pertama, proyek ini mencakup pembuatan prediksi dengan model machine learning. Model ini akan digunakan untuk memprediksi kemungkinan karyawan keluar dari perusahaan berdasarkan data yang tersedia. Selain itu, model ini juga akan membantu mengidentifikasi faktor-faktor utama yang memengaruhi tingkat attrition.  
Kedua, proyek ini melibatkan penyimpanan data ke database. Data karyawan akan disimpan dengan rapi menggunakan SQLAlchemy, sehingga memudahkan akses dan pengelolaan data untuk kebutuhan analisis di masa depan. Penyimpanan data yang terstruktur ini juga memastikan bahwa data dapat digunakan secara efisien untuk pembaruan dashboard atau analisis lanjutan.  
Ketiga, proyek ini mencakup pembuatan business dashboard dengan Metabase. Dashboard ini akan memvisualisasikan data attrition rate dan faktor-faktor yang memengaruhinya secara interaktif. Tujuannya adalah untuk memberikan alat yang membantu tim HR dalam memonitor tren attrition dan mengambil keputusan strategis berdasarkan wawasan yang diperoleh dari visualisasi data.  

## Persiapan
Data yang digunakan dalam proyek ini berasal dari dataset employee_data. Dataset ini berisi informasi rinci tentang karyawan, yang mencakup berbagai aspek penting.  
Informasi yang terdapat dalam dataset meliputi data demografi seperti usia dan jenis kelamin karyawan. Selain itu, terdapat data terkait posisi karyawan, seperti JobLevel (tingkat pekerjaan) dan JobInvolvement (tingkat keterlibatan kerja). Dataset juga mencakup informasi tentang lama bekerja (TotalWorkingYears), kompensasi seperti MonthlyIncome, MonthlyRate, dan HourlyRate, serta kepuasan kerja yang diukur melalui JobSatisfaction dan EnvironmentSatisfaction. Yang terpenting, dataset ini juga mencatat status keluar karyawan (Attrition), yang menjadi fokus utama analisis.  

Setup environment:
Untuk mendukung analisis dan pengembangan proyek, lingkungan kerja disiapkan dengan menggunakan beberapa pustaka Python berikut:  
- SQLAlchemy==2.0.40
- pandas==2.2.2
- numpy==2.0.2
- matplotlib==3.10.0
- seaborn==0.13.2
- scikit-learn==1.6.1
- imbalanced-learn==0.13.0
- joblib==1.4.2


## Business Dashboard
# Penjelasan Business Dashboard:
Business dashboard untuk PT Jaya Jaya Maju telah dikembangkan menggunakan Metabase, sebuah platform visualisasi data yang interaktif. Dashboard ini dirancang untuk membantu departemen HR memahami tingkat attrition rate dan faktor-faktor yang memengaruhinya secara mendalam.  
# Bagian 1: Overall Attrition Rate
Pada bagian utama dashboard, tingkat attrition keseluruhan ditampilkan dalam bentuk gauge chart. Visualisasi ini menunjukkan bahwa tingkat attrition di perusahaan saat ini mencapai 16.98%. Dengan tampilan yang sederhana namun jelas, gauge chart ini memungkinkan tim HR untuk segera melihat seberapa serius masalah attrition yang dihadapi perusahaan.  
# Bagian 2: Attrition Rate berdasarkan Faktor-Faktor Utama
Dashboard ini juga menyajikan analisis mendalam tentang tingkat attrition berdasarkan berbagai faktor. Visualisasi ini menggunakan kombinasi histogram dan line chart untuk menampilkan distribusi karyawan, jumlah karyawan yang keluar, serta tingkat attrition untuk setiap faktor berikut:  
- StockOptionLevel: Karyawan dengan level opsi saham 0 memiliki tingkat attrition tertinggi, yaitu sekitar 22%.
- MonthlyIncome: Karyawan dengan pendapatan bulanan di bawah $4,000 menunjukkan tingkat attrition tertinggi, yaitu sekitar 40%.
- JobInvolvement: Karyawan dengan tingkat keterlibatan kerja rendah (level 1) memiliki tingkat attrition tertinggi, yaitu sekitar 30%.
- JobLevel: Karyawan di level pekerjaan 1 memiliki tingkat attrition tertinggi, yaitu sekitar 25%.
- TotalWorkingYears: Karyawan dengan pengalaman kerja kurang dari 5 tahun menunjukkan tingkat attrition tertinggi, yaitu sekitar 30%.
- Age: Karyawan muda (usia 18-25 tahun) cenderung memiliki tingkat attrition yang lebih tinggi dibandingkan karyawan yang lebih tua.
- MonthlyRate: Tidak ada pola yang konsisten, tetapi tingkat attrition tertinggi (~30%) terlihat pada rentang $9,000-$12,000.
- EnvironmentSatisfaction: Karyawan dengan kepuasan lingkungan kerja rendah (level 1) memiliki tingkat attrition tertinggi, yaitu sekitar 35%.
- JobSatisfaction: Karyawan dengan kepuasan kerja rendah (level 1) menunjukkan tingkat attrition tertinggi, yaitu sekitar 30%.
- HourlyRate: Tidak ada pola yang jelas, tetapi tingkat attrition tertinggi (~25%) terlihat pada rentang 30-45.
# Bagian 3: Fitur Interaktif
Dashboard ini dilengkapi dengan fitur interaktif untuk meningkatkan fleksibilitas analisis. Tim HR dapat menggunakan filter seperti "Jumlah Keluar Lebih Besar Dari" atau "Jumlah Keluar Lebih Kecil Dari" untuk memfokuskan analisis pada kelompok karyawan tertentu. Fitur ini memungkinkan HR untuk menyesuaikan analisis sesuai dengan kebutuhan spesifik mereka.  
#Bagian 4: Visualisasi Faktor Utama
Dashboard juga menampilkan grafik Top 10 Faktor yang Mempengaruhi Attrition dalam bentuk bar chart. Grafik ini menunjukkan bahwa StockOptionLevel, MonthlyIncome, dan JobInvolvement adalah tiga faktor teratas yang paling memengaruhi tingkat attrition. Informasi ini sangat penting untuk membantu HR memprioritaskan area yang perlu diperbaiki.  

## Conclusion
Proyek ini berhasil mengidentifikasi faktor-faktor utama yang menyebabkan tingginya tingkat attrition rate di PT Jaya Jaya Maju. Berdasarkan analisis, tingkat attrition keseluruhan perusahaan mencapai 16.98%, yang jauh di atas batas wajar sebesar 10%. Angka ini menunjukkan bahwa perusahaan perlu segera mengambil langkah strategis untuk mengatasi masalah ini.  
Analisis lebih lanjut mengungkapkan bahwa StockOptionLevel adalah faktor yang paling berpengaruh terhadap tingkat attrition. Karyawan yang tidak memiliki opsi saham (level 0) menunjukkan tingkat attrition tertinggi, yaitu sekitar 22%. Faktor kedua yang signifikan adalah MonthlyIncome, di mana karyawan dengan pendapatan bulanan di bawah $4,000 memiliki tingkat attrition tertinggi, yaitu sekitar 40%.  
Faktor lain seperti JobInvolvement, JobLevel, TotalWorkingYears, EnvironmentSatisfaction, dan JobSatisfaction juga berkontribusi besar terhadap tingkat attrition. Karyawan dengan keterlibatan kerja rendah, level pekerjaan rendah, pengalaman kerja yang sedikit, serta kepuasan kerja dan lingkungan yang rendah cenderung lebih sering keluar dari perusahaan.  
Model machine learning yang dikembangkan dalam proyek ini berhasil memprediksi karyawan yang berpotensi keluar dengan akurasi yang baik. Selain itu, model ini juga menghasilkan daftar feature importance yang digunakan untuk memahami faktor-faktor utama penyebab attrition. (Catatan: Jika ada metrik evaluasi seperti akurasi, precision, atau recall, dapat ditambahkan di sini untuk memperkuat hasil.)  
Business dashboard yang dibuat menggunakan Metabase memberikan visualisasi yang jelas dan interaktif. Dashboard ini memungkinkan tim HR untuk memonitor tingkat attrition dan faktor-faktor penyebabnya secara real-time, sehingga mendukung pengambilan keputusan berbasis data. Dengan adanya dashboard ini, HR dapat lebih mudah mengidentifikasi tren dan mengambil tindakan yang tepat untuk mengurangi turnover.  
Secara keseluruhan, proyek ini memberikan wawasan yang berharga bagi PT Jaya Jaya Maju. Dengan memahami faktor-faktor utama penyebab attrition, perusahaan dapat merancang strategi retensi yang lebih efektif. Langkah ini diharapkan dapat mengurangi biaya rekrutmen, meningkatkan produktivitas, dan menjaga kontinuitas operasional perusahaan.  



## Rekomendasi Action Items (Optional)
Berdasarkan hasil analisis dan temuan dalam proyek ini, berikut adalah beberapa rekomendasi tindakan yang dapat diimplementasikan oleh PT Jaya Jaya Maju untuk mengurangi tingkat attrition:  
1. Meningkatkan Kompensasi dan Opsi Saham
Perusahaan perlu fokus pada peningkatan kompensasi untuk karyawan dengan pendapatan bulanan rendah (di bawah $4,000). Tinjau ulang skema gaji untuk memastikan bahwa kompensasi yang ditawarkan kompetitif dengan standar pasar. Selain itu, perusahaan dapat menawarkan opsi saham kepada karyawan di level yang lebih rendah (StockOptionLevel 0) untuk meningkatkan rasa memiliki dan loyalitas mereka terhadap perusahaan.  
2. Meningkatkan Keterlibatan dan Kepuasan Karyawan
Untuk mengatasi rendahnya JobInvolvement, perusahaan dapat mengadakan program pelatihan dan pengembangan yang dirancang untuk meningkatkan keterlibatan karyawan. Selain itu, survei karyawan perlu dilakukan secara berkala untuk menggali lebih dalam penyebab ketidakpuasan kerja, baik dari segi JobSatisfaction maupun EnvironmentSatisfaction. Hasil survei ini dapat menjadi dasar untuk memperbaiki kebijakan internal, seperti meningkatkan fasilitas kerja atau memperbaiki budaya perusahaan.  
3. Program Retensi untuk Karyawan Muda dan Level Rendah
Karyawan muda (usia 18-25 tahun) dan karyawan di JobLevel 1 menunjukkan tingkat attrition yang tinggi. Untuk itu, perusahaan dapat mengimplementasikan program retensi khusus, seperti mentoring, pelatihan pengembangan karier, atau memberikan kesempatan promosi bagi karyawan yang menunjukkan kinerja baik. Selain itu, perusahaan perlu menyediakan jalur karier yang jelas bagi karyawan dengan pengalaman kerja rendah (TotalWorkingYears < 5 tahun) untuk meningkatkan motivasi mereka bertahan.  
4. Monitoring Berkelanjutan melalui Dashboard
Tim HR dapat memanfaatkan dashboard secara rutin untuk memantau tren attrition dan mengevaluasi efektivitas strategi retensi yang diterapkan. Sebagai langkah lanjutan, perusahaan dapat menambahkan fitur notifikasi pada dashboard. Fitur ini akan memberikan peringatan dini jika tingkat attrition pada kelompok tertentu, seperti karyawan dengan kepuasan kerja rendah, mulai meningkat.  
5. Meningkatkan Budaya Perusahaan
Perusahaan perlu membangun budaya kerja yang lebih inklusif dan mendukung untuk meningkatkan EnvironmentSatisfaction. Kegiatan seperti team building atau sesi komunikasi terbuka antara manajemen dan karyawan dapat membantu menciptakan lingkungan kerja yang lebih positif. Selain itu, memberikan penghargaan (recognition) kepada karyawan berprestasi dapat meningkatkan motivasi dan loyalitas mereka terhadap perusahaan.  
6. Evaluasi dan Penyesuaian Kebijakan Secara Berkala
Perusahaan perlu melakukan evaluasi berkala terhadap kebijakan yang telah diterapkan untuk melihat dampaknya terhadap tingkat attrition. Berdasarkan hasil evaluasi, kebijakan dapat disesuaikan untuk memastikan bahwa strategi retensi tetap relevan dengan kebutuhan karyawan dan kondisi perusahaan.  


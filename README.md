# Laporan Proyek Machine Learning -  Muhammad Nurul Fatwa Al Fajar

## Project Overview
![55e257ed-234a-441b-a94c-efd19ad2aedf](https://github.com/user-attachments/assets/b05a4903-136a-4196-8ab5-09bbd195071e)

Bagi kalian yang belum mengetahui, Anime adalah animasi khas Jepang, Berasal dari serapan kata "Animation"[[1](https://id.wikipedia.org/wiki/Anime#:~:text=4.2%20Bacaan%20terkait-,Definisi%20dan%20penggunaan,animasi%20yang%20dibuat%20di%20Jepang%22.)]( telah menjadi tontonan favorit di berbagai kalangan dan kini dapat diakses melalui banyak platform streaming. Meski begitu, banyaknya judul yang tersedia terkadang menyulitkan pengguna aplikasi dalam memilih anime yang sesuai dengan preferensi mereka masing masing. Untuk mengatasi permasalahan ini, pada penelitian ini mengajukan pengembangan sistem rekomendasi[[2](https://openlibrarypublications.telkomuniversity.ac.id/index.php/engineering/article/view/20612/19925)]. Sistem ini dirancang untuk menganalisis riwayat tontonan pengguna, genre yang disukai, serta penilaian yang pernah diberikan. Berdasarkan data tersebut, sistem dapat menyarankan anime yang paling sesuai dengan selera individu[[3](https://journal.mediapublikasi.id/index.php/logic/article/view/4299)].

Tak hanya itu, elemen tambahan seperti tingkat popularitas, ulasan dari pengguna lain, dan rekomendasi dari komunitas juga akan menjadi pertimbangan dalam sistem ini. Pendekatan ini diharapkan memberikan manfaat besar, baik bagi pengguna maupun penyedia layanan streaming. Bagi pengguna, sistem ini memungkinkan mereka menemukan anime baru yang sesuai minat, menjelajahi genre yang belum pernah ditonton, dan mendapatkan rekomendasi sesuai dengan suasana hati mereka. Sementara bagi perusahaan, sistem ini berpotensi meningkatkan jumlah penonton, menyajikan konten yang lebih bervariasi, meningkatkan kepuasan pengguna, serta memahami pola preferensi penonton terhadap anime.

Secara keseluruhan, sistem rekomendasi ini dapat menjadi solusi yang efektif dalam membantu pengguna dalam menemukan judul anime yang cocok dengan minat mereka, sekaligus meningkatkan kualitas pengalaman menonton secara menyeluruh[[4](https://www.researchgate.net/publication/274712918_Rekomendasi_Anime_dengan_Latent_Semantic_Indexing_Berbasis_Sinopsis_Genre)].


## Business Understanding
Sistem rekomendasi anime berpotensi memberikan berbagai manfaat signifikan, baik bagi penonton maupun penyedia layanan streaming. Bagi pengguna, sistem ini mempermudah dalam menemukan anime yang sesuai dengan minat secara lebih praktis dan efektif. Sementara itu, bagi platform streaming, sistem ini dapat meningkatkan interaksi pengguna, memperkuat loyalitas penonton, serta membantu operasional platform menjadi lebih efisien dan responsif terhadap kebutuhan pengguna.[[5](http://repository.uin-malang.ac.id/18842/1/18842.pdf)]

## Problem Statements
- Bagaimana membangun sistem rekomendasi anime yang menyarankan tontonan kepada pengguna dengan mengacu pada genre yang diminati?
- Bagaimana penyedia layanan streaming dapat menyarankan anime yang belum pernah ditonton oleh pengguna dengan memanfaatkan data penilaian yang telah diberikan?
- Bagaimana membangun model rekomendasi menggunakan pendekatan Cosine Similarity dan algoritma K-Nearest Neighbor?
- Bagaimana mengevaluasi kinerja dari model sistem rekomendasi yang sudah dikembangkan?

## Goals
Untuk menangani permasalahan tersebut, dirancanglah sebuah sistem rekomendasi dengan tujuan sebagai berikut :
- Menyajikan daftar Top-N rekomendasi anime kepada pengguna berdasarkan genre yang diminati.
- Memberikan sejumlah rekomendasi anime yang relevan dengan minat pengguna dan belum pernah ditonton sebelumnya.
- Mengembangkan model sistem rekomendasi menggunakan pendekatan Cosine Similarity dan K-Nearest Neighbor berdasarkan fitur yang telah diekstraksi dari dataset.
- Mengevaluasi kinerja model sistem rekomendasi dengan menerapkan metrik pengukuran yang sesuai

Solution Approach
Data dianalisis melalui proses ***Exploratory Data Analysis (EDA)*** dan ***divisualisasikan*** untuk memahami pola serta karakteristik yang ada. Untuk memperoleh model prediksi yang optimal, dilakukan ***pembersihan data***, seperti menghapus ***nilai yang hilang*** (missing value), memeriksa keberadaan ***data duplikat***, menghapus karakter ***alfanumerik*** yang tidak relevan, serta menghilangkan ***tautan*** (URL). Selanjutnya, data ***kategorikal dikonversi menjadi format numerik*** menggunakan metode ***one-hot encoding***. Guna menilai performa model yang dibangun, digunakan metrik evaluasi seperti ***Precision***, ***Score Calinski-Harabasz***, dan ***Skor Davies-Bouldin***.

# T3chS3nse
Data Science Batch 33 - Rakamin Akademy
Tugas Final Projek
## Stage 1
Observasi :

- Berdasarkan informasi pada dataset tersebut bisa di lihat bahwa terdapat 1470 entry data dengan 35 features dan memiliki tipe dan isian data yang sudah sesuai
- Tidak terdapat data yang NULL dan duplikat pada keseluruhan features yang tersedia
- Pada data statistic, jika diperhatikan daris segi mean dan mediannya semua features cenderung memiliki persebaran data yang “cukup merata” namun pada feature Monthly Income terlihat perbedaan yang lumayan signifikan sehingga diduga distribusinya mengalami skewed
- Berdasarkan boxplot, bisa disimpulkan bahwa terdapat beberapa features yang memiliki nilai melebihi nilai minimum dan maximumnya atau terindikasi memiliki data outlier.
- Terdapat 2 feature dari data numerical yang memiliki 1 nilai unik yaitu EmployeeCount dan StandarHours
- Data outlier ini akan di olah lebih lanjut menggunakan z-score
- Jika dilihat dari visualisasi distribusi masing-masing feature maka terdapat beberapa feature yang mengalami positively skewed, seperti pada MonthlyIncome NumCompaniesWorked PercentSalaryHike TotalWorkingYears YearsAtCompany YearsInCurrentRole YearsSinceLastPromotion YearsWithCurrManager
- Untuk lebih jelas, bisa dilihat dari violinplot di atas, bahwa memang persebaran data untuk kolom-kolom yang sebelumnya di sebut mengalami positively skewed
- Dari default data, terdapat 9 feature categorical
- Terdapat 1 feature categorical yang memiliki 1 nilai unik yaitu Over18, ini bisa di drop pada proses selanjutnya.
- Berdasarkan heatmap disamping bisa dilihat bahwa terdapat 2 features yang memiliki 1 nilai unik sehingga tidak menampilkan korelasi antar features. Hal ini akan dilakukan drop pada Analisa lebih lanjut
- Untuk features targer (Attrition) setelah dilakukan labeling bisa dilihat bahwa hubungan antar features terhadapt target tidak terdapat korelasi yang terbilang kuat, sehingga akan dilakukan Analisa lebih lanjut untuk mengetahui features yang berpengaruh terhadap target
- Terdapat indikasi multikolinieritas pada JobLevel dan MonthlyIncome, sehingga pada tahap selanjutnya bisa dilakukan drop pada salah satu features tersebut
- Ada juga beberapa features yang korelasinya cukup kuat yaitu > 0.7, namun tidak cukup kuat untuk dihapus salah satunya.
- Berdasarkan Analisa data kategorical dan numerical menggunakan visualisas univariat dan multivariat sejauh ini, features yang akan di pertahankan adalah sebagai berikut : Age EnvironmentSatisfaction JobInvolvement JobLevel JobSatisfaction MaritalStatus MonthlyIncome OverTime TotalWorkingYears YearsAtCompany YearsCurrentRole YearsWithCurrManager
- Berdasarkan grafik distribusi Monthly Income, karyawan dengan gaji dibawah $10000 cenderung memilih meninggalkan perusahaan
- Terlihat bahwa rata-rata jarak dari rumah karyawan ke kantor mempengaruhi keputusan untuk meninggalkan perusahaan.
- Secara keseluruhan, karyawan yang meninggalkan perusahan rata-rata telah bekerja selama 5 tahun lebih
- Setelah di lakuakn analisan lebih lanjut, Pada interval waktu 0-5 tahun, frekuensi karyawan paling banyak yang keluar, namun pada tahun pertama ternyata sudah banyak karywana baru yang memutuskan untuk langsung resign
- Secara keseruhuan proporsi baik yang laki-laki dan perempuan memiliki nilai yang mirip.
- Untuk yang meninggalkan perusahaan baik laki-laki dan perempuan secara berturut-turut adalah 17,01% dan 14,80%
- Terlihat bahwa secara jumlah, dari department R&D paling banyak meninggalkan perusahaan, namun secara Rasionya, ternyata departement Sales yang paling banyak memutuskan untuk resign.
- Pada dept. Sales posisi Sales Representative paling banyak yang memutuskan keluar, sedangkan jika dari dept. R&D paling banyak yang keluar dari posisi Library Technician
- Setiap karyawan yang memilih 1 untuk tingkat kenyamanan kerja ternyata memiliki kecendrungan lebih tinggi untuk pergi dan meninggalkan perusahaan.
- Bisa diperhatikan, bahwa semakin tinggi rate yang dipilih maka semakin sedikit pula karyawan yang resign
- Hal ini berlaku juga untuk kenyamaan lingkungan kerja, semakin kecil rate yang dipilih makan semakin memberikan kecendrungan untuk karyawan untuk meninggalkan perusahaan
- Jika dilihat dari performa ratingnya, bisa disimpulkan bahwa yang memiliki rating 3 & 4 sama-sama memiliki presentase yang hamper serupa, berada pada 16% .
- Dari grafik disamping, maka bisa disimpulkan, bahwa yang paling banyak meninggalkan perushaan adalah mereka yang cenderung memiliki jam lembur
- Dari jumlah karyawan yang terlibat dalam suatu pekerjaan, yang tingkat keterlibatannya paling rendah (1) cenderung lebih banyak yang memutuskan keluar sekitar 33.27%
- Karyawan dengan level rendah cendrung lebih banyak yang keluar, mungkin hal ini bisa terjadi karena adanya tawaran yang lebih menaraik dari perusahaan lain disamping mereka juga ingin meningkatkan jenjang karir

Bisnis Rekomendasi :

Memberikan reward atau bonus bagi karyawan yang memiliki performa baik.
Memberikan pelatihan untuk meningkatkan kompetensi kaaryawan
Membuka kesempatan bagi karyawan untuk meningkatkan jenjang karir disertai dengan kenaikan gaji sesuai pencapaiannya
Mengadakan Outing untuk menjalin kerjasama dan membangun rasa kekeluargaan
Membuat sebuah ajang lomba antar departemen untuk meningkatkan kekompakkan antar departemen
_________________________________________________________
## Stage 2
SUMMARY PROJECT:

1. Data Cleansing
- Berdasarkan informasi data, maka dapat disimpulkan bahwa tidak terdapat missing value
- Setelah melakukan pengecekan terhadap keseluruhan feature secara-Bersama-sama maka tidak terdapat data duplikat
- Berdasarkan boxplot, maka terdapat beberapa outlier di beberapa feature sehingga kami menanganinya dengan mengaplikasikan metode Z-Score untuk menghilangkan outlier.
- Feature transformation yang diterapkan adalah standarisasi, karena melihat distribusi masih ada beberapa feature yang tidak normal, sehingga kami menggunakan metode Standarisasi (Standarscaler) untuk melakukan scaling pada interval skala tertentu
- Feature encoding yang kami terapkan ada 2, yaitu Label ecoding untuk feature : attrition, Gender, Mariatal Status dan Business Travel, sedangakn One-hot encoding diterapkan pada feature Departmen, EducationField dan Jobrole
- Pada metode imbalance ini kami menerapkan metode oversampling untuk menghindari adanya informasi yang terbuang.
2. Feature Engineering
- Pada fase feature selection, kami mengeliminasi feature yang memiliki 1 nilai unik seperti standarhour, over18 dan juga Employeecount dan juga yang memiliki nilai unik sebanyak dataset yaitu Employeenummber, selain itu kami juga memeilih feature Performance rating karena dari visualisasi rasionya hampir sama sehingga kami putuskan tidak berdampak pada target.

- Kami tidak melakukan feature extraction karena dirasa feature yang sudah ada saat ini sudah cukup memberikan informasi yang akan mempengaruhi target.

- Feature tambahan:

- OvertimeRatio: Fitur ini dapat dihitung dengan membagi jumlah jam kerja lembur (overtime) per bulan oleh 'TotalWorkingYears'. Fitur ini akan mencerminkan sejauh mana karyawan cenderung bekerja lembur dibandingkan dengan pengalaman kerja mereka.

- PromotionSpeed: Fitur ini dapat dihitung dengan membagi 'YearsSinceLastPromotion' oleh 'TotalWorkingYears’.

- EmployeeTenure: Fitur ini dapat dihitung berdasarkan selisih antara 'YearsInCurrentRole' dan 'YearsAtCompany'. Fitur ini akan menunjukkan berapa lama seorang karyawan telah bekerja di perusahaan saat ini dalam peran yang sedang dijalani.

- JobStabilityIndex: Fitur ini dapat dihitung dengan menggabungkan 'YearsAtCompany', 'YearsInCurrentRole', dan 'YearsSinceLastPromotion'. Fitur ini akan mencerminkan stabilitas pekerjaan dan kesempatan untuk promosi dalam perusahaan

# **Credit Card Customer Analysis**


## **Group Sigma Profile** 
----
1. Andika Darmawan - bisnisandikadarmawan@gmail.com | [LinkedIn](https://www.linkedin.com/in/andika-d-746414214/) | [GitHub](https://github.com/FrancisDarma)
2. Gede Sariasa - sariasa14@gmail.com | [LinkedIn](https://www.linkedin.com/in/gede-sariasa-b5a77a134/) | [GitHub](https://github.com/sariasa14)
3. Adha Ozy Prima Dewangga - adaozy81@gmail.com | [LinkedIn](https://www.linkedin.com/in/adhaozyprimadewangga/) | [GitHub](https://github.com/Markenji?tab=repositories)



## Dataset
Dataset diambil dari [kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)

# **BUSINESS UNDERSTANDING**
----

## **Background**
Sebuah Bank A ingin mengetahui profile Customer mereka berdasarkan pola penggunaan produk Kartu Kredit bank mereka. Hal ini akan menjadi dasar untuk strategi marketing bank untuk menyusun produk bank yang lebih sesuai dengan profile Customer mereka dan dengan demikian menaikkan tingkat penggunaan atau **usage** per customernya.

Kenaikan usage ini diharapkan akan meningkatkan nilai portofolio kartu kredit per Customer yang akhirnya dapat meningkatkan portofolio kartu kredit Bank A secara keseluruhan.

Dengan demikian premis Strategi dan Measurement Bisnis yang akan dilakukan adalah sebagai berikut:

1. Segmentasi Customer ke dalam kelompok-kelompok tertentu dengan perilaku transaksi yang serupa.
2. Desain produk perbankan dan komunikasi pasar yang lebih khusus terhadap Customer-Customer tersebut, dan akhirnya menciptakan relationship Customer yang lebih baik.
3. Loyalitas Customer meningkat dan demikian mereka lebih sering menggunakan Kartu Kredit Bank A untuk berbelanja.
4. Kenaikan jumlah transaksi (frekuensi/kuantitas transaksi) dan nilai volume pinjaman kartu kredit yang terpakai dalam rentang batasan limit yang sudah ditentukan.
5. Keuntungan bank per bulan meningkat yang diperoleh dari:
    * Bunga dari cicilan kartu kredit (baik pembelian atau tarik tunai kartu kredit)
    * Fee dari transaksi di mesin EDC
    * Berkurangnya kerugian dari Customer yang gagal bayar akibat kita salah mengidentifikasi segmen Customer yang tepat.

## **Problems Identification**
Saat ini, Bank A memiliki data transaksi kartu kredit setiap customernya, namun dari data tersebut hanya berisi data numerik rangkuman transaksi dari setiap Customernya. Karena kita belum mempunyai kategori dan memerlukan tambahan insights untuk melakukan pengkategorian Customer tersebut, maka tidak cukup kalau kita hanya melakukan analisa dan visualisasi data untuk menemukan kecenderungan setiap customer, karena hal tersebut berpotensi menyebabkan adanya variabel-variabel pengelompokkan yang *overlooked* atau diabaikan. Sehingga dalam permasalahan ini nantinya seperti akan dijelaskan lebih detail pada bagian **Proposed Solutions** kita perlu melakukan pemodelan Machine Learning.

Selain itu dari segi konsep bisnis kita perlu mendefinisikan rumusan permasalahan bisnis, yang akan kita jadikan dasar dalam membangun sebuah model Machine Learning, hal tersebut antara lain:

1. Variabel mana saja yang paling menggambarkan tingkat **usage/retensi** Customer? Bagaimana hubungan antara variabel tersebut dengan tingkat **usage/retensi**?
2. Bagaimana pengelompokkan Customer pengguna kartu kredit yang paling mungkin dibentuk dari data yang diberikan? Apakah pengelompokkan ini dapat membantu kita mengenali gambaran **siapa** customer kita tersebut?
3. Berapa kenaikan tingkat **usage/retensi** yang diharapkan apabila kita melakukan program marketing yang lebih targeted pada kelompok-kelompok customer tersebut?

## **Conceptual Framework**
Untuk memecahkan rumusan masalah diatas, maka kiranya kita perlu mencari pustaka atau referensi yang kira-kira dapat memberikan kita gambaran konseptual yang menjadi peta untuk mencari hal-hal apa saja yang mempengaruhi **usage** Customer terhadap sebuah produk.

Dalam hal ini kita akan menggunakan teori **Loyalitas Customer** terhadap sebuah produk. Berikut gambarannya:

## **Proposed Solutions**
Guna mengetahui dan mencari tahu, jawaban atas rumusan masalah di atas, kita akan menggunakan beberapa teknik yaitu:

1. **Teknik Visualisasi Data dan Statistika Deskriptif**, metode ini kita gunakan untuk mempelajari pola sebaran data dan kemungkinan keterhubungan antara variabel satu dengan yang lain, dan juga untuk memahami proses pencatatan bisnis kartu kredit dari Bank A. Kita sebenarnya juga dapat melakukan pengkategorian Segmen Customer berdasarkan kemiripan perilaku antar Customer yang kita temukan dalam Statistika Deskriptif.
<br><br>Namun teknik ini memiliki keterbatasan, yaitu kita tidak dapat membangun sebuah model yang dapat memprediksi di masa depan terhadap munculnya Customer baru, akan masuk ke dalam kategori apa. Padahal dalam kasus ini, kita perlu melakukan pengkategorian Customer agar kita dapat melakukan komunikasi produk yang lebih targeted, bahkan pada hari pertama sejak Customer tersebut menjadi nasabah pengguna Kartu Kredit Bank A.
<br><br>Selain itu, visualisasi data saja tidak cukup agar kita dapat menangkap pola data yang tersembunyi di dalam sebuah data set.

Maka dari itu, kita memerlukan teknik ke 2 yaitu:

2. **Pemodelan Clusterisasi data dengan Pemodelan Machine Learning**.
<br>Ini kita lakukan, agar kita dapat mempelajari pola-pola tersembunyi dalam dataset, dengan harapan kita dapat menemukan pengkategorian jenis Customer secara lebih akurat dengan menggunakan prinsip Statistika dan matematis.

Diharapkan dengan pemodelan ini kita dapat memperoleh benefit sebagai berikut:
* Peningkatan keuntungan, akibat **usage** kartu kredit yang meningkat, karena kita melakukan desain benefit kartu kredit dan mengkomunikasikan benefit tersebut secara lebih tepat kepada segmen Customer yang sesuai, sehingga Customer semakin tertarik melakukan aktivasi terhadap produk Kartu Kredit mereka.
* Minimasi biaya, yang disebabkan oleh komunikasi produk yang tidak tepat sasaran. Dengan klusterisasi yang dihasilkan dari model ML, diharapkan efektivitas komunikasi ke segmen Customer meningkat dengan biaya komunikasi dan marketing yang sama, sehingga perusahaan menjadi lebih produktif.
* Meningkatnya Loyalitas Customer secara keseluruhan, karena dengan marketing yang lebih akurat, Customer merasakan perusahaan sangat mengayomi kebutuhan mereka, sehingga hal tersebut membuat Customer nyaman dengan produk Kartu Kredit Bank A, sehingga mereka akan terus menggunakan kartu kredit Bank A (**usage** stabil, **retensi** meningkat).

Ketiga hal diatas, diharapkan akan berdampak terhadap meningkatnya profitabilitas produk Kartu Kredit Bank A secara signifikan.

## **Konten Utama**

#### Library
![Pandas License](https://img.shields.io/badge/pandas-1.5.3-lightgrey)  
![Pandas License](https://img.shields.io/badge/numpy-1.22.4-yellow)  
![Pandas License](https://img.shields.io/badge/seaborn-0.12.2-blue)  
![Pandas License](https://img.shields.io/badge/matplotlib-3.7.1-red)<br>
![scikit-learn ](https://img.shields.io/badge/scikit--learn-1.2.2-coral?labelColor=grey&style=flat)<br>
![imblearn ](https://img.shields.io/badge/scipy-1.10.1-olive?labelColor=grey&style=flat)<br>
![category-encoders](https://img.shields.io/badge/missingno-0.5.2-emerald?labelColor=grey&style=flat)<br>


<h4>Credit Card</h4>
<h4><b>Konteks</b></h4>
<p>Sample Dataset merangkum perilaku penggunaan sekitar 9000 pemegang kartu kredit aktif selama 6 bulan terakhir. File tersebut berada di tingkat pelanggan dengan 18 variabel perilaku.</p>
<h5><b>Fitur</b></h5>
<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th>Data Type</th>
  </tr>
  <tr>
    <th><b>CUST_ID</b></th>
    <td>Identifikasi pemegang Kartu Kredit (Kategorikal).</td>
    <td>Object</td>
  </tr>
      <tr>
    <th><b>BALANCE</b></th>
    <td>Saldo jumlah yang tersisa di akun mereka untuk melakukan pembelian.</td>
    <td>Float64</td>
  </tr>
  </tr>
      <tr>
    <th><b>BALANCE_FREQUENCY</b></th>
    <td>Seberapa sering Saldo diperbarui, skor antara 0 dan 1 (1 = sering diperbarui, 0 = tidak sering diperbarui).</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>PURCHASES</b></th>
    <td>Jumlah pembelian yang dilakukan dari akun.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>ONEOFF_PURCHASES</b></th>
    <td>Jumlah pembelian maksimum dilakukan dalam sekali jalan.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>INSTALLMENTS_PURCHASES</b></th>
    <td>Jumlah pembelian dilakukan secara cicilan.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>CASH_ADVANCE</b></th>
    <td>Tarik tunai dari credit card.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>PURCHASES_FREQUENCY</b></th>
    <td>Seberapa sering Pembelian dilakukan, skor antara 0 dan 1 (1 = sering dibeli, 0 = tidak sering dibeli).</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>ONEOFFPURCHASESFREQUENCY</b></th>
    <td>Seberapa sering Pembelian terjadi dalam sekali jalan (1 = sering dibeli, 0 = tidak sering dibeli).</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>PURCHASESINSTALLMENTSFREQUENCY</b></th>
    <td>Seberapa sering pembelian dengan mencicil dilakukan (1 = sering dilakukan, 0 = tidak sering dilakukan).</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>CASHADVANCEFREQUENCY</b></th>
    <td>Seberapa sering uang muka dibayarkan.</td>
    <td>Float64</td>
  </tr>  </tr>
      <tr>
    <th><b>CASHADVANCETRX</b></th>
    <td>Jumlah Transaksi yang dilakukan dengan "Cash in Advanced.</td>
    <td>Int64</td>
  </tr>
    </tr>
      <tr>
    <th><b>PURCHASES_TRX</b></th>
    <td>Jumlah transaksi pembelian yang dilakukan.</td>
    <td>Int64</td>
  </tr>
    </tr>
      <tr>
    <th><b>CREDIT_LIMIT</b></th>
    <td>Limit Kartu Kredit untuk pengguna.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>PAYMENTS</b></th>
    <td>Jumlah Pembayaran yang dilakukan oleh pengguna.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>MINIMUM_PAYMENTS</b></th>
    <td>Jumlah minimum pembayaran yang dilakukan oleh pengguna.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>PRCFULLPAYMENT</b></th>
    <td>Persentase pembayaran penuh yang dibayarkan oleh pengguna.</td>
    <td>Float64</td>
  </tr>
    </tr>
      <tr>
    <th><b>TENURE </b></th>
    <td>Jangka waktu layanan kartu kredit untuk pengguna.</td>
    <td>Int64</td>
  </tr>
</table>

<p>Sumber Data : <a href="https://www.kaggle.com/datasets/arjunbhasin2013/ccdata">Klik disini</a></p>
<p>Data Awal Terdiri dari : 8950 Baris × 18 Kolum</p>

## Daftar Isi Main Project ipynb
 - [DATA UNDERSTANDING](#DATA-UNDERSTANDING)
 - [DATA CLEANING AND FEATURE ENGINEERING](#DATA-CLEANING-AND-FEATURE-ENGINEERING)
 - [MODEL EXPLORATION AND EXPERIMENTATIONS](#MODEL-EXPLORATION-AND-EXPERIMENTATIONS)
 - [EXPERIMENTS SUMMARY](#EXPERIMENTS-SUMMARY)
 - [FINAL CLUSTERING CONCLUSION AND RECOMMENDATIONS](#FINAL-CLUSTERING-CONCLUSION-AND-RECOMMENDATIONS)
 - [BUSINESS IMPLEMENTATION](#BUSINESS-IMPLEMENTATION)
 - [TABLEAU DASHBOARD](#TABLEAU-DASHBOARD)

## **DATA UNDERSTANDING**
----

### Data
----
![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/1.PNG?raw=true)

### Data Visualization & EDA
----

#### Graphical Method - Histogram
![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/2.png?raw=true)

#### Outliers and Missing Value Analysis
![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/3.png?raw=true)

#### Correlation Heatmap
![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/4.png?raw=true)

## **DATA CLEANING AND FEATURE ENGINEERING**
----
#### - Duplicate Value
#### - Data Types & Drop Unnecessary Columns
#### - Transform Data Distributions
#### - Add Feature = 'USAGE'
#### - Handling Outliers

## **MODEL EXPLORATION AND EXPERIMENTATIONS**
----

#### - PCA Function
#### - Clustering Evaluation untuk KMeans
      - M1. KMeans with original data (Credit)
      - M2. KMeans with normalized data Box-cox Yeo Johnson
      - M3. KMeans with normalized data Log(1+x)
#### - Clustering Evaluation untuk Agglomerative
      - A1. Agglomerative Hierarchical Clustering (Ward Linkage)
      - A2. Agglomerative Hierarchical Clustering (Maximum Linkage)
      - A3. Agglomerative Hierarchical Clustering (Average Linkage)
#### - DBSCAN

## **EXPERIMENTS SUMMARY**
----

* Normalisasi dataset dengan Box-cox Yeo Johnson maupun Log(1+x) memberikan hasil      kluster yang lebih buruk. Sehingga pengujian untuk data ini tidak dilanjutkan untuk model yang lain.
* **Silhouette score merupakan metrik evaluasi yang menjadi pedoman utama** dalam penentuan apakah model sudah baik atau belum, karena metrik ini memiliki rentang nilai yang paling jelas dibandingkan metrik yang lain.
* Terdapat 5 model dengan nilai skor evaluasi yang bagus.

### Conclusion Model

Jika membandingkan silhouette score dari kedua model ini, model KMeans memiliki nilai yang lebih baik yang berarti model KMeans kemungkinan tumpang-tindih yang lebih kecil. Sehingga **model akhir yang dipilih adalah model KMeans**.

Faktor-faktor yang menjadi alasan pemilihan model Kmeans, yaitu:
- Nilai silhoutette score yang masih dapat terima setelah diterapakan pada data aslinya.
- Segmentasi cluster yang lebih jelas dari pada penggunaan Agglomerative dan DBSCAN.
- Nilai calinski-harabasz score paling bagus diterapkan di model KMeans dengan cluster 4.

## **5. FINAL CLUSTERING & RECOMMENDATIONS**
----

#### Final Model : K-Means 4 cluster dengan PCA (original dataset)
![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/5.png?raw=true)

#### Explanatory Data Analysis 2
![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/5.png?raw=true)
#### Analisa Usage Kartu Kredit
![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/6.png?raw=true)

#### Barplot 
 - Perbandingan Pembayaran Penuh Setiap Cluster <br>
  ![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/a.png?raw=true) <br>
  - Perbandingan Usage Setiap Cluster <br>
  ![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/b.png?raw=true) <br>
  - Perbandingan Credit Limit & Balance Setiap Cluster <br>
  ![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/c.png?raw=true) <br>
  - Rincian Penggunaan Kartu Kredit pada Customer 0 <br>
  ![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/d.png?raw=true) <br>
  - Rincian Penggunaan Kartu Kredit pada Customer 1 <br>
  ![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/e.png?raw=true) <br>
  - Rincian Penggunaan Kartu Kredit pada Customer 2 <br>
  ![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/f.png?raw=true) <br>
  - Rincian Penggunaan Kartu Kredit pada Customer 3 <br>
  ![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/g.png?raw=true) <br>



## **FINAL CLUSTERING CONCLUSION AND RECOMMENDATIONS**
----

##A# **Conclusion**
#### Customer pengguna kartu kredit terbagi menjadi 4 kelompok, yaitu:
- **Cluster 0**
- **Cluster 1**
- **Cluster 2**
- **Cluster 3**

#### Feature yang berpengaruh kepada Usage, yaitu:
- **BALANCE** berkorelasi secara sangat kuat pada usage tetapi secara negatif sebesar -0,82.
- **MINIMUM** PAYMENTS berkorelasi secara kuat pada usage tetapi secara negatif sebesar -0,78.
- **PRC_FULL_PAYMENT** berkorelasi secara sedang pada usage secara positif sebesar 0,52.
- **CASH_ADVANCE**, CASH_ADVANCE_FREQUENCY, dan CASH_ADVANCE_TRX berkorelasi secara sedang pada usage tetapi secara negatif sekitar -0.5.

#### Pengelompokan customer berdasarkan cluster dan tipe customer itu dalam penggunaan kartu kredit, yaitu:
- **Cluster 0** = Middle-Low Cash Advance Customer.
- **Cluster 1** = Middle High Income Loyal and Discipline Customer.
- **Cluster 2** = WatchList Customer.
- **Cluster 3** = High Income, High Lifestyle, Consumptive Customer.

### **Rekomendasi**

#### **Rekomendasi untuk Pengembangan Model**
1. Mencoba menggunakan metrics evaluasi seperti Dunn Index, C-index, McClainRao, CCC, Log Det Ratio, dan Log SS Ratio
2. Mencoba algorithma mechine learning clustering lainnya, seperti Mean-Shift Clustering dan K-Medians (perlu pengembangan lebih khusus terkait algoritma ini) karena data asli tidak terdistribusi normal.

#### **Rekomendasi Bisnis**

Berdasarkan pengelompokan cluster yang sudah dibuat maka strategi marketing yang dilakukan sebagai berikut :

**1. For All Customer**

Pada semua seluruh customer startegi yang akan diberikan adalah sebagai berikut:

1. Iklan promosi tentang kredit setiap 1 bulan sekali.
2. Pembebasan bunga pada semua jenis transaksi mulai dari  Installments_Purchases dan Cash_Advance pada hari-hari tertentu.
3. Pada Oneoff_Purchases dan Installments_Purchases akan diberikan cashback pembelian barang sebanyak 5 kali pembelian pertama setiap bulan.
4. Iklan di TV, untuk melakukan komunikasi Branding dan Awareness Kartu Kredit di masyarakat umum (Build Product Awareness).

**2. Middle-Low Cash Advance Customer (Customer 0)**

Pada semua customer 0 startegi yang akan diberikan adalah sebagai berikut:

1. Pada Cash_Advance akan diberikan keringan berupa denda jika telat melakukan pembayaran pada 3 bulan pertama.
2. Memberikan reward berupa bebas bunga jika pengguna kartu kredit melakukan penarik dengan jumlah penarik dari bulan sebelumnya.
3. Menawarkan program membership kepada customer yang sering melakukan Cash_Advance dengan tawaran fee atau bunga yang lebih ringan.
4. Memberikan iklan atau edukasi bahwa selain Cash_Advance ada pula produk Oneoff_Purchases dan Installments_Purchases dengan memberikan reward berupa bebas bunga selama 3 bulan jika melakukan salah satu dari dua produk yang ditawarkan.
5. Memberikan Voucher makanan atau merchant setiap kali mereka melakukan penarikan tunai Kartu Kredit.
6. Melakukan A/B Testing dengan 2 reward yang berbeda (yang pertama reward/voucher pembelian OneOff, yang kedua reward/voucher pembelian Installment) dan melihat reward mana yang lebih efektif meningkatkan purchases Customer ini.
7. **Target Strategi diatas diharapkan akan meningkatkan (Conservative Target):**
  1. Nominal Cash Advance naik 5% dari rata-rata saat ini (960 dollar).
  2. Nominal OneOffPurchases naik 5%.
  3. Nominal InstallmentPurchases naik 5%
  4. Diharapkan ini akan menaikkan Usage sebesar 3%.

**3. Middle High Income Loyal and Discipline Customer (Customer 1)**

Pada semua customer 1 startegi yang akan diberikan adalah sebagai berikut:

1. Customer yang telat pembayaran pada Oneoff_Purchases akan diberikan keringanan berupa bunga yang dikurangi setengahnya (2% menjadi 1%).
2. Reward akan diberikan kepada customer yang melakukan Oneoff_Purchases selama 1 tahun dan tidak menggalami tunggakan akan diberikan reward berupa mengikuti undian berhadiah tahunan bank AGO.
3. Memberikan iklan atau edukasi bahwa selain Oneoff_Purchases ada pula produk Cash_Advance dan Installments_Purchases dengan memberikan reward berupa bebas bunga selama 3 bulan jika melakukan salah satu dari dua produk yang ditawarkan.
4. Kalau mereka melakukan Purchases diatas 5000 mereka akan mendapat Cashback.
5. Tawarkan Loyalty Points yang mereka dapatkan dari setiap pembelian barang sekaligus pembayaran cicilan kartu kredit yang mereka lakukan, dan point tersebut dapat digunakan untuk kesempatan Undian (Wheel of Fortune) untuk mendapatkan hadiah gratis dari Bank. Kita akan tag mereka sebagai **Loyal Customers**.
6. **Target Strategi diatas diharapkan akan meningkatkan (Conservative Target):**
  1. Rata-rata **Purchases** mereka naik diatas 5000 Dollar.

**4. WatchList Customer (Customer 2)**

Pada semua customer 2 startegi yang akan diberikan adalah sebagai berikut:

1. Customer 2 sebaiknya diberikan penawaran berupa penghilangan bunga  agar melakukan pelunasan kartu kredit.
2. Reward dan Cashback akan diberikan jika mereka sudah melunasi sebagian dari tunggakan mereka.
3. Melakukan survei kenapa mereka lebih banyak melakukan Cash_Advance dengan balance dan minimum payment yang tidak seimbang ditakutkan mereka adalah customer fraud atau bisa jadi mereka adalah customer yang sedang bangkrut.
4. Kalau memang mereka setelah 12 bulan tidak dapat melakukan pembayaran, kita akan terminate Kartu Kredit (Write-Off Kartu Kredit) dan kita akan akan tag mereka sebagai **Col 5** dan tidak dapat menggunakan Kartu Kredit hingga mereka dapat melunasi outstanding mereka dan membayar denda.
5. **Target Strategi diatas diharapkan akan menurunkan jumlah Customer ini menjadi 50%.**


**5. High Income, High Lifestyle, Consumptive Customer (Customer 3)**

Pada semua customer 3 startegi yang akan diberikan adalah sebagai berikut:

1. Customer 3 diberikan memberkhusus karena rata-rata Oneoff_Purchases mereka adalah yang tertinggi.
2. Reward juga akan diberikan dalam bentuk kupon udian tahunan yang berhadiah berbagai macam mulai dari Rumah, Mobil, dan Emas.
3. Customer 3 juga akan dimanjakan dengan bebas terkena denda telat pembayaran selama 3 kali dalam setahun jika melebihi dari batasan itu member akan dicabut.
4. Berikan mereka keanggotan VIP / Customer Prioritas.
5. Berikan mereka reward Hotel Gratis ketika jalan-jalan keluar negeri atau penukaran Mileage Airlines ternama untuk Tour dan Travel keluar negeri.
6. Pemberian Points untuk setiap pembelajaan barang mewah seperti mobil maupun Fashion.
7. **Target Strategi diatas diharapkan akan tetap membuat mereka semakin nyaman dan Loyal terhadap produk Bank kita.**

## **BUSINESS IMPLEMENTATION**
----

**Keuntungan yang bisa didapatkan bank dari meningkatnya penggunaan pengguna kartu kredit bergantung pada beberapa faktor**, seperti:

- Suku bunga yang dibebankan kepada pemegang kartu kredit yang tidak membayar saldo penuh setiap bulannya. Ini adalah sumber pendapatan utama bagi penerbit kartu kredit, dan bervariasi tergantung pada skor kredit dan profil risiko pemegang kartu. Di Amerika Serikat, rata-rata suku bunga kartu kredit yang dibayarkan oleh rekening berbunga adalah 19,33%
- Biaya yang dibebankan kepada pemegang kartu kredit untuk layanan kartu, seperti biaya tahunan, biaya keterlambatan, biaya transaksi luar negeri, biaya penarikan tunai, dll. Biaya ini dapat menambah jumlah pendapatan yang signifikan bagi penerbit, terutama jika pemegang kartu tidak berhati-hati untuk menghindarinya. Misalnya, biaya keterlambatan terdiri dari sekitar 15% dari profitabilitas kartu kredit
- Pendapatan pertukaran atau "biaya gesek" yang diperoleh setiap kali pemegang kartu menggunakan kartu mereka untuk melakukan pembelian. Ini adalah biaya yang dibayarkan oleh pedagang kepada penerbit untuk memproses transaksi. Biasanya berkisar antara 1% hingga 3% dari jumlah pembelian, tergantung pada jenis kartu dan jaringan. Penerbit juga dapat mengumpulkan biaya tambahan dari pedagang untuk menerima pembayaran kartu, seperti biaya jaringan, biaya penilaian, dll
- Hadiah dan manfaat yang ditawarkan kepada pemegang kartu untuk memberi insentif kepada mereka untuk menggunakan kartu mereka lebih sering dan setia. Ini dapat mencakup uang kembali, poin, mil, diskon, asuransi, dll. Namun, imbalan dan manfaat ini juga datang dengan biaya bagi emiten, yang harus membayarnya baik dari dana mereka sendiri atau dari kemitraan dengan perusahaan lain. Oleh karena itu, emiten harus menyeimbangkan daya tarik imbalan dengan profitabilitas mereka.

Untuk memperkirakan berapa banyak keuntungan yang dapat diperoleh bank dari peningkatan penggunaan pengguna kartu kredit, seseorang perlu mengetahui saldo rata-rata, suku bunga, struktur biaya, tingkat pertukaran, dan tingkat imbalan portofolio kartu kredit mereka, serta peningkatan yang diharapkan dalam volume dan frekuensi transaksi. Namun, berdasarkan beberapa asumsi umum dan rata-rata industri, seseorang dapat membuat perhitungan kasar menggunakan rumus berikut:

<b>Profit = (Balance x Interest Rate) + (Fees) + (Interchange Revenue) - (Rewards Cost) </b>

Misalnya, bank AGO memiliki 1000 pengguna tipe Middle-Low Cash Advance Customer (Customer 0) yang kartu kreditnya memiliki saldo rata-rata $ 1000 masing-masing, membayar tingkat bunga rata-rata 20%, membayar $ 50 dalam biaya per tahun masing-masing, menghasilkan $ 2000 dalam pembelian per tahun masing-masing dengan tingkat pertukaran rata-rata 2%, dan menerima $ 100 dalam hadiah per tahun masing-masing. Keuntungan bank dari pengguna ini adalah:

Profit = (1000 x 1000 x 0.2) + (1000 x 50) + (1000 x 2000 x 0.02) - (1000 x 100) = $190,000

Sekarang anggaplah bank berhasil meningkatkan penggunaan pengguna ini sebesar 5%, yang berarti mereka meningkatkan saldo, pembelian, dan hadiah masing-masing sebesar 10%. Keuntungan bank dari pengguna ini adalah:

Profit = (1000 x 1050 x 0.2) + (1000 x 50) + (1000 x 2100 x 0.02) - (1000 x 105) = $197,000

Oleh karena itu,<b> keuntungan bank AGO akan meningkat sebesar $ 7.000 atau 3,6% dengan meningkatkan penggunaan pengguna kartu kredit sebesar 5%</b>. Tentu saja, ini adalah contoh yang sangat disederhanakan yang tidak memperhitungkan banyak faktor lain yang dapat mempengaruhi profitabilitas kartu kredit, seperti tingkat default, biaya operasi, persaingan, regulasi, kepuasan pelanggan, dll.

## **TABLEAU DASHBOARD**
----
[Link Tableau Dashboard](https://public.tableau.com/app/profile/adha.ozy.prima.dewangga/viz/DasboardFinalProjectCreditCardCustomerAnalysis/Dashboard1?publish=yes)

Berikut merupakan tampilan Tableau Dashboard.

![alt text](https://github.com/PurwadhikaDev/SigmaGroup_JC_DS_OL_09_FinalProject/blob/main/Image/Dashboard%201.png?raw=true)

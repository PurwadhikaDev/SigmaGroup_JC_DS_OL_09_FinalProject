# **Credit Card Customer Analysis**
Final Project


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
 - [DATA UNDERSTANDING](#Data-Understanding-dan-Data-Cleaning)
 - [DATA CLEANING & FEATURE ENGINEERING](#Data-Understanding-dan-Data-Cleaning)
 - [MODEL EXPLORATION AND EXPERIMENTATIONS](#Data-Analysis)
 - [EXPERIMENTS SUMMARY](#Feature-selection-dan-Feature-Engineering)
 - [FINAL CLUSTERING, CONCLUSION & RECOMMENDATIONS](#Conclusion-and-Recommendation)
 - [BUSINESS IMPLEMENTATION](#BUSINESS-IMPLEMENTATION)

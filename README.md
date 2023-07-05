# **Credit Card Customer Analysis**
Final Project


## **Group Sigma Profile** 
----
1. Andika Darmawan - bisnisandikadarmawan@gmail.com | [LinkedIn](https://www.linkedin.com/in/andika-d-746414214/) | [GitHub](https://github.com/FrancisDarma)
2. Gede Sariasa - sariasa14@gmail.com | [LinkedIn](https://www.linkedin.com/in/gede-sariasa-b5a77a134/) | [GitHub](https://github.com/HerdiansyahPP)
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

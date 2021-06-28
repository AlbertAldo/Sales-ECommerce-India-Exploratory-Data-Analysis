# Sales-ECommerce-India-Exploratory-Data-Analysis

# EDA (Exploratory Data Analysis) - Sales E-Commerce India

 **Exploratory Data Analysis** pada Dataset Sales E-Commerce India pada April 2018 - Maret 2019 untuk mendapatkan Informasi / Insight yang dibutuhkan berdasarkan data transaksi penjualan E-Commerce India yang diperoleh dan memberikan Rekomendasi yang dapat diberikan melalui Insight yang didapatkan.

EDA (Exploratory Data Analysis) - Sales E-Commerce India ini menggunakan dataset dari yg diperoleh dari :
https://www.kaggle.com/benroshan/ecommerce-data

Exploratory Data Analysis ini dibagi dalam 4 tahap yaitu :
1. Mempelajari Dataset
2. Define Problem and Goals
3. Mengambil Insight dari Dataset
4. Memberikan Rekomendasi

## 1. Mempelajari Dataset
Mempelajari Dataset meliputi :
```
- Pengecekan Tipe data
  (object, int64, float64)
- Pengecekan Missing Value
  Menemukan index kosong pada List of Order.csv sehingga langsung di drop karena data missing value yang berulang di akhir. Kemudian setelah digabung menjadi 1 dataframe tidak ada Missing Value.
- Pengecekan Outliers
  • Pada Kolom Amount ditemukan 155 nilai Outliers, tetapi tidak dilakukan pengubahan data dikarenakan kolom ini adalah total Amount dari Penjualan.
  • Pada Kolom Profit ditemukan 291 nilai Outliers, tetapi tidak dilakukan pengubahan data dikarenakan kolom ini adalah total Profit dari Penjualan yang didapatkan.
  • Pada Kolom Quantity ditemukan 22 nilai Outliers, tetapi tidak dilakukan pengubahan data dikarenakan kolom ini adalah total Kuantitas yang terjual.
- Pengecekan Kolom yg bertipe Tanggal
  Ditemukan kolom yang bertipe tanggal yaitu terdapat pada kolom Order Date dan dilakukan pengubahan menjadi Datetime, serta dilakukan Ekstraksi menjadi kolom Year Month dan Day.
```

Dalam Dataset Sales E-Commerce India ini terdapat beberapa nama Kolom, yaitu :
```
Nama Kolom pada dataset sebagai berikut:
- Order ID = ID transaksi yang dilakukan oleh pembeli

- Amount = Total Pendapatan yang diperoleh dari Transaksi

- Profit = Total Profit yang diperoleh dari Transaksi tersebut

- Quantity = Total kuantitas pada Transaksi tersebut

- Category = Kategori yang tersedia di E-Commerce India

- Sub-Category = Sub-Kategori dari Kategori yang ada

- Order Date = Tanggal terjadinya Transaksi

- CustomerName = Nama Customer yang melakukan Transaksi

- State = Wilayah dari Customer yang melakukan Transaksi

- City = Kota dari Customer yang melakukan Transaksi

- Year Month = Ekstraksi dari Order Date untuk mengambil Bulan Tahun

- Day = Ekstraksi dari Order Date untuk mengambil nama hari
```

## 2. Define Problem and Goals
Setelah mempelajari Dataset, maka ditentukan Problem and Goals sebagai berikut :
```
Define Problems :
- Meningkatkan Penjualan dari Ketiga Category yang memiliki rata-rata Amount Penjualan dibawah dari rata-rata Target Selama 1 Tahun Penjualan.

Exploratory Data Analysis Goals :
- Mencari tahu Category yang memiliki rata-rata Amount Penjualan dibawah dari rata-rata Target selama 1 tahun periode penjualan.
- Mencari tahu apakah Penjualan terhadap Ketiga Category sudah mendapatkan Profit bagi Perusahaan.
- Mencari tahu efisiensi dan strategi apa saja yang dapat dilakukan untuk meningkatkan penjualan dari Category yang memiliki rata-rata Amount Penjualan dibawah dari rata-rata Target selama 1 tahun periode penjualan berdasarkan data yang diperoleh.
```

## 3. Mengambil Insight dari Dataset
Setelah melakukan Define Problem and Goals kemudian dilakukan Analisis Data, dan didapatkan beberapa Insight sebagai berikut :

- Pencapaian Target Penjualan Furniture :
    ```
    Pencapaian Target Penjualan Furniture pada Sales di Tahun 2018 kurang menunjukkan hal yang positif, namun pada Tahun 2019 mulai trend yang positif dalam sisi Target Penjualan. Secara rata-rata Amount Furniture yang didapat (10598.4167) masih di bawah rata-rata Target yang diharapkan (11075).
    ```

- Pencapaian Target Penjualan Clothing :
    ```
    Pencapaian Target Penjualan Clothing pada Sales kurang baik, dari 12 bulan Penjualan Clothing, hanya ada 3 bulan yang mencapai Target Penjualan, yaitu pada bulan April 2018, November 2018, dan Maret 2019. Secara rata-rata Amount Clothing yang didapat (11587.8333) masih di bawah rata-rata Target yang diharapkan (14500).
    ```

- Pencapaian Target Penjualan Electronics :
    ```
    Pencapaian Target Penjualan Electronics pada Sales sudah cukup baik, dari 12 bulan Penjualan Electronics, hanya ada 3 bulan yang tidak mencapai Target Penjualan, yaitu pada bulan Juli 2018, September 2018, dan Februari 2019. Secara rata-rata Amount Clothing yang didapat (13772.25) sudah diatas rata-rata Target yang diharapkan (10750).
    ```

- Total Profit dari 3 Category (Furniture, Clothing, Electronics) : 
    ```
    Total Profit yang menyumbang nilai tertinggi selama 1 Tahun Penjualan yaitu melalui Penjualan Clothing sebesar 11163, yang kedua melalui Penjualan Electronics sebesar 10494 dan yang paling rendah melalui Penjualan Furniture sebesar 2298 dengan Total Profit 23955.
    ```

- Penjualan Furniture :
    ```
    - Penjualan Furniture yang diatas rata-rata ada pada Hari Kamis, Jumat, dan Minggu.
    - Penjualan Furniture teramai (diatas rata-rata total transaksi per kota) ada di Kota Bhopal, Chandigarh, Delhi, Indore, Kashmir, Mumbai, Pure, dan Thiruvananthapuram.
    ```

- Penjualan Clothing : 
    ```
    - Penjualan Clothing yang diatas rata-rata ada pada Hari Senin, Selasa, Kamis, Jumat, dan Minggu.
    - Penjualan Clothing teramai (diatas rata-rata total transaksi per kota) ada di Kota Ahmedabad, Bhopal, Chandigarh, Delhi, Indore, Kolkata, Mumbai, dan Pune.
    ```

## 4. Memberikan Rekomendasi 
Berdasarkan Insight yang didapat, berikut Rekomendasi yang diberikan :
```
1. Penjualan Furniture dan Clothing masih dibawah dari rata-rata Target yang ditentukan, sehingga perlu dilakukan peningkatan pada kedua Category tersebut.

2. Peningkatan pada Furniture dapat disarankan untuk meningkatkan Jumlah Transaksi Selama Setahun pada Hari Senin, Selasa, Rabu, dan Sabtu menjadi minimal 35 Transaksi (diatas rata-rata Transaksi) dengan memaksimalkan pada kota-kota yang transaksinya di bawah rata-rata yaitu pada kota Ahmedabad, Allahabad, Amritsar, Bangalore, Chennai, Gangtok, Goa, Hyderabad, Jaipur, Kohima, Kolkata, Lucknow, Patna, Simla, Surat, dan Udaipur. Apabila ini dapat dilakukan maka akan berpotensi meningkatkan kenaikan 9.05% untuk mengejar diatas rata-rata Target.

3. Peningkatan pada Clothing dapat disarankan untuk meningkatkan Jumlah Transaksi sebesar 30% pada setiap hari selama setahun agar dapat mengejar diatas rata-rata Target dengan cara memaksimalkan pada kota-kota yang transaksinya di bawah rata-rata yaitu pada kota Allahabad, Amritsar, Bangalore, Chennai, Gantok, Goa, Hyderabad, Jaipur, Kashmir, Kohima, Lucknow, Patna, Simla, Surat, Thiruvananthapuram, dan Udaipur. Apabila dapat ditingkatkan maka akan sangat baik dikarenakan Profit yang didapat melalui Penjualan Category Clothing selama 1 tahun cukup tinggi.

4. Untuk memaksimalkan peningkatan Penjualan di tiap-tiap kota yang dibawah rata-rata yaitu dengan memberikan Promo pada daerah tersebut, agar para Customers dapat tertarik untuk membeli.

5. Untuk beberapa kota-kota yang penjualannya masih dibawah rata-rata dilakukan Survey ketertarikan Customers dengan produk E-Commerce India, dengan begini bisa mengetahui apa saja kekurangan dan kelebihan yang dimiliki oleh E-Commerce India, dan dapat dikembangkan kembali pada bagian yang dirasa kurang oleh Customers.
```



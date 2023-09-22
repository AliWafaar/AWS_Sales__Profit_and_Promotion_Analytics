# README

Notebook ini dibuat sebagai proyek capstone kedua saya dalam mengikuti kursus Data Science di Purwadhika. Notebook ini berisi analisis data dari awal hingga akhir dan merupakan portofolio saya dalam perjalanan belajar menuju ilmu data.

Dataset ini memberikan kita wawasan tentang penjualan perusahaan AWS kepada perusahaan lain dalam lingkup **B2B (Business-to-Business)** dari tahun 2020 hingga 2023.

Dataset ini bisa di Akses di : [Link Data Set](https://github.com/AliWafaar/AWS_Sales_and_Profit_Analytics/blob/main/Amazon%20Web%20Service%20Sales.csv)

Dashboard Tableau Bisa di akses di : [Link Dashboard Tableau](https://public.tableau.com/shared/PF62BYW5H?:display_count=n&:origin=viz_share_link&:device=desktop) (Pastikan sudah login akun Tableau Public kalian)

# Latar Belakang AWS


**Amazon Web Services (AWS)** adalah anak perusahaan Amazon.com yang telah mendominasi industri **layanan komputasi awan** sejak berdiri pada tahun 2006.
**Layanan AWS** mencakup beragam aspek, termasuk:

1. **Storage**: Penyimpanan data dalam berbagai format dan kapasitas.
2. **Database**: Layanan basis data yang aman dan skalabel.
3. **Security**: Keamanan data dan infrastruktur yang sangat penting.
4. **Messaging**: Komunikasi dan pertukaran informasi yang efisien.
5. **Compute**: Sumber daya komputasi yang fleksibel dan kuat.

**Segment produk AWS** yang ditawarkan kepada pelanggan B2B juga bervariasi:

1. **SMB (Small and Medium-sized Business)**: AWS menyediakan solusi dengan biaya terjangkau untuk bisnis kecil dan menengah, termasuk mesin virtual dan basis data.

2. **Strategic**: Ini adalah solusi untuk bisnis yang telah berkembang dan memerlukan layanan lebih canggih, seperti manajemen aplikasi web dan analitik data.
3. **Enterprise**: AWS menawarkan solusi lengkap untuk bisnis skala besar yang memerlukan tingkat keamanan, dukungan, dan fitur tingkat tinggi, seperti manajemen hak akses dan dukungan khusus.

Dengan demikian, AWS bukan hanya pemimpin dalam industri komputasi awan, tetapi juga mitra yang dapat memenuhi beragam kebutuhan bisnis B2B dengan berbagai solusi yang tersedia.

# **Pernyataan Masalah**

Amazon Web Services (AWS) memiliki komitmen untuk mencapai pertumbuhan setiap tahunnya, tetapi dihadapkan pada sejumlah kendala yang perlu diatasi. Kendala-kendala ini meliputi:

1. **Profitabilitas Produk**: AWS menghadapi tantangan dalam mengoptimalkan profitabilitas beberapa produknya yang saat ini mengalami kerugian.

2. **Penurunan Penjualan dan Profit**: Terjadi penurunan dalam penjualan dan profit yang memerlukan perhatian khusus untuk memahami penyebabnya dan mengambil tindakan yang sesuai.

3. **Perencanaan Pemasaran yang Tidak Terukur**: AWS perlu meningkatkan perencanaan pemasaran yang lebih terukur, termasuk waktu pelaksanaan, lokasi, dan target pasar.

4. **Rencana Diskon yang Tidak Terukur**: Rencana diskon yang ada belum cukup terukur dalam hal waktu, lokasi, dan target pasar, sehingga perlu diperbaiki.

# **Output Yang di Harapkan**
Dalam rangka mencapai tujuan ini, analisis akan difokuskan pada beberapa variabel kunci:

1. **Evaluasi Penjualan dan Profit Menurut Industri, Segmen, Asal (Negara dan Kota), serta Produk**: Dengan memahami kinerja penjualan dan profitabilitas dalam berbagai industri, segmen, asal (negara dan kota), serta produk, kita dapat mengidentifikasi area yang memerlukan perbaikan dan mengalokasikan sumber daya secara efisien.

2. **Analisis Tren Penjualan dan Profitabilitas Tahunan dan Bulanan**: Melalui analisis tren penjualan dan profitabilitas secara tahunan dan bulanan, kita dapat mengidentifikasi pola dan sinyal peringatan yang memungkinkan pengambilan tindakan yang tepat pada waktu yang tepat.

3. **Dampak Diskon terhadap Penjualan dan Profit**: Dengan mengevaluasi dampak diskon terhadap penjualan dan profitabilitas, kita dapat mengembangkan rencana diskon yang lebih efektif dengan memperhatikan waktu, lokasi, dan target pasar.

Melalui analisis mendalam ini dan pengembangan strategi yang tepat, AWS dapat mengatasi kendala yang dihadapi dan merencanakan langkah-langkah yang akan membawa pertumbuhan berkelanjutan dalam penjualan, profitabilitas, dan pemasaran produk B2B ke depan.

_____

Stakeholder: **Tim Pemasaran dan Tim Pengembangan Produk (R&D)**

# **Dataset**

Seperti ini tampilan dataset awal kita
![Screenshot 2023-09-15 111631](https://github.com/AliWafaar/AWS_Sales_and_Profit_Analytics/assets/141825588/66e5ee16-1127-4434-8e2e-ffeea95fb203)

Berikut adalah penjelasan lengkap dari Dataset kita:

|Nama Kolom| Keterangan|
|----------|------------|
|Row ID | ID unik setiap pesanan|
|Order ID | ID unik setiap pesanan|
|Order Date | Tanggal ketika pesanan dilakukan|
|Date Key | Representasi numerik dari tanggal pesanan (YYYYMMDD)|
|Contact Name | Nama orang yang melakukan pemesanan|
|Country | Negara tempat pemesanan dilakukan|
|City | Kota tempat pemesanan dilakukan|
|Region | Wilayah tempat pesanan dilakukan|
|Subregion | Subwilayah tempat pesanan dilakukan|
|Customer | Nama perusahan yang melakukan pemesanan|
|Customer ID | ID unik untuk setiap pelanggan|
|Industry | Industri tempat pelanggan berada|
|Segment | Segmen pelanggan|
|Product | Produk yang dipesan|
|Licence | ID lisensi unik untuk produk|
|Sales | Jumlah total penjualan untuk transaksi|
|Quantity | Jumlah total item dalam transaksi|
|Discount | Diskon yang diterapkan pada transaksi|
|Profit | Keuntungan dari transaksi|


1. Mengubah format data yang sesuai dengan yang seharusnya.

2. Memeriksa dan mengisi nilai yang hilang.
3. Menambahkan kolom-kolom baru untuk pengelompokan data time to time.
4. Menghapus kolom-kolom yang tidak diperlukan.

**Ini adalah tampilan data yang sudah di bersihkan**
![Screenshot 2023-09-15 112300](https://github.com/AliWafaar/AWS_Sales_and_Profit_Analytics/assets/141825588/87ba6433-c01d-4780-8352-75d5a29e52ad)

# Analisis

Di sini, kita akan memulai proses analisis data yang mencakup beberapa aspek penting.

1. Timeline Sales: Analisis ini akan memberikan wawasan tentang bagaimana penjualan berfluktuasi sepanjang waktu, termasuk tren peningkatan atau penurunan.

2. Timeline Profit: Melalui analisis ini, kita dapat memahami bagaimana profit berubah seiring berjalannya waktu dan mengidentifikasi periode dengan kinerja keuntungan yang baik atau buruk.

3. Discount by Month: Analisis diskon per bulan akan membantu kita melihat pola penggunaan diskon dan apakah ada bulan-bulan tertentu yang lebih efektif dalam meningkatkan penjualan atau profitabilitas.

4. Sales by Country: Dengan menganalisis penjualan berdasarkan negara, kita dapat mengidentifikasi pasar yang paling kuat dan mungkin mengevaluasi strategi ekspansi ke negara-negara baru.

5. Segment Sales: Analisis ini akan membantu kita memahami kinerja penjualan di berbagai segmen bisnis, yang dapat membantu dalam penyesuaian strategi pemasaran dan produk.

6. Company Sales: Menilai penjualan per perusahaan akan memungkinkan kita untuk mengidentifikasi kontributor utama terhadap pendapatan keseluruhan dan memahami peran masing-masing perusahaan dalam portofolio bisnis.

7. Product Profit: Melalui analisis profit produk, kita dapat menilai produk mana yang memberikan profitabilitas tertinggi dan apakah ada produk yang memerlukan peninjauan atau pengembangan lebih lanjut.

# Conclusion

Berdasarkan analisis yang telah dilakukan, dapat disimpulkan bahwa ada beberapa aspek yang perlu diperhatikan untuk meningkatkan kinerja perusahaan.

- Penurunan signifikan dalam time to time sales dan profit sebagian besar disebabkan oleh kebijakan diskon dan strategi pemasaran yang kurang tepat sasaran. Adanya penurunan profit pada bulan salah satunya dikarenakan penggunaan diskon yang berlebihan,seperti yang kita ketahui meskipun discount dapat meningkatkan jumlah transaksi,discount juga dapat mengurangi profitabilitas perusahaan. Solusi potensial adalah mengalokasikan diskon dengan bijak, fokus pada bulan-bulan dengan transaksi yang dominan lebih sedikit untuk meningkatkan profit dan penjualan.

- Dengan memperhatikan data penjualan berdasarkan negara, kita dapat merancang strategi pemasaran yang lebih tepat sasaran. Negara dengan penjualan rendah dapat menjadi target untuk mencari pasar baru, sementara negara dengan penjualan tinggi perlu mendapatkan promosi khusus untuk mempertahankan dan meningkatkan kontribusi mereka terhadap perusahaan.

- Analisis segmentasi memberikan wawasan berharga. Pertama, dengan memeriksa penjualan berdasarkan industri, kita dapat menilai kinerja masing-masing segmen sesuai dengan industri yang ada. Dengan memahami mana segmen yang lebih kuat dalam industri tertentu, kita dapat menentukan segmen mana yang harus dikembangkan lebih lanjut untuk memanfaatkan peluang yang ada.

- Melalui analisis pelanggan atau perusahaan, kita dapat mengidentifikasi perusahaan-perusahaan utama yang menjadi pelanggan utama dan produk-produk yang paling banyak dibeli oleh mereka. Dengan informasi ini, kita dapat menentukan segmen mana yang perlu dikembangkan lebih lanjut untuk memenuhi kebutuhan setiap perusahaan tersebut. Ini akan membantu perusahaan dalam merancang strategi khusus untuk memperluas basis pelanggan dan meningkatkan penjualan di segmen yang relevan

- Analisis profit berdasarkan produk membantu kita mengidentifikasi produk-produk yang berkinerja baik dan yang kurang baik, serta menentukan segmen mana di mana produk tersebut tampil baik atau buruk. Dengan pengetahuan ini, kita dapat fokus pada mengoptimalkan produk-produk yang berkinerja baik dan mengembangkan strategi perbaikan untuk produk yang tidak berkinerja sebagaimana diharapkan. Selain margin pada produk, discount juga dapat mengurangi profitabilitas dari produk tersebut. Oleh karena itu, pemahaman yang mendalam tentang bagaimana discount memengaruhi profit menjadi kunci dalam pengambilan keputusan bisnis.

Secara keseluruhan, dengan memahami dan mengambil langkah-langkah berdasarkan analisis ini, perusahaan dapat meningkatkan profitabilitas, penjualan, dan strategi pemasaran mereka sesuai dengan potensi yang ada dalam berbagai segmen dan pasar.

# **Recomendation**

**1. Optimasi Kebijakan Diskon dan Strategi Pemasaran:**
   - **Peninjauan Kebijakan Diskon**: Evaluasi kebijakan diskon saat ini dan pastikan diskon dialokasikan secara bijak jangan menggunakan diskon berlebih pada bulan dengan penjualan yang tinggi seperti pada bulan:
      - **September**
      - **November**
      - **Desember**
   - **Penggunaan Diskon yang Tepat**: Pertimbangkan penggunaan diskon pada bulan-bulan dengan penjualan rendah, untuk meningkatkan profitabilitas seperti pada bulan:
      - **Januari**
      - **Febuari**
      - **Maret**
   
   **2. Penyesuaian Strategi Berdasarkan Data Penjualan Negara:**
   - **Penjualan di Negara dengan Potensi Rendah**: Fokus pada negara dengan penjualan rendah seperti **Qatar, Iceland, Denmark, Croatia, dan Slovenia** untuk mencari peluang pasar baru.
   - **Penjualan di Negara dengan Potensi Tinggi**: Tingkatkan promosi di negara dengan penjualan tinggi seperti **AS, Inggris, Jepang, Kanada, dan Prancis** untuk mempertahankan kontribusi mereka.

**3. Pengembangan Segmen yang Potensial:**
   - **Segmentasi Berdasarkan Industri**: Identifikasi segmen yang memiliki potensi pertumbuhan, seperti :
      - Segment **SMB** pada industri **Finance, Energy, Manufacturing, Healthcare, Tech, Consumer Product, Retail, dan Transportation**
      - Segment **Strategic** pada industri **Communication**
      - Segment **Enterprise** pada industri **Misc**

**4. Fokus pada Perusahaan Utama dan Meminta Feedback:**
   - **Strengthen Hubungan dengan Perusahaan Utama**: Perkuat hubungan dengan perusahaan utama seperti: 
      - **Anthem** 
      - **Allianz**
      - **Ford Motor**
   - **Pengembangan Produk Khusus**: Kembangkan produk yang sesuai dengan kebutuhan perusahaan utama, seperti:
      - Segment **SMB** pada **Anthem** dan **Ford**
      - Segment **Strategic** pada **Allianz**
   - **Umpan Balik Aktif**: Selalu minta umpan balik dari perusahaan-perusahaan utama untuk memahami kebutuhan mereka dan menyesuaikan produk dan layanan.

**5. Optimasi Portofolio Produk:**
   - **Analisis Profit Berdasarkan Produk**: Evaluasi profitabilitas produk berdasarkan segment mereka, seperti:
      - Segment **SMB** pada **Alchemcy** dan **Site Analytics**
      - Segment **Strategic** pada **Data Smasher**.
   - **Penggunaan Diskon yang Bijak**: Hindari penggunaan diskon yang berlebihan, terutama pada produk dengan quantity penjualan yang tinggi seperti pada product:
      - **Contact Matcher**
      - **Big Ol Databese**
   - **Evaluasi Produk yang Tidak Efektif**: Evaluasi kembali dan pertimbangkan untuk menghapus produk yang tidak dapat mencapai kinerja yang diharapkan dari portofolio untuk menghindari pemborosan sumber daya seperti:
      - **Marketing Suites**
      - **Storage**

**6. Monitoring dan Evaluasi Terus-Menerus:**
   - **Pemantauan Rutin**: Implementasikan pemantauan dan evaluasi terus-menerus untuk memastikan perbaikan berkelanjutan dalam kinerja perusahaan.

___

Selengkapnya bisa di akses di File .Ipynb





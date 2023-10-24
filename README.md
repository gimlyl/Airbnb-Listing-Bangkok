# Airbnb Listing Analysis: Insights from Bangkok's Accommodation Landscape
### **BACKGROUND** 
Airbnb adalah jaringan pasar daring dan penginapan rumahan sejawat yang memungkinkan pengguna mendaftarkan atau menyewa properti untuk digunakan dalam jangka pendek. Harga sewanya ditetapkan oleh pemilik properti. Airbnb memiliki cabang diberbagai negara salah satu cabangnya ada di Bangkok. Membahas pentingnya Airbnb sebagai platform untuk penyewaan properti jangka pendek maupun jangka panjang. Ini menguraikan tujuan analisis, yaitu untuk memahami pengaruh ulasan pada pengambilan keputusan dan harga sewa di Bangkok. Analisis ini juga bermaksud untuk memahami distribusi jenis properti, korelasi ulasan dengan jenis properti, dan lingkungan dengan daftar terbanyak. **Airbnb Bangkok mau menganalisis apakah Reviews dapat mempengaruhi pengambilan keputusan seseorang dalam memilih tempat hunian ataupun reviews berpengaruh terhadap harga sewa tempat hunian**. Beberapa parameter akan digunakan yaitu:
- Mencari tahu tipe hunian apa saja yang terlisting di aplikasi Airbnb.
- Mencari tahu tipe hunian apa yang memiliki review terbanyak. 
- Neighbourhood apa yang memiliki tempat hunian terbanyak.
- Mencari tahu tipe hunian apa yang memiliki review paling sedikit.
- Mencari tahu berapa jumlah hunian yang memiliki review dan yang tidak memiliki review.
<br>

**Stakeholders** > Airbnb Product Owner Perwakilan Bangkok
<br>

### **Goals** 
- Mencari Tahu Tipe hunian apa yang paling banyak ditemukan melalui aplikasi Airbnb yang berlokasi di Bangkok untuk setiap lokasi
- Menambahkan kebijakan baru supaya penyewa bisa memberikan review
- Memberikan rekomendasi untuk customer/penyewa yang sedang mencari hunian dilokasi tertentu di Bangkok
<br

# Dataset:
**Column Data Mentah**
| Feature                      | Deskripsi                                                                   |
|---------------------------------|-----------------------------------------------------------------------------|
| id                       | Pengenal unik Airbnb untuk tempat tersebut.               |
| name                       | Nama tempat hunian.               |
| host_id                       | Pengenal unik Airbnb untuk tuan rumah/pengguna.               |
| Host Name                       | Merupakan field untuk menampung data pemilik tempat tersebut               |
| neighborhood                      | Lingkungan ini di-geocode menggunakan garis lintang dan bujur terhadap lingkungan seperti yang didefinisikan oleh terbuka atau publik shapefile digital.              |
| Latitude & Longitude            | Field untuk lokasi (map)                                                    |
| Room Type                       | Tipe hunian yang bisa disewa melalui aplikasi Airbnb yang berlokasi di Bangkok |
| Price                           | Harga sewa hunian tersebut                                                 |
| Minimum Nights                  | Minimal lama waktu penyewaan tempat hunian                                  |
| Number of Reviews               | Jumlah review yang dimiliki hunian tersebut                                 |
| last_review              | Tanggal ulasan terakhir/terbaru.                                 |
| Calculated Host Listings Count | Jumlah tempat hunian yang dimiliki oleh pemilik yang terdapat di kota tersebut |
| availability_365 | avaliability_x. Kalender menentukan ketersediaan daftar x hari di masa depan. Catatan: tempat mungkin tersedia karena telah dipesan oleh tamu atau diblokir oleh tuan rumah. |
| number_of_reviews_ltm | Jumlah ulasan yang dimiliki daftar (dalam 12 bulan terakhir). |

<br>
Informasi lengkap mengenai tipe hunian 
<br>

| Room Type                       | Entire home/apartment, Private rooms, Shared rooms, Hotel |
|---------------------------------|-----------------------------------------------------------------------------|
| Entire home/apartment           |Seluruh tempat adalah yang terbaik jika Anda mencari rumah yang jauh darinya rumah. Dengan seluruh tempat, Anda akan memiliki seluruh ruangan dirimu sendiri. Ini biasanya mencakup kamar tidur, kamar mandi, dapur, dan pintu masuk khusus yang terpisah. Tuan rumah harusnya catat dalam deskripsi apakah mereka akan berada di properti atau tidak (misal: "Tuan rumah menempati lantai pertama rumah") dan menyediakan lebih lanjut rincian pada daftar. |
| Private rooms                 | Kamar pribadi sangat cocok jika Anda menginginkan sedikit privasi, dan masih menghargai koneksi lokal. Saat Anda memesan kamar pribadi, Anda akan memiliki kamar pribadi untuk tidur dan mungkin berbagi beberapa ruang dengan orang lain. Anda mungkin perlu berjalan kaki melalui ruang dalam ruangan yang mungkin ditempati oleh tuan rumah atau tamu lain untuk sampai ke kamarmu. |
| Shared rooms                 | Kamar bersama diperuntukkan bagi Anda yang tidak keberatan berbagi ruang dengan orang lain. Saat Anda memesan kamar bersama, Anda akan tidur di ruang yang digunakan bersama dengan orang lain dan berbagi keseluruhan ruang dengan orang lain. Kamar bersama sangat populer di kalangan wisatawan fleksibel yang mencari teman baru dan penginapan ramah anggaran. |
| Hotel                 | Kamar hotel diperuntukkan bagi Anda yang sedang melakukan perjalanan ataupun yang sedang ingin menyewa tempat untuk istirahat. Hotel memiliki layanan room service yang dapat digunakan, akan tetapi barang-barang yang ada didalam kamar hotel tidak boleh dirusak ataupun diambil. | 
   
Sections:
# Data Import and Cleaning:

## Importing the Airbnb Bangkok dataset.
Disini kita akan mengecek anomali serta missing value yang terdapat didalam dataset Airbnb Bangkok kemudian anomali dan missing value tersebut akan diatasi atau dihandle
To Do List:
1. Mengecek Info Data
2. Mengecek Duplikasi Data
    - Menghilangkan Duplikasi Data(jika ada)
3. Mengecek data anomalies
    - Mengatasi data anomalis
4. Mengubah nama column sehingga mudah untuk digunakan ataupun dibaca
5. Drop column yang tidak digunakan 
6. Menambahkan column baru untuk digunakan dalam analisis data
7. Mengecek Persebaran Data

ini merupakan tahap-tahap yang akan dilakukan dalam proses data wrangling & cleaning

## **Conclusions**

Bangkok, sebagai salah satu kota yang paling banyak didatangi oleh para turis di Thailand, memiliki beragam distrik, masing-masing dengan karakteristiknya, memberikan pengalaman yang unik bagi pengunjung. Dari analisa yang dilakukan, diketahui bahwa mayoritas hunian yang terdaftar di Airbnb di Bangkok terletak di distrik perbelanjaan dan bisnis.

Dari analisis tersebut, beberapa poin penting adalah:

**Variasi Tipe Hunian**:
Terdapat empat tipe hunian utama yang terlist di Airbnb Bangkok: Entire Home/Apartment, Private Room, Hotel Room, dan Shared Room.

**Kekurangan Review**:
Banyak hunian yang tidak memiliki review, mempengaruhi daya tarik bagi calon penyewa dan mengurangi jumlah pilihan hunian yang memenuhi kebutuhan mereka, karena kurangnya testimoni atau ulasan dari pengunjung sebelumnya.

**Karakteristik Distrik**:
Distrik seperti Vadhana dan Khlong Toei menawarkan lokasi strategis, dengan Vadhana sebagai pusat kota dan Khlong Toei sebagai lokasi pelabuhan kontainer terbesar di Thailand, keduanya juga menyediakan beragam fasilitas komersial dan tempat penting lainnya.

**Pengaruh Harga dan Review**:
Analisis menunjukkan bahwa ada korelasi terbalik dan kecil antara harga dan review. Sedangkan, Total Price sangat dipengaruhi oleh Minimum Night, dengan pengaruh sebesar 82%, menandakan semakin lama durasi sewa, harga yang perlu dibayar akan semakin besar.

**Implikasi**:
**Pentingnya** **Review**:
Pemilik hunian harus mendorong pengunjung untuk meninggalkan review untuk meningkatkan daya tarik hunian mereka, memandu calon penyewa dalam membuat keputusan, dan memperluas opsi hunian yang tersedia.

**Penyesuaian** **Harga**:
Dengan adanya pengaruh antara harga dan durasi sewa, pemilik hunian perlu menetapkan harga yang kompetitif dan realistis sesuai dengan durasi sewa yang diinginkan oleh penyewa potensial.

**Secara keseluruhan, untuk meningkatkan daya tarik dan keberagaman pilihan hunian, pemilik hunian perlu mempertimbangkan faktor-faktor di atas dalam strategi pemasaran dan penentuan harga mereka.**

# **Rekomendasi**
Berdasarkan analisis yang telah dilakukan, berikut adalah beberapa rekomendasi yang dapat diterapkan untuk mengoptimalkan layanan dan penawaran hunian di Airbnb Bangkok:

1. **Meningkatkan Jumlah Review**:
Dengan 36% hunian yang belum memiliki review, sangat disarankan untuk mengimplementasikan kebijakan yang mendorong pengguna dan penyewa untuk meninggalkan review setelah masa tinggal mereka. Review ini harus mencakup rating dan informasi detil mengenai pengalaman mereka, yang nantinya akan membantu calon penyewa dalam membuat keputusan yang lebih baik dan meningkatkan kredibilitas dan daya tarik hunian yang terlist.

2. **Menonjolkan Tipe Hunian Populer**:
Mengingat kebanyakan hunian yang terlisting adalah Entire Home/Apartment dan Private Room, dapat dilakukan strategi pemasaran yang menonjolkan jenis hunian ini kepada calon penyewa. Namun, strategi ini juga harus disesuaikan dengan preferensi lokasi dari pengguna, untuk memastikan kecocokan antara tawaran dan kebutuhan penyewa.

3. **Mengidentifikasi Peluang Bisnis di Distrik Populer**:
Wilayah Vadhana dan Khlong Toei, sebagai daerah dengan jumlah listing terbanyak, menawarkan peluang bisnis yang signifikan. Airbnb dapat menjalin kerjasama dengan lebih banyak pemilik hunian di distrik-distrik ini dan distrik terkenal lainnya untuk meningkatkan jumlah listing dan menjangkau audiens yang lebih luas.

4. **Penyesuaian Strategi Pemasaran**:
Mengembangkan dan menyesuaikan strategi pemasaran yang lebih terfokus pada daerah-daerah dengan permintaan tinggi dan jenis hunian yang lebih populer dapat membantu dalam mencapai penetrasi pasar yang lebih luas dan memenuhi kebutuhan penyewa dengan lebih efektif.

**Dengan mengimplementasikan rekomendasi-rekomendasi ini, diharapkan akan tercipta peningkatan dalam layanan, kepuasan pengguna, dan keberhasilan bisnis untuk hunian yang terdaftar di Airbnb Bangkok.**







# Airbnb Listing Bangkok Analysis
Airbnb adalah jaringan pasar daring dan penginapan rumahan sejawat yang memungkinkan pengguna mendaftarkan atau menyewa properti untuk digunakan dalam jangka pendek. Harga sewanya ditetapkan oleh pemilik properti. Airbnb memiliki cabang diberbagai negara salah satu cabangnya ada di Bangkok. Membahas pentingnya Airbnb sebagai platform untuk penyewaan properti jangka pendek maupun jangka panjang. 

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
Handling missing values, outliers, and data anomalies.
## Exploratory Data Analysis (EDA):

Visualisasi listings dari property type, location, and price range.
analisis korelasi antara variables price, reviews.
## Location Analysis:

mencari tahu popular neighborhoods and harga sewa average rental prices.
Mapping listings untuk visualisasi distribsui di Bangkok.








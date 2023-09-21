# Airbnb Listing Bangkok Analysis
This project aims to analyze Airbnb listings for Bangkok, providing insights into the rental market, preferences of travelers, and potential areas of improvement for hosts.

# Dataset:
The dataset is sourced from Airbnb and contains detailed listings for Bangkok.
It includes information such as property type, location, price, reviews, and other relevant details.
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

Visualizing the distribution of listings by property type, location, and price range.
Analyzing the correlation between variables such as price, reviews, and amenities.
## Location Analysis:

Exploring popular neighborhoods and their average rental prices.
Mapping the listings to visualize the distribution across Bangkok.
## Price Prediction:

(If applicable) Building a predictive model to estimate rental prices based on listing features.
# Recommendations:

Offering suggestions for hosts to improve their listings and increase revenue.
Providing insights for travelers to make informed booking decisions.








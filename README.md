# Analisis Prediktif Harga Berlian💎

Proyek ini adalah studi kasus Machine Learning Terapan untuk mempelajari analisis prediktif menggunakan **dataset diamonds**. Tujuannya adalah untuk membangun model prediksi yang dapat memperkirakan harga berlian berdasarkan fitur seperti karat, potongan, warna, dan kejernihan.

## Daftar Isi

- [Pendahuluan](#pendahuluan)
- [Dataset](#dataset)
- [Gambaran Proyek](#gambaran-proyek)
- [Instalasi](#instalasi)
- [Kesimpulan](#kesimpulan)

## Pendahuluan

Proyek ini bertujuan untuk melakukan analisis prediktif terhadap harga berlian menggunakan model KNN, Random Forest, dan Boosting. Dengan menggunakan dataset berlian yang besar, kita akan memprediksi harga berlian berdasarkan karakteristiknya seperti berat (carat), kualitas potongan (cut), warna (color), dan kejernihan (clarity).

## Dataset

Dataset yang digunakan dalam proyek ini berasal dari pustaka `ggplot2` dan terdiri dari fitur-fitur berikut:

- **carat**: Bobot berlian.
- **cut**: Kualitas potongan berlian (Fair, Good, Very Good, Premium, Ideal).
- **color**: Warna berlian, diukur dari D (terbaik) hingga J (terburuk).
- **clarity**: Kejernihan berlian (IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1).
- **depth**: Persentase kedalaman total berlian (z / mean(x, y)).
- **table**: Lebar bagian atas berlian.
- **price**: Harga berlian dalam USD.
- **x**: Panjang berlian dalam mm.
- **y**: Lebar berlian dalam mm.
- **z**: Kedalaman berlian dalam mm.

Untuk informasi lebih lanjut tentang dataset, kunjungi [ggplot2 diamonds reference](https://ggplot2.tidyverse.org/reference/diamonds.html).

## Gambaran Proyek

Proyek ini mengikuti langkah-langkah dasar dalam pipeline machine learning:

1. **Eksplorasi Data**: Memahami distribusi dan hubungan antar variabel.
2. **Pra-pemrosesan Data**: Menyiapkan data dengan encoding variabel kategorikal dan membaginya menjadi set pelatihan dan pengujian.
3. **Pemodelan**: Membangun model **Regresi Linier** untuk memprediksi harga berlian.
4. **Evaluasi**: Mengukur performa model menggunakan metrik **Mean Squared Error (MSE)** dan **R-squared (R²)**.

## Instalasi

Untuk menjalankan proyek ini di lokal atau di Google Colab, instalasi berikut diperlukan:

- numpy
- pandas
- matplotlib
- seaborn

Instal semua dependensi dengan perintah berikut:

```bash
pip install numpy matplotlib pandas seaborn
```

Jika menggunakan Google Colab, dataset dapat diunduh secara langsung dari URL:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/tidyverse/ggplot2/main/data-raw/diamonds.csv"
diamonds = pd.read_csv(url)
```

## Kesimpulan

Setelah menguji beberapa model, Random Forest (RF) terbukti memberikan performa terbaik dengan nilai eror yang paling kecil dibandingkan dengan model lain, seperti Boosting, yang memiliki nilai eror tertinggi (di atas 800). Oleh karena itu, model Random Forest dipilih sebagai model terbaik untuk memprediksi harga berlian.

Hasil prediksi menggunakan algoritma Random Forest menunjukkan kecocokan yang paling mendekati nilai aktual. Untuk pengembangan selanjutnya, disarankan untuk menguji hasil prediksi dengan data lain, atau melakukan hyperparameter tuning seperti mengubah nilai n_estimators pada algoritma Random Forest. Untuk meningkatkan performa, hyperparameter tuning dapat dilakukan pada semua algoritma yang digunakan, dan teknik Grid Search dapat diterapkan untuk menemukan parameter optimal.

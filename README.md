# #Cashtag
## PowerPoint : https://docs.google.com/presentation/d/1cpjM3O4ye1guOLGIsd5fB2guvB7VDWfbVuOVgkaFFDo/edit#slide=id.p

## Data Analyst
Telco Customer Churn

## Prerequisites
1. Link download dataset [here](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
2. Instalasi dengan pip install requirements.txt

## Deskripsi:
Dataset ini menggambarkan perilaku dan profil pelanggan di
perusahaan Telco yang digunakan guna menganalisis dan memprediksi
retensi pelanggan.

## Data:
Setiap baris mewakili pelanggan, setiap kolom berisi atribut pelanggan.

Kumpulan data mencakup informasi tentang:

1. Pelanggan yang pergi dalam sebulan terakhir – kolomnya disebut Churn
2. Layanan yang telah didaftarkan oleh setiap pelanggan – telepon, banyak saluran, internet, keamanan online, pencadangan online, perlindungan perangkat, dukungan teknis, serta streaming TV dan film
3. Informasi akun pelanggan – sudah berapa lama mereka menjadi pelanggan, kontrak, metode pembayaran, tagihan tanpa kertas, tagihan bulanan, dan total tagihan
4. Info demografis tentang pelanggan – jenis kelamin, rentang usia, dan jika mereka memiliki pasangan dan tanggungan

## Melihat Distribusi dari TotalCharge?

dfa =df.copy()<br>
dfa['TotalCharges'] = pd.to_numeric(dfa['TotalCharges'], errors='coerce')<br>
dfa.dropna(subset=['TotalCharges'], inplace=True)<br>

fig, axes = plt.subplots(1,2, figsize=(17,6))

plt.sca(axes[0])
sns.boxplot(x="TotalCharges", data=dfa)
plt.title('Distribution of TotalCharge')

plt.sca(axes[1])
sns.histplot(data=dfa["TotalCharges"],kde=True)

**Distribusi data dari TotalCharger Negative Skewed
Kebanyakan dari pelanggan Telco memiliki total biaya dibawah $2000**

## Insight

1. Pelanggan dengan kontrak month to month paling tinggi dengan jumlah total 3875 pelanggan
2. Jumlah pelanggan Churn Kebanyakan dari customer pria
3. Rata-rata biaya bulanan tertinggi ada pada metode pembayaran electronic check, sedangkan yang paling rendah pada metode pembayaran mailed check
4. Kebanyakan Pelanggan Telco memiliki masa berlangganan kurang dari 20 bulan atau lebih dari 41 bulan
5. Baik warga Senior maupun warga non-senior kebanyakan menggunakan layanan telepon
6. Distribusi data dari TotalCharger Negative Skewed dan Kebanyakan dari pelanggan Telco memiliki total biaya dibawah 2000 dollar.
7. Kebanyakan dari pelanggan yang berhenti berlangganan (churn) memiliki biaya bulanan yang tinggi, lebih dari 60 dollar.
8. Pelanggan yang memiliki pasangan dan tanggungan memiliki tingkat churn yang paling rendah, sedangkan pelanggan yang tidak memiliki keduanya memiliki tingkat churn yang paling tinggi

## Rekomendasi Bisnis Insight

**Sebagian besar Pengguna yang memiliki masa kerja di bawah satu tahun mengalami Churn** <br>
Sekitar 55 persen Pengguna Baru (di bawah satu tahun) mengalami Churn. Kami ingin tahu mengapa sebagian besar pengguna baru churn, Jadi kami akan fokus pada pengguna yang churn di bawah satu tahun <br><br>

**Lebih dari Setengah Pengguna yang Churn di bawah satu tahun memiliki Kontrak Bulanan dan telah Menikah** <br>
Pengguna Baru yang Churn hampir semuanya memiliki kontrak Bulan-ke-Bulan. Hipotesis kami bahwa pengguna ingin mencoba produk terlebih dahulu. Namun, produk ini tidak cocok untuk mereka, jadi mereka Churn. Mari kita lihat mengapa lebih banyak pengguna yang sudah menikah dari pada yang lajang <br><br>

**Tagihan Bulanan dari Distribusi User yang sudah Menikah adalah kurang dari 60**<br>
User yang Menikah yang melakukan Churn memiliki biaya bulanan yang lebih sedikit dari pada User yang Single. Kebanyakan dari mereka memiliki kontrak Bulan-ke-Bulan dan masa kerja kurang dari satu tahun. Kami dapat memberikan mereka promo paket keluarga untuk mendorong pengguna lebih setia kepada penyedia ini<br>

## References

Homework Data Visualization <br> 
Rakamin Data Science Batch 25 Sukma Rizki


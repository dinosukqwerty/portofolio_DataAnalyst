# #Cashtag

## Data Analyst
Telco Customer Churn

● Deskripsi:<br>
Dataset ini menggambarkan perilaku dan profil pelanggan di
perusahaan Telco yang digunakan guna menganalisis dan memprediksi
retensi pelanggan.

● Data:<br>
Setiap baris mewakili pelanggan, setiap kolom berisi atribut pelanggan.

Kumpulan data mencakup informasi tentang:

1. Pelanggan yang pergi dalam sebulan terakhir – kolomnya disebut Churn
2. Layanan yang telah didaftarkan oleh setiap pelanggan – telepon, banyak saluran, internet, keamanan online, pencadangan online, perlindungan perangkat, dukungan teknis, serta streaming TV dan film
3. Informasi akun pelanggan – sudah berapa lama mereka menjadi pelanggan, kontrak, metode pembayaran, tagihan tanpa kertas, tagihan bulanan, dan total tagihan
4. Info demografis tentang pelanggan – jenis kelamin, rentang usia, dan jika mereka memiliki pasangan dan tanggungan

## Prerequisites
1. Link download dataset [here](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
2. Instalasi dengan pip install requirements.txt

## Getting Started

- WA_Fn-UseC_-Telco-Customer-Churn

## Dataset WA_Fn-UseC_-Telco-Customer-Churn
Jumlah pelanggan dilihat dari tipe kontrak?
v 

dfg = df.groupby(['Contract'])['customerID'].nunique().reset_index(name='unique_customers')

x = dfg['Contract']
y = dfg['unique_customers']

## Melihar Distribusi dari TotalCharge?

dfa =df.copy()
dfa['TotalCharges'] = pd.to_numeric(dfa['TotalCharges'], errors='coerce')
dfa.dropna(subset=['TotalCharges'], inplace=True)

fig, axes = plt.subplots(1,2, figsize=(17,6))

plt.sca(axes[0])
sns.boxplot(x="TotalCharges", data=dfa)
plt.title('Distribution of TotalCharge')

plt.sca(axes[1])
sns.histplot(data=dfa["TotalCharges"],kde=True)

## References

Homework Data Visualization <br> 
Rakamin Data Science Batch 25 Sukma Rizki


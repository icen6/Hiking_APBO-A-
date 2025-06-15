# UTS APBO A KELOMPOK 6 

Repositori ini berisi hasil Ujian Tengah Semester (UTS) mata kuliah Analisis Pemrograman Berbasis Objek (APBO) - Kelas A 

## Dosen Pengampu
Adi Wahyu Pribadi, S.Si., M.Kom

## Anggota Kelompok 6
| No | Nama Anggota          | NPM         |
|----|-----------------------|-------------|
| 1  | Fadzry Dewa Sya'bana  | 4523210043  |
| 2  | Daffa Yassar Ahmad    | 4523210032  |
| 3  | Dendy Anugrahi Rabbi  | 4523210034  |
| 4  | Muhamad Ihsan Setiawan| 4523210069  |
| 5  | Handra Putra Alma     | 4523210052  |

## Hike Station 

### 1. Aktor/Role Yang Terlibat

• Admin
Memiliki peran sebagai administrator sistem yang bertugas mengatur menu, memproses penyewaan yang diterima, mengelola informasi penyewaan, serta menangani proses pembayaran.

• Penyewa
Memiliki peran sebagai pengguna sistem yang bertugas melakukan penyewaan, menginput data pribadi, menentukan metode pembayaran, serta mendapatkan notifikasi terkait penyewaan.


### 2. Use Case Diagram
![ERD-Page-2 drawio](https://github.com/user-attachments/assets/87452242-f228-4d99-8a0a-90faa339eab6)
 


### 3. Entitas Utama 

#### A. Penyewa  

| Nama Atribut   | Tipe Data    | Keterangan                     |
| -------------- | ------------ | ------------------------------ |
| ID_Penyewa     | VARCHAR(10)  | Primary key, ID unik penyewa   |
| nama_penyewa   | VARCHAR(30)  | Nama lengkap penyewa           |
| alamat         | VARCHAR(50)  | Alamat tempat tinggal penyewa  |
| no_telp        | VARCHAR(15)  | Nomor telepon penyewa          |


#### B. sewa_barang 

| Nama Atribut         | Tipe Data   | Keterangan                     |
| -------------------- | ----------- | ------------------------------ |
| ID_sewabarang        | VARCHAR(10) | Primary key, ID unik sewabarang|
| ID_Penyewa           | VARCHAR(10) | Foreign key dari penyewa       |
| tanggal_sewa         | DATE        | Tanggal awal sewa barang       |
| tanggal_pengembalian | DATE        | Tanggal pengembalian barang    |


#### C. Barang 

| Nama Atribut        | Tipe Data     | Keterangan                         |
| --------------------| ------------- | ---------------------------------- |
| ID_Barang           | VARCHAR(10)   | Primary key, ID unik barang        |
| nama_barang         | VARCHAR(100)  | Nama barang                        |
| stok_barang         | INT           | Jumlah stok tersedia               |
| harga_sewa_barang   | DECIMAL(10,2) | Harga sewa per unit barang         |
| jumlah_barang       | INT           | Jumlah barang yang disewa          |
| ID_Kategori_Barang  | VARCHAR(10)   | Foreign key dari Kategori_Barang   |


#### D. Kategori Barang 

| Nama Atribut        | Tipe Data   | Keterangan                            |
| --------------------| ----------- | ------------------------------------- |
| ID_Kategori_Barang  | VARCHAR(10) | Primary key, ID unik kategori barang  |
| jenis_kategori      | VARCHAR(50) | Jenis atau nama kategori              |
| kapasitas_barang    | VARCHAR(50) | Kapasitas barang                      |


#### E. Status Barang 

| Nama Atribut   | Tipe Data    | Keterangan                                 |
| -------------- | -------------| ------------------------------------------ |
| Status_Barang  | VARCHAR(50)  | Primary key, Status barang                 |
| ID_Penyewa     | VARCHAR(10)  | Foreign key dari Penyewa                   |
| ID_sewabarang  | VARCHAR(10)  | Foreign key dari sewa_barang               |


#### F. Transaksi 

| Nama Atribut    | Tipe Data     | Keterangan                               |
| -------------   | ------------- | ---------------------------------------- |
| ID_Transaksi    | VARCHAR(10)   | Primary key, ID unik transaksi           |
| metode_transaksi| VARCHAR(50)   | Metode transaksi (tunai, transfer, dll)  |
| total_transaksi | DECIMAL(10,2) | Total jumlah yang dibayarkan             |
| ID_Penyewa      | VARCHAR(10)   | Foreign key dari Penyewa                 |
| Status_Barang   | VARCHAR(50)   | Foreign key dari Status_Barang           |


### 4. ERD 
![ERD-Page-1 drawio](https://github.com/user-attachments/assets/98f56cd8-ad8c-4196-a586-78e533eb9f85)



### 5. Class Diagram 
![image](https://github.com/user-attachments/assets/442d80eb-4250-4325-9799-aad0612dfd1a)

### 6. Sequence Diagram
#### Penyewa
##### Halaman Login Penyewa
![image](https://github.com/user-attachments/assets/62d7698f-1114-4acd-9815-c103ae49c9e4)

##### Halaman Melihat Daftar Barang
![image](https://github.com/user-attachments/assets/b9c5f181-6e6a-4689-a537-7e659d0e711c)

##### Halaman Sewa Barang
![image](https://github.com/user-attachments/assets/46a5f4fb-a8b6-4040-b2ec-87f514cb49c1)

##### Halaman Transaksi
![image](https://github.com/user-attachments/assets/b4a2e933-04f2-4342-9569-296471753d9b)

##### Halaman History Sewa Barang
![image](https://github.com/user-attachments/assets/7e7e2afd-1b28-48c7-b1fa-6728f2c69be0)

#### Admin
##### Halaman Login Admin
![image](https://github.com/user-attachments/assets/c76f4e46-8cb2-4ff1-ada0-99a2001c9764)

##### Halaman Kelola Data Penyewa
![image](https://github.com/user-attachments/assets/4ad04801-9d92-41fd-ac39-60d20a7188ce)

##### Halaman Kelola Data Barang
![image](https://github.com/user-attachments/assets/0fdbcbc7-f949-4d0f-8b1f-50aa3fa54921)

##### Halaman Kelola Data Transaksi
![image](https://github.com/user-attachments/assets/2fb2620b-2121-428a-b3e7-4c6732c6a6d5)

##### Halaman Membuat Laporan Sewa
![image](https://github.com/user-attachments/assets/85b4e7a8-c38b-4a17-947c-0ee607d24b85)


### 7. Mock Up 
#### Halaman Utama
![image](https://github.com/user-attachments/assets/e4f369fe-958e-48fc-8ea3-204901c31b24)

#### Halaman Login
![image](https://github.com/user-attachments/assets/ac910007-3469-438a-a86c-ed45ae5859ec)

#### Halaman Keranjang
![image](https://github.com/user-attachments/assets/10d3f428-c4a5-4390-9ffc-7ecb45f156b1)

#### Halaman Payment Success
![image](https://github.com/user-attachments/assets/ead8c496-a287-4474-a159-65a41e86effb)

#### Halaman Item History
![image](https://github.com/user-attachments/assets/ec20f20f-945d-4288-b7f5-fc75a6ad1492)


### 8. Fakta Integritas 
![image](https://github.com/user-attachments/assets/bb267377-a244-4034-9e8a-5d2b720f6be8)


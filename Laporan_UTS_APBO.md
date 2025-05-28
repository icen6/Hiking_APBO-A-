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

• Pemilik
Memiliki peran sebagai administrator sistem yang bertugas mengatur menu, memproses penyewaan yang diterima, mengelola informasi penyewaan, serta menangani proses pembayaran.

• Penyewa
Memiliki peran sebagai pengguna sistem yang bertugas melakukan penyewaan, menginput data pribadi, menentukan metode pembayaran, serta mendapatkan notifikasi terkait penyewaan.


### 2. Use Case Diagram 
![Usecase drawio](https://github.com/user-attachments/assets/31f79dba-7a2f-4fa8-a2c4-af8b6ed84c6c)


### 3. Entitas Utama 

#### A. Customer  

| Nama Atribut   | Tipe Data    | Keterangan                     |
| -------------- | ------------ | ------------------------------ |
| ID_Customer    | VARCHAR(10)  | Primary key, ID unik customer  |
| nama_customer  | VARCHAR(30)  | Nama lengkap customer          |
| alamat         | VARCHAR(50)  | Alamat tempat tinggal customer |
| no_telp        | VARCHAR(15)  | Nomor telepon customer         |


#### B. Penyewaan 

| Nama Atribut         | Tipe Data   | Keterangan                     |
| -------------------- | ----------- | ------------------------------ |
| ID_Penyewaan         | VARCHAR(10) | Primary key, ID unik penyewaan |
| ID_Customer          | VARCHAR(10) | Foreign key dari Customer      |
| tanggal_sewa         | DATE        | Tanggal awal penyewaan         |
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
| ID_Customer    | VARCHAR(10)  | Foreign key dari Customer                  |
| ID_Penyewaan   | VARCHAR(10)  | Foreign key dari Penyewaan                 |


#### F. Bayar 

| Nama Atribut  | Tipe Data     | Keterangan                               |
| ------------- | ------------- | ---------------------------------------- |
| ID_Bayar      | VARCHAR(10)   | Primary key, ID unik pembayaran          |
| metode_bayar  | VARCHAR(50)   | Metode pembayaran (tunai, transfer, dll) |
| total_bayar   | DECIMAL(10,2) | Total jumlah yang dibayarkan             |
| ID_Customer   | VARCHAR(10)   | Foreign key dari Customer                |
| Status_Barang | VARCHAR(50)   | Foreign key dari Status_Barang           |


### 4. ERD 
![image](https://github.com/user-attachments/assets/cdafc97a-01c1-4c31-b05d-394ada849867)




### 5. Class Diagram 
![image](https://github.com/user-attachments/assets/442d80eb-4250-4325-9799-aad0612dfd1a)


### 6. Mock Up 
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







### 7. Fakta Integritas 
![image](https://github.com/user-attachments/assets/bb267377-a244-4034-9e8a-5d2b720f6be8)


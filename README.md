# **Dokumentasi Aplikasi Gudang dengan Alur Kerja (Flow)**

## **1. Penerimaan Barang dengan Pengecekan Kelengkapan**

### **1.1. Alur Kerja Penerimaan Barang dengan Pengecekan Kelengkapan**

1. **Barang Tiba di Gudang**:

   - Barang tiba di gudang sesuai dengan pesanan dari tim purchasing.
   - Pengguna menentukan apakah barang tersebut untuk **Stok Umum** atau **PO Pelanggan**.

2. **Pengecekan Kesesuaian Barang**:

   - Tim gudang memeriksa barang yang datang dengan daftar pesanan dari tim purchasing.
   - Pengecekan meliputi jenis barang, jumlah, spesifikasi lain seperti ukuran, jenis material, dan kelengkapan berdasarkan packing list yang disediakan oleh vendor.

3. **Pencetakan Ceklis Pengecekan Barang**:

   - Sistem mencetak **Ceklis Pengecekan Barang** yang berisi daftar komponen atau item yang harus ada dalam pengiriman.
   - Ceklis ini digunakan oleh tim gudang untuk memeriksa setiap komponen dan memastikan bahwa semua item dalam pengiriman sesuai.

4. **Proses Pengecekan Barang**:

   - Tim gudang menggunakan ceklis tersebut untuk memeriksa kelengkapan barang.
   - Setiap item pada ceklis dicentang jika lengkap atau ditandai jika ada yang kurang.

5. **Penandaan Status Barang**:

   - Setelah pengecekan selesai, status barang diberi label sebagai **Lengkap** atau **Tidak Lengkap**.
   - Jika barang lengkap, statusnya dicatat dalam sistem sebagai "Lengkap".
   - Jika ada komponen yang kurang, barang diberi label "Tidak Lengkap", dan ini dicatat dalam sistem.

6. **Penanganan Barang Tidak Lengkap**:

   - Untuk barang yang tidak lengkap, tim gudang mengomunikasikan masalah ini dengan tim purchasing atau vendor untuk tindakan lebih lanjut, seperti pengiriman ulang atau penggantian barang yang kurang.
   - Sistem mencatat status barang sebagai "Tidak Lengkap" dan menunggu resolusi.

7. **Pencatatan Barang Masuk**:

   - Jika barang dinyatakan lengkap atau setelah resolusi, barang dicatat secara resmi dalam sistem.

8. **Level Approval**:

   - Setelah pencatatan, transaksi memerlukan persetujuan dari atasan untuk memastikan bahwa barang yang masuk sudah sesuai dengan pesanan.

9. **Pencetakan Surat Tanda Terima Barang**:

   - Setelah approval, sistem mencetak surat tanda terima barang yang mencakup detail barang, status kelengkapan, dan jumlah.

10. **Penempatan Barang di Lokasi Penyimpanan**:
    - Barang kemudian ditempatkan di lokasi penyimpanan yang sesuai di gudang, dan lokasi dicatat dalam sistem.

### **1.2. Flowchart Penerimaan Barang dengan Pengecekan Kelengkapan**

```plaintext
[Barang Tiba di Gudang]
     --> [Pengecekan Kesesuaian Barang]
     --> [Pencetakan Ceklis Pengecekan Barang]
     --> [Proses Pengecekan Barang]
         --> [Penandaan Status Barang]
             --> [Barang Lengkap] --> [Pencatatan Barang Masuk]
             --> [Barang Tidak Lengkap] --> [Penanganan Barang Tidak Lengkap]
     --> [Level Approval]
     --> [Pencetakan Surat Tanda Terima Barang]
     --> [Penempatan Barang di Lokasi Penyimpanan]
```

---

## **2. Pengiriman Barang ke Customer**

### **2.1. Alur Kerja Pengiriman Barang ke Customer**

1. **Permintaan Pengiriman Barang**:

   - Tim sales atau departemen terkait mengajukan permintaan pengiriman barang ke customer.
   - Permintaan ini harus mencakup detail pesanan, jumlah, dan informasi pelanggan.
   - Permintaan harus disetujui oleh atasan sebelum diproses.

2. **Pengecekan Ketersediaan Stok**:

   - Sistem memeriksa ketersediaan stok untuk memastikan bahwa barang tersedia dan siap untuk dikirim.

3. **Pengambilan Barang dari Gudang**:

   - Barang diambil dari lokasi penyimpanan berdasarkan informasi yang ada di sistem.

4. **Pengecekan Kelengkapan (Packing List)**:

   - Sistem mencetak packing list untuk memastikan semua komponen barang yang akan dikirim lengkap.
   - Barang dicek dan dikemas sesuai standar perusahaan.

5. **Verifikasi Ulang dengan Tim Sales**:

   - Sebelum barang dikirim, dilakukan verifikasi ulang dengan tim sales untuk memastikan pesanan sesuai dengan permintaan customer.

6. **Pengurangan Stok**:

   - Setelah verifikasi, sistem mengurangi stok barang sesuai dengan jumlah yang akan dikirim.

7. **Pencetakan Surat Jalan**:

   - Sistem mencetak surat jalan yang akan menyertai pengiriman barang ke customer.

8. **Pengiriman Barang ke Customer**:

   - Barang dikirim ke customer sesuai dengan detail pesanan.

9. **Konfirmasi Penerimaan oleh Customer**:
   - Customer mengonfirmasi penerimaan barang, dan transaksi dianggap selesai.

### **2.2. Flowchart Pengiriman Barang ke Customer**

```plaintext
[Permintaan Pengiriman Barang] --> [Pengecekan Ketersediaan Stok]
                                --> [Pengambilan Barang dari Gudang]
                                --> [Pengecekan Kelengkapan (Packing List)]
                                --> [Verifikasi Ulang dengan Tim Sales]
                                --> [Pengurangan Stok]
                                --> [Pencetakan Surat Jalan]
                                --> [Pengiriman Barang ke Customer]
                                --> [Konfirmasi Penerimaan oleh Customer]
```

---

## **3. Pemindahan Barang Antar Lokasi**

### **3.1. Alur Kerja Pemindahan Barang**

1. **Permintaan Pemindahan Barang**:

   - Permintaan diajukan untuk memindahkan barang ke lokasi lain (misalnya gudang lain atau showroom).
   - Detail yang diperlukan mencakup detail barang, jumlah, dan lokasi tujuan.
   - Permintaan ini harus disetujui oleh atasan sebelum diproses.

2. **Pengecekan Ketersediaan Stok**:

   - Sistem memeriksa ketersediaan stok untuk memastikan barang tersedia dan siap dipindahkan.

3. **Pengambilan Barang dari Gudang**:

   - Barang diambil dari lokasi penyimpanan di gudang berdasarkan informasi yang ada di sistem.

4. **Pengecekan Kelengkapan Barang (Packing List)**:

   - Sistem mencetak packing list yang mencakup semua komponen yang harus ada untuk setiap produk yang dipindahkan.

5. **Pengepakan Barang**:

   - Barang yang telah dicek dan dipastikan lengkap dikemas dengan baik untuk dipindahkan ke lokasi baru.

6. **Pencatatan Lokasi Stok Baru**:

   - Sistem diperbarui untuk mencatat bahwa barang telah dipindahkan ke lokasi baru (gudang lain atau showroom).

7. **Pencetakan Dokumen Transfer Barang**:

   - Sistem mencetak dokumen transfer barang yang mencakup detail barang dan tujuan lokasi baru.

8. **Pengiriman Barang ke Lokasi Baru**:

   - Barang dikirim ke lokasi tujuan dengan dokumen yang sesuai.

9. **Konfirmasi Penerimaan di Lokasi Baru**:
   - Penerima di lokasi baru mengonfirmasi penerimaan barang, dan sistem diperbarui untuk mencatat bahwa barang telah diterima di lokasi yang baru.

### **3.2. Flowchart Pemindahan Barang Antar Lokasi**

```plaintext
[Permintaan Pemindahan Barang] --> [Pengecekan Ketersediaan Stok]
                                 --> [Pengambilan Barang dari Gudang]
                                 --> [Pengecekan Kelengkapan Barang (Packing List)]
                                 --> [Pengepakan Barang]
                                 --> [Pencatatan Lokasi Stok Baru]
                                 --> [Pencetakan Dokumen Transfer Barang]
                                 --> [Pengiriman Barang ke Lokasi Baru]
                                 --> [Konfirmasi Penerimaan di Lokasi Baru]
```

---

## **4. Manajemen Data Produk**

### **4.1. Alur Kerja Manajemen Data Produk**

1. **Penambahan Produk Baru**:

   - Pengguna dapat menambahkan produk baru ke dalam sistem dengan detail lengkap seperti nama, deskripsi, kategori, ukuran, jenis material, dan vendor.

2. **Pengeditan Produk**:

   - Produk yang sudah ada dapat diedit untuk memperbarui informasi seperti stok, harga, atau spesifikasi lainnya.

3. **Penghapusan Produk**:

   - Pengguna dapat menghapus produk dari sistem jika tidak lagi relevan.

4. **Pengelolaan Kategori dan Vendor**:

   - Sistem memungkinkan pengelolaan kategori produk dan vendor yang terkait dengan produk-produk tertentu.

5. **Laporan Data Produk**:
   - Sistem menghasilkan laporan tentang produk yang tersedia, termasuk jumlah stok dan pergerakan produk.

### **4.2. Flowchart Manajemen Data Produk**

```plaintext
[Penambahan Produk Baru] --> [Pengeditan Produk] --> [Penghapusan Produk]
                          --> [Pengelolaan Kategori dan Vendor]
                          --> [Laporan Data Produk]
```

---

## **5. Manajemen Jadwal Pengiriman**

### **5.1. Alur Kerja Manajemen Jadwal Pengiriman**

1. **Penjadwalan Pengiriman Barang**:
   - Pengguna dapat

membuat jadwal pengiriman barang berdasarkan prioritas atau tenggat waktu tertentu.

2. **Kalender Pengiriman**:

   - Sistem menampilkan jadwal pengiriman dalam bentuk kalender untuk memudahkan manajemen jadwal.

3. **Notifikasi dan Reminder**:

   - Sistem mengirimkan notifikasi dan reminder kepada tim terkait untuk pengiriman yang akan datang.

4. **Reschedule Pengiriman**:

   - Pengguna dapat melakukan penjadwalan ulang (reschedule) jika terjadi perubahan rencana.

5. **Tracking Status Pengiriman**:
   - Sistem melacak status pengiriman dari persiapan, pengiriman, hingga konfirmasi penerimaan di tujuan.

### **5.2. Flowchart Manajemen Jadwal Pengiriman**

```plaintext
[Penjadwalan Pengiriman Barang] --> [Kalender Pengiriman]
                                  --> [Notifikasi dan Reminder]
                                  --> [Reschedule Pengiriman]
                                  --> [Tracking Status Pengiriman]
```

---

## **6. Manajemen Notifikasi**

### **6.1. Alur Kerja Manajemen Notifikasi**

1. **Peringatan Stok Menipis**:

   - Sistem mengirimkan notifikasi jika stok barang menipis di bawah level aman.

2. **Notifikasi Transaksi**:

   - Pengguna menerima notifikasi untuk setiap transaksi penting seperti penerimaan barang, pengiriman barang, dan perpindahan stok.

3. **Notifikasi Tindakan Lanjutan**:
   - Sistem mengirimkan notifikasi untuk tindakan lanjutan yang diperlukan, seperti approval dari atasan atau pengambilan tindakan atas stok yang hampir habis.

### **6.2. Flowchart Manajemen Notifikasi**

```plaintext
[Peringatan Stok Menipis] --> [Notifikasi Transaksi]
                            --> [Notifikasi Tindakan Lanjutan]
```

---

## **7. Penanganan Barang Rusak / Return**

### **7.1. Alur Kerja Penanganan Barang Rusak / Return**

1. **Permintaan Pengembalian Barang**:

   - Tim sales atau departemen lain mengajukan permintaan pengambilan barang untuk keperluan return atau karena barang rusak.

2. **Pembuatan Surat Tugas Pengambilan Barang**:

   - Sistem menghasilkan surat tugas pengambilan barang berdasarkan permintaan yang diajukan.

3. **Pengambilan dan Pengiriman Barang ke Gudang**:

   - Barang yang diambil dari lokasi dikirim kembali ke gudang untuk pemeriksaan lebih lanjut.

4. **Pengecekan Barang di Gudang**:

   - Barang diperiksa untuk menentukan kondisinya, apakah dapat diperbaiki atau tidak.

5. **Klasifikasi Barang Rusak**:

   - Barang rusak diklasifikasikan sebagai barang yang tidak dapat diperbaiki (dihapus dari stok) atau yang dapat diperbaiki (menunggu keputusan lebih lanjut).

6. **Permintaan Perbaikan**:

   - Tim sales mengajukan permintaan perbaikan resmi jika barang bisa diperbaiki.

7. **Pengiriman Barang ke Vendor untuk Perbaikan**:

   - Barang yang perlu diperbaiki dikirim ke vendor, dan sistem mencatatnya sebagai "Dalam Perbaikan".

8. **Pemantauan dan Pengembalian Barang dari Vendor**:
   - Sistem memantau status perbaikan hingga barang dikembalikan dari vendor, dan diperiksa ulang sebelum dimasukkan kembali ke stok.

### **7.2. Flowchart Penanganan Barang Rusak / Return**

```plaintext
[Permintaan Pengembalian Barang] --> [Pembuatan Surat Tugas Pengambilan Barang]
                                   --> [Pengambilan dan Pengiriman Barang ke Gudang]
                                   --> [Pengecekan Barang di Gudang]
                                   --> [Klasifikasi Barang Rusak]
                                   --> [Permintaan Perbaikan]
                                   --> [Pengiriman Barang ke Vendor untuk Perbaikan]
                                   --> [Pemantauan dan Pengembalian Barang dari Vendor]
```

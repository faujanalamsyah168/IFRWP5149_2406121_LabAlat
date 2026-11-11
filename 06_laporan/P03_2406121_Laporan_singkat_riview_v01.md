### 1. Deskripsi Kegiatan
Praktikum pertemuan ketiga ini berfokus pada pemodelan tingkat lanjut dalam *Use Case Diagram*, yaitu penulisan relasi `<<include>>` dan `<<extend>>`. Praktikan diminta untuk menganalisis dua skenario sistem (Sistem Informasi Peminjaman Peralatan Laboratorium dan Sistem Informasi Akademik) untuk memisahkan mana fungsi utama, mana perilaku wajib (include), dan mana perilaku tambahan bersyarat (extend). 

### 2. Langkah Kerja
1.  **Identifikasi Kebutuhan & Aktor:** Menganalisis tabel kebutuhan (LAB-R01 s.d. LAB-R06 dan SIA-R01 s.d. SIA-R06) serta menentukan aktor yang terlibat beserta tujuannya.
2.  **Katalogisasi Use Case:** Menyusun katalog *use case* beserta perannya (fungsi utama, perilaku yang disertakan, atau tambahan bersyarat).
3.  **Pemodelan Diagram:** Menggambar *Use Case Diagram* di *draw.io*, memastikan aktor berada di luar batas sistem, dan menghubungkan relasi `include` serta `extend` dengan arah panah yang benar.
4.  **Penyusunan Deskripsi:** Membuat tabel deskripsi rinci untuk setiap *use case* (Skenario Utama, Prasyarat, Alur Utama, Alur Alternatif, dan *Extension Point*).
5.  **Validasi Logbook:** Memastikan semua poin pada logbook P03 terpenuhi (seperti letak *extension point*, pembedaan prasyarat vs include, dan ekspor gambar yang sesuai).

### 3. Hasil Pemodelan dan Analisis Relasi
**A. Sistem Laboratorium (LAB):**
*   **Include:** `LAB-UC03 Ajukan peminjaman` memanggil `LAB-UC04 Periksa ketersediaan`. Hal ini karena pemeriksaan stok adalah syarat mutlak sebelum pengajuan bisa disimpan.
*   **Extend:** `LAB-UC05 Cetak bukti pengajuan` mengextend `LAB-UC03`. Kondisi: *[mahasiswa memilih cetak]* pada *Extension point* konfirmasi pengajuan. Pengajuan tetap berhasil meski tanpa mencetak bukti.

**B. Sistem Informasi Akademik (SIA):**
*   **Include:** `SIA-UC03 Ajukan KRS` memanggil `SIA-UC04 Validasi KRS`. Proses validasi (cek prasyarat, benturan jadwal) wajib dijalankan setiap kali KRS diajukan.
*   **Extend:** `SIA-UC05 Unduh bukti pengajuan KRS` mengextend `SIA-UC03`. Kondisi: *[mahasiswa memilih mengunduh bukti]*.

### 4. Pembahasan
Penerapan relasi `<<include>>` dan `<<extend>>` sangat penting untuk menjaga modularitas diagram. Pada praktikum ini, `<<include>>` berhasil diterapkan pada proses validasi/pemeriksaan yang bersifat wajib (tidak bisa dihindari). Sementara itu, `<<extend>>` diterapkan pada fitur tambahan (cetak/unduh bukti) yang sifatnya opsional. 
Selain itu, pemisahan antara **Prasyarat** (misal: *Mahasiswa telah terautentikasi*) dengan **Include** (misal: *Sistem memanggil UC Validasi*) sudah dibedakan dengan jelas pada tabel deskripsi. Alur alternatif juga telah menggambarkan skenario kegagalan (misal: validasi gagal atau stok tidak tersedia), sehingga rancangan sistem menjadi lebih komprehensif dan siap dikembangkan.

### 5. Kesimpulan
Berdasarkan praktikum yang telah dilakukan, dapat disimpulkan bahwa:
1.  Praktikan berhasil memodelkan *Use Case Diagram* dengan relasi `include` dan `extend` yang tepat sesuai kaidah UML.
2.  Praktikan mampu membedakan perilaku wajib (*include*) dan perilaku opsional bersyarat (*extend*) beserta penentuan *extension point*-nya.
3.  Seluruh artefak yang dihasilkan (diagram, tabel katalog, tabel deskripsi, dan tabel analisis model) telah konsisten, saling terhubung, dan memenuhi standar kelayakan sesuai *checklist* pada logbook.
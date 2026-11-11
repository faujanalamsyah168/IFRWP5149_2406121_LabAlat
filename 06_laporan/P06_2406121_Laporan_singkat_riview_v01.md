### 1. Deskripsi Kegiatan
Praktikum pertemuan kelima ini berfokus pada penulisan **Skenario Use Case** (Use Case Description). Tugas utama praktikan adalah menerjemahkan diagram kumulatif dari Pertemuan 4 ke dalam bentuk narasi tekstual yang rinci dan terstruktur. Skenario ini mencakup alur normal (sukses), skenario alternatif (penanganan error/kondisi khusus), dan skenario akhir, dengan memisahkan secara tegas antara aksi yang dilakukan aktor dan respon yang diberikan oleh sistem.

### 2. Langkah Kerja
1.  **Identifikasi Use Case:** Mengacu pada diagram P04, mengidentifikasi seluruh *use case* beserta relasinya (Asosiasi, Include, Extend, Generalization, Realization).
2.  **Penyusunan Tabel Skenario:** Membuat tabel berisi kolom Nama Use Case, Aktor, Tujuan, Deskripsi, dan tabel utama dua kolom (Kegiatan vs. Respon Sistem).
3.  **Penulisan Skenario Normal:** Menuliskan langkah-langkah sukses secara berurutan (satu aksi per langkah) beserta respon sistem yang sesuai.
4.  **Penanganan Relasi:** 
    *   Menerapkan `<<include>>` sebagai rujukan ke tabel lain (tidak menyalin langkah).
    *   Menerapkan `<<extend>>` sebagai skenario alternatif dengan mencantumkan *condition* dan *extension point*.
    *   Menerapkan *Generalization* dengan hanya menulis perilaku pembeda pada *use case* khusus dan merujuk ke *use case* umum.
5.  **Penyusunan Skenario Alternatif dan Akhir:** Menuliskan cabang-cabang kegagalan (misal: validasi gagal, stok habis) dengan penomoran lanjutan, serta mendefinisikan kondisi akhir dari *use case* tersebut.
6.  **Validasi Logbook:** Memastikan semua instruksi pada logbook P05 terpenuhi, termasuk konsistensi nama, ID, dan pengecualian khusus untuk aktor Kepala Laboratorium (LAB-UC07).

### 3. Hasil Pekerjaan
Praktikan berhasil menyusun **12 tabel skenario untuk Sistem Laboratorium (LAB)** dan **13 tabel skenario untuk Sistem Informasi Akademik (SIA)**. Beberapa poin penting dari hasil pekerjaan ini antara lain:
*   **Skenario Umum & Khusus:** SIA-UC10 (Kelola Data Mahasiswa) ditulis sebagai skenario umum, sedangkan SIA-UC11 (Tambah), UC12 (Ubah), dan UC13 (Hapus) hanya memuat perilaku pembeda dan merujuk kembali ke SIA-UC10. Hal yang sama diterapkan pada LAB-UC02 dengan turunannya.
*   **Skenario Aktor Umum:** SIA-UC07 (Lihat Kalender Akademik) ditulis satu kali atas nama aktor umum (Civitas Akademika), mencakup perilaku untuk Mahasiswa dan Dosen.
*   **Konsistensi Kolaborasi:** *Collaboration* seperti LAB-CO02 disebutkan pada keterangan tabel LAB-UC11, menunjukkan bahwa *use case* tersebut direalisasikan oleh kolaborasi terkait, tanpa menambahkan langkah aktivitas baru.
*   **Kasus Khusus:** Tabel LAB-UC07 (Lihat Laporan Peminjaman) ditulis berdiri sendiri tanpa memuat relasi *include* atau *extend*, sesuai dengan aturan bahwa Kepala Laboratorium hanya memiliki satu *use case* tersebut.

### 4. Pembahasan
Penulisan skenario *use case* menuntut ketelitian tinggi dalam memisahkan aksi manusia (aktor) dan aksi mesin (sistem). Pada pengerjaan ini, penerapan tabel dua kolom (Kegiatan vs. Respon Sistem) terbukti sangat efektif untuk memvisualisasikan aliran interaksi. 

Tantangan utama dalam praktikum ini adalah menerapkan konsep **Generalization** dan **Relasi**. Untuk *Generalization*, praktikan tidak diperkenankan menduplikasi tabel untuk aktor atau *use case* yang memiliki perilaku yang sama. Oleh karena itu, penggunaan rujukan antar-tabel (misal: *"Langkah bersama mengikuti Tabel SIA-UC10"*) sangat krusial untuk menjaga efisiensi dokumen. Sementara itu, penulisan *Extend* berhasil ditempatkan dengan tepat pada Skenario Alternatif, karena sifatnya yang opsional dan bergantung pada kondisi tertentu (misal: *"Jika mahasiswa memilih unduh bukti"*). Penulisan alur alternatif ini juga memastikan bahwa sistem memiliki penanganan yang jelas jika terjadi kegagalan (seperti input nilai di luar rentang yang sah).

### 5. Kesimpulan
Berdasarkan praktikum yang telah dilakukan, dapat disimpulkan bahwa:
1.  Praktikan telah berhasil menerjemahkan diagram *Use Case* yang kompleks menjadi dokumen spesifikasi tekstual (Skenario *Use Case*) yang rinci, terstruktur, dan mudah dipahami.
2.  Praktikan mampu menerapkan aturan penomoran, pemisahan aktor-sistem, serta relasi `<<include>>`, `<<extend>>`, dan *Generalization* sesuai dengan kaidah penulisan skenario UML yang benar.
3.  Seluruh artefak pendukung (skenario LAB dan SIA, metadata) telah disusun secara konsisten dengan diagram P04 dan memenuhi seluruh *checklist* evaluasi yang dipersyaratkan.
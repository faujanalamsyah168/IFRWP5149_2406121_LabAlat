### 1. Deskripsi Kegiatan
Praktikum pertemuan keempat ini berfokus pada penerapan teknik pemodelan tingkat lanjut dalam *Use Case Diagram*, yaitu **Generalization** (pewarisan) dan **Collaboration** (kolaborasi yang merealisasikan *use case*). Praktikan diminta untuk mengembangkan diagram dari pertemuan sebelumnya (bersifat kumulatif) dengan menambahkan aktor umum, *use case* umum, serta entitas *collaboration* untuk memodelkan sistem Laboratorium dan Sistem Informasi Akademik (SIA) secara lebih mendalam.

### 2. Langkah Kerja
1.  **Analisis Skenario Baru:** Membaca skenario P04 untuk LAB (penambahan aktor Dosen dan proses pengembalian alat) dan SIA (layanan hasil studi seperti input nilai dan KHS).
2.  **Identifikasi Generalization:** Menentukan aktor umum (Peminjam untuk LAB, Civitas Akademika untuk SIA) dan *use case* umum (Kelola Data Peralatan/Mahasiswa) beserta turunannya (Tambah, Ubah, Hapus).
3.  **Pemodelan Collaboration:** Menggambar *use case* Collaboration sebagai elips garis putus-putus (misal: `LAB-CO02`) dan menghubungkannya dengan garis putus-putus *realization* ke *use case* utamanya.
4.  **Penyusunan Deskripsi & Model Analisis:** Memperbarui tabel deskripsi (seperti penambahan alur untuk Catat Pengembalian dan Input Nilai) serta menyusun tabel spesifikasi hubungan (Model Analisis) yang mencakup asosiasi, *include*, *extend*, *generalization*, dan *realization*.
5.  **Validasi Logbook:** Memastikan semua instruksi terpenuhi, termasuk tidak menimpa file P03, menandai kebutuhan yang belum dimodelkan (seperti denda) sebagai pertanyaan terbuka, dan menjawab studi kasus Situasi A, B, C.

### 3. Hasil Pemodelan dan Analisis
**A. Sistem Laboratorium (LAB):**
*   **Aktor:** Terdapat aktor umum `Peminjam` yang diwarisi oleh `Mahasiswa` dan `Dosen`. Asosiasi fungsi `Lihat Ketersediaan` dan `Ajukan Peminjaman` ditarik dari aktor umum.
*   **Use Case:** `LAB-UC08`, `UC09`, dan `UC10` (Tambah/Ubah/Hapus) merupakan *use case* khusus yang mewarisi `LAB-UC02 Kelola Data Peralatan`.
*   **Collaboration:** `LAB-CO01` merealisasikan `Ajukan Peminjaman`, dan `LAB-CO02` merealisasikan `Catat Pengembalian Peralatan` (yang di dalamnya terdapat `<<include>>` ke `Periksa Kondisi Peralatan`).

**B. Sistem Informasi Akademik (SIA):**
*   **Aktor:** Aktor umum `Civitas Akademika` mewariskan fungsi `Lihat Kalender Akademik`. Aktor `Mahasiswa` dan `Dosen` adalah aktor khususnya.
*   **Use Case:** `SIA-UC11`, `UC12`, dan `UC13` (Tambah/Ubah/Hapus Data Mahasiswa) merupakan turunan dari `SIA-UC10 Kelola Data Mahasiswa`.
*   **Collaboration:** `SIA-CO01` merealisasikan `Input Nilai Mata Kuliah`, dan `SIA-CO02` merealisasikan `Lihat KHS`.

**C. Jawaban Jobsheet Review (Situasi A, B, C):**
*   **Situasi A:** Mahasiswa tidak perlu garis asosiasi langsung ke Kalender Akademik karena fungsi tersebut diwariskan dari aktor umum `Civitas Akademika`.
*   **Situasi B:** Dosen yang bukan pengampu akan ditolak aksesnya oleh sistem (sesuai Alur Alternatif A1 pada SIA-UC08).
*   **Situasi C:** Sistem akan mencegah/menolak proses hapus data karena aturan bisnis melarang penghapusan mahasiswa yang masih memiliki data akademik aktif.

### 4. Pembahasan
Penerapan **Generalization** pada diagram ini sangat efektif untuk mengurangi redundansi. Dengan menarik garis asosiasi hanya dari aktor umum (`Peminjam` atau `Civitas Akademika`), diagram menjadi lebih bersih tanpa mengurangi makna fungsionalitas, karena aktor khusus secara otomatis mewarisi hak akses tersebut. 

Di sisi lain, penggunaan **Collaboration** dan **Realization** memberikan dimensi teknis pada *Use Case Diagram*. *Collaboration* (digambarkan dengan elips putus-putus) menunjukkan bagaimana sebuah *use case* (yang bersifat logis/konseptual) diwujudkan (*realized*) oleh sekumpulan objek atau kelas yang saling berinteraksi. Hal ini menjembatani antara analisis kebutuhan pengguna dengan desain sistem yang sebenarnya, memastikan bahwa setiap fungsi utama memiliki rancangan implementasi yang jelas.

### 5. Kesimpulan
Berdasarkan praktikum yang telah dilakukan, dapat disimpulkan bahwa:
1.  Praktikan berhasil mengembangkan *Use Case Diagram* kumulatif dengan menerapkan relasi **Generalization** (pada aktor dan *use case*) serta **Collaboration & Realization** secara tepat sesuai kaidah UML.
2.  Praktikan mampu menganalisis aturan bisnis (*business rules*) dan pengecualian sistem dengan baik, yang dibuktikan melalui jawaban analisis situasi dan penyusunan alur alternatif pada tabel deskripsi.
3.  Seluruh artefak pendukung (skenario, kebutuhan, deskripsi, dan model analisis) telah disusun secara konsisten, tertelusur dengan baik (*traceability*), dan memenuhi seluruh *checklist* yang dipersyaratkan dalam logbook praktikum.
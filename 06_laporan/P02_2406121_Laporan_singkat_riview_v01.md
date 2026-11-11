### 1. Deskripsi Kegiatan
Praktikum pertemuan kedua ini berfokus pada pemodelan **Use Case Diagram** dan kegiatan **Review (evaluasi)**. Praktikan dituntut untuk mampu menerjemahkan dua skenario sistem yang berbeda (Sistem Laboratorium dan Sistem Informasi Akademik) ke dalam bentuk diagram Use Case, serta mampu mengidentifikasi kesalahan notasi pada diagram yang diberikan untuk kemudian diperbaiki sesuai kaidah standar UML.

### 2. Langkah Kerja
1.  **Analisis Skenario:** Membaca dua skenario utama, yaitu `P02_LAB_skenario_v01.md` (interaksi Mahasiswa dan Petugas Lab terkait peralatan) dan `P02_SIA_skenario_v01.md` (interaksi Mahasiswa dan Admin Akademik terkait jadwal kuliah).
2.  **Pemodelan Diagram:** Menggambar Use Case Diagram menggunakan *draw.io* untuk kedua skenario tersebut.
3.  **Review Diagram:** Mengevaluasi sebuah diagram *Use Case* yang salah (terlampir pada gambar ketiga) dan mencatat temuan beserta perbaikannya ke dalam *jobsheet review*.
4.  **Validasi Logbook:** Memastikan seluruh hasil pemodelan memenuhi *checklist* pada `P02_2406121_logbook_v01.md` (misal: aktor di luar sistem, *use case* berbentuk elips, dll).

### 3. Hasil Pemodelan dan Review
**A. Hasil Pemodelan (Sesuai Skenario):**
*   **Diagram Lab:** Memuat 1 aktor (Mahasiswa) dengan fungsi "Lihat ketersediaan peralatan", dan 1 aktor (Petugas Laboran) dengan fungsi "Kelola data peralatan" di dalam batas sistem peminjaman.
*   **Diagram SIA:** Memuat aktor (Mahasiswa) dengan *use case* "Lihat jadwal kuliah", dan aktor (Admin Akademik) dengan *use case* "Kelola jadwal kuliah" di dalam batas sistem informasi akademik.
*   **Logbook:** Seluruh poin *checklist* pada logbook telah terpenuhi (sesuai format, tidak ada panah urutan antar-fungsi, dan ekspor sesuai sumber).

**B. Temuan Review (Jobsheet Review):**
Berdasarkan pemeriksaan diagram yang salah, ditemukan 4 hal yang diperbaiki:
1.  **Nama Sistem:** Judul "Sistem Laboratorium" salah, harus diubah menjadi **"Sistem Informasi Akademik"** karena konteks kasusnya adalah jadwal kuliah.
2.  **Notasi Fungsi:** "Lihat jadwal" yang awalnya berbentuk kotak harus diubah menjadi **bentuk elips/bulat**, karena merepresentasikan sebuah *use case*.
3.  **Relasi Aktor:** "Kelola jadwal kuliah" harus dihubungkan (diberi garis asosiasi) ke aktor **"Admin Akademik"**, bukan Mahasiswa.
4.  **Posisi Aktor:** Aktor Mahasiswa harus diletakkan **di luar batas sistem** (*system boundary*), karena aktor adalah entitas eksternal.

### 4. Pembahasan
Dalam pemodelan Use Case Diagram, ketepatan notasi sangat penting. Hasil review menunjukkan bahwa kesalahan umum sering terjadi pada penempatan batasan sistem dan bentuk geometris. Sebuah fungsi/layanan sistem wajib digambarkan dengan elips (Use Case), sedangkan aktor (pengguna) harus berada di luar kotak sistem karena mereka yang mengoperasikan sistem, bukan bagian dari sistem itu sendiri. Selain itu, garis asosiasi (hubungan) harus tepat menyambungkan aktor dengan fungsi yang berhak diaksesnya sesuai skenario. Melalui latihan ini, pemahaman mengenai pemisahan hak akses (misal: Mahasiswa hanya bisa melihat, Admin yang mengelola) dapat divisualisasikan dengan benar.

### 5. Kesimpulan
Berdasarkan praktikum yang telah dilakukan, dapat disimpulkan bahwa:
1.  Praktikan berhasil membuat **Use Case Diagram** untuk dua sistem berbeda (Lab dan SIA) sesuai dengan standar notasi UML yang benar.
2.  Praktikan mampu melakukan **review/evaluasi** terhadap diagram yang cacat dan memberikan perbaikan berdasarkan kaidah perancangan sistem (seperti memperbaiki bentuk *use case* dan penempatan aktor).
3.  Seluruh artefak praktikum (skenario, metadata, diagram, dan logbook) telah dikerjakan dengan konsisten dan memenuhi standar kelayakan validasi tugas.
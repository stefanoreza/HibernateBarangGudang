HibernateBarangGudang

Sistem sederhana untuk manajemen data barang gudang menggunakan Java dan Hibernate (ORM).
Proyek ini ditujukan sebagai contoh atau dasar pengembangan aplikasi inventaris gudang berbasis Java dengan pemetaan objek-relasional.

📑 Daftar Isi

Deskripsi Proyek

Fitur

Struktur Proyek

Persyaratan Sistem

Instalasi

Konfigurasi Hibernate

Cara Menjalankan

Contoh Penggunaan

Dependensi

Troubleshooting

Kontributor

Lisensi

📘 Deskripsi Proyek

HibernateBarangGudang adalah aplikasi Java yang menggunakan Hibernate untuk mengakses dan mengelola data barang dalam sebuah gudang.
Proyek ini mencakup model data, konfigurasi Hibernate, serta mekanisme dasar CRUD untuk entitas gudang/barang.

Repository ini bisa digunakan sebagai:

Contoh belajar Hibernate

Kerangka awal proyek inventaris

Template ORM Java dengan Ant Build

✨ Fitur

Pemodelan entitas Barang / Gudang dengan Hibernate

Operasi CRUD dasar

Mapping database otomatis

Struktur build menggunakan Apache Ant

Dapat dikembangkan menjadi aplikasi inventaris lengkap

📁 Struktur Proyek
HibernateBarangGudang/
│
├── nbproject/        → Konfigurasi NetBeans
├── reports/          → Output laporan (opsional)
├── src/              → Kode sumber Java & Hibernate
├── build.xml         → Script build Apache Ant
├── manifest.mf       → Manifest aplikasi
└── .gitignore

🖥️ Persyaratan Sistem

Pastikan telah menginstal:

Java JDK 8+

Database (MySQL / PostgreSQL / lainnya)

Apache Ant (jika ingin build via Ant)

Hibernate (akan dimasukkan sebagai library di proyek)

🔧 Instalasi

Clone repository:

git clone https://github.com/stefanoreza/HibernateBarangGudang.git


Buka menggunakan IDE Java seperti:

NetBeans (default project)

IntelliJ IDEA

Eclipse

Pastikan library Hibernate dan JDBC driver sudah dimasukkan ke classpath.

⚙️ Konfigurasi Hibernate

Cari file konfigurasi Hibernate di:

src/hibernate.cfg.xml


Sesuaikan bagian berikut:

<property name="hibernate.connection.url">jdbc:mysql://localhost:3306/nama_database</property>
<property name="hibernate.connection.username">root</property>
<property name="hibernate.connection.password">password</property>
<property name="hibernate.dialect">org.hibernate.dialect.MySQLDialect</property>


Jika belum ada file tersebut, kamu bisa menambahkannya secara manual.

▶️ Cara Menjalankan
Jika menggunakan IDE

Klik Run Project (NetBeans)
atau

Jalankan class utama (main) dari package src.

Jika menggunakan Ant

Jalankan:

ant compile
ant run

🧪 Contoh Penggunaan

Contoh melakukan operasi CRUD melalui DAO:

Barang barang = new Barang();
barang.setNama("Mouse");
barang.setJumlah(10);

BarangDao dao = new BarangDao();
dao.save(barang);

List<Barang> list = dao.getAll();
for (Barang b : list) {
    System.out.println(b.getNama());
}

📦 Dependensi

Tambahkan library berikut:

hibernate-core

hibernate-entitymanager (jika perlu)

mysql-connector-j (jika memakai MySQL)

javax.persistence API

Masukkan ke dalam folder lib/ atau via IDE Project Libraries.

❗ Troubleshooting
Masalah	Solusi
“No suitable driver”	Tambahkan driver JDBC ke classpath
Hibernate tidak membuat tabel	Pastikan hibernate.hbm2ddl.auto=create/update
Error koneksi DB	Periksa URL, username, password
Ant build gagal	Cek Java Home & konfigurasi Ant
👤 Kontributor

Stefano Reza – Pemilik repository

Jika kamu ingin saya tambahkan daftar contributor lain, beri tahu saja.

📄 Lisensi

Proyek ini tidak mencantumkan lisensi.
Jika ingin, saya bisa buatkan rekomendasi lisensi (MIT, Apache 2.0, GPL, dsb).

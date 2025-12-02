# 📦 Sistem Manajemen Inventaris Sederhana (CRUD - Hibernate & MySQL)

Proyek ini adalah aplikasi desktop berbasis Java Swing yang dirancang untuk mengelola data inventaris barang. Aplikasi ini mengimplementasikan operasi CRUD (Create, Read, Update, Delete) dan menggunakan teknologi **Hibernate ORM** sebagai jembatan antara aplikasi Java dan database **MySQL**.

## ✨ Fitur Utama

* **Manajemen Data Barang:** Melakukan operasi Tambah, Ubah, Hapus data barang.
* **Tampilan Data:** Menampilkan seluruh data barang secara real-time di JTable.
* **Validasi Input:** Memastikan integritas data sebelum disimpan ke database.
* **Koneksi ORM:** Menggunakan Hibernate untuk mempermudah interaksi dengan database tanpa perlu menulis native SQL yang kompleks.
* **Laporan (Planned/Future):** Integrasi Jasper Report untuk menghasilkan laporan inventaris yang dapat dicetak (misalnya format PDF).

## 🛠️ Teknologi yang Digunakan

| Kategori | Teknologi | Deskripsi |
| :--- | :--- | :--- |
| **Bahasa Pemrograman** | Java JDK 8+ | Bahasa inti yang digunakan untuk membangun aplikasi. |
| **Antarmuka (GUI)** | Java Swing / NetBeans Designer | Digunakan untuk membangun tampilan antarmuka desktop. |
| **Object-Relational Mapping (ORM)** | **Hibernate ORM** | Memetakan objek Java (`Barang.java`) ke tabel database. |
| **Database** | MySQL | Digunakan sebagai sistem manajemen database. |
| **Konektor** | MySQL Connector/J | Driver untuk koneksi Java ke MySQL. |
| **IDE** | NetBeans / Eclipse | Lingkungan pengembangan yang direkomendasikan. |

## 💾 Struktur Database

Aplikasi ini berinteraksi dengan satu tabel utama di database.

| Kolom | Tipe Data | Keterangan |
| :--- | :--- | :--- |
| `kode_barang` | VARCHAR (PK) | Primary Key, kode unik barang. |
| `nama_barang` | VARCHAR | Nama produk/barang. |
| `stok` | INT | Jumlah stok yang tersedia saat ini. |
| `harga_satuan` | DOUBLE | Harga beli atau harga jual satuan. |
| `kategori` | VARCHAR | Kategori barang (misalnya: Elektronik, Pakaian, Makanan). |

### ⚙️ Konfigurasi Database (MySQL)

Pastikan Anda membuat database dengan nama yang sesuai sebelum menjalankan aplikasi:

```sql
CREATE DATABASE IF NOT EXISTS db_inventaris;

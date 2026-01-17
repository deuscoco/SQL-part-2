# 📘 Basis Data Part 2 – SELECT DISTINCT, Prefix, dan Alias


---

## 📌 Pendahuluan

Pada **Basis Data Part 2**, pembahasan difokuskan pada teknik lanjutan dalam perintah `SELECT`, yaitu penggunaan **SELECT DISTINCT**, **prefix pada kolom**, serta **alias pada kolom dan tabel**. Materi ini sangat penting untuk menghindari duplikasi data, memperjelas sumber kolom, serta membuat hasil query lebih mudah dibaca.

Dokumentasi ini disusun dalam format **Markdown** agar dapat langsung digunakan sebagai **README di GitHub**, sekaligus berisi **jawaban lengkap seluruh quiz** pada modul Basis Data Part 2.

---

## 🗂️ Contoh Tabel: `ms_produk`

| no_urut | kode_produk | nama_produk           | harga |
| ------- | ----------- | --------------------- | ----- |
| 1       | prod-01     | Kotak Pensil DQLab    | 62500 |
| 2       | prod-02     | Flashdisk DQLab 64 GB | 55000 |
| 3       | prod-03     | Buku Tulis DQLab      | 12000 |
| 5       | prod-03     | Buku Tulis DQLab      | 12000 |
| 11      | prod-01     | Kotak Pensil DQLab    | 62500 |
| 12      | prod-03     | Buku Tulis DQLab      | 12000 |

---

## 1️⃣ SELECT DISTINCT

`SELECT DISTINCT` digunakan untuk menghilangkan data duplikat pada hasil query.

### 📘 Quiz 1

**Soal:** Buat query dengan `DISTINCT` untuk menghasilkan data yang tidak duplikat.

**Query (Jawaban):**

```sql
SELECT DISTINCT
    no_urut,
    kode_produk,
    nama_produk,
    harga
FROM ms_produk;
```

---

## 2️⃣ Prefix pada Nama Kolom

Prefix digunakan untuk memperjelas asal kolom, terutama ketika melibatkan lebih dari satu tabel.

### 📘 Quiz 2

**Soal:** Buat query dengan prefix kolom.

**Query (Jawaban):**

```sql
SELECT
    ms_produk.no_urut,
    ms_produk.nama_produk,
    ms_produk.harga
FROM ms_produk;
```

---

## 3️⃣ Alias pada Kolom

Alias digunakan untuk mengganti nama kolom pada hasil output agar lebih mudah dibaca.

### 📘 Quiz 3

**Soal:** Gunakan alias sehingga:

* `no_urut` menjadi `nomor`
* `nama_produk` menjadi `nama`

**Query (Jawaban):**

```sql
SELECT
    no_urut AS nomor,
    nama_produk AS nama
FROM ms_produk;
```

---

## 4️⃣ Alias TANPA Keyword `AS`

Pada SQL, keyword `AS` bersifat opsional.

### 📘 Quiz 4

**Soal:** Gunakan alias tanpa keyword `AS`:

* `no_urut` menjadi `nomor`
* `nama_produk` menjadi `nama`

**Query (Jawaban):**

```sql
SELECT
    no_urut nomor,
    nama_produk nama
FROM ms_produk;
```

---

## 5️⃣ Menggabungkan Prefix & Alias

Prefix dan alias dapat digunakan secara bersamaan.

### 📘 Quiz 5

**Soal:** Tampilkan kolom `harga` dari tabel `ms_produk` dengan alias `harga_jual` dan lengkap dengan prefix.

**Query (Jawaban):**

```sql
SELECT
    ms_produk.harga AS harga_jual
FROM ms_produk;
```

---

## 6️⃣ Alias pada Tabel (Tanpa `AS`)

Alias tabel mempersingkat penulisan nama tabel dalam query.

### 📘 Quiz 6

**Soal:** Ganti nama tabel `ms_produk` menjadi `t2` dan tampilkan seluruh isinya tanpa keyword `AS`.

**Query (Jawaban):**

```sql
SELECT *
FROM ms_produk t2;
```

---

## 7️⃣ Prefix dengan Alias Tabel

Menggunakan alias tabel sebagai prefix kolom.

### 📘 Quiz 7

**Soal:** Gunakan alias tabel `t2` (tanpa `AS`) untuk menampilkan kolom `nama_produk` dan `harga` dengan prefix alias.

**Query (Jawaban):**

```sql
SELECT
    t2.nama_produk,
    t2.harga
FROM ms_produk t2;
```

---

## ✅ Penutup

Dengan memahami penggunaan `SELECT DISTINCT`, prefix, dan alias, kita dapat menghasilkan query SQL yang lebih rapi, jelas, dan efisien. Materi ini menjadi dasar penting sebelum melanjutkan ke query yang lebih kompleks seperti `JOIN`, `UNION`, dan subquery.

---

## 🔗 Referensi

* [https://docs.google.com/document/d/18Dc_2P8xDXz7c1FEO37xxm_4Rxx09i49DOvnigZapaA/edit?usp=sharing]
* [https://www.mysql.com](https://www.mysql.com)
* [https://www.postgresql.org](https://www.postgresql.org)
* [https://learn.microsoft.com/sql](https://learn.microsoft.com/sql)

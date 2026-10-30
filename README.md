# pertemuan-13-debugging-2225250002

---

## Tujuan Repositori

Repositori ini dibuat untuk memenuhi tugas Praktik 4 Pertemuan 13 mata kuliah Algoritma dan Pemrograman. Repositori ini berfokus pada penerapan *debugging*, *tracing*, *testing*, dan penyusunan *test case* menggunakan Python di VS Code. Melalui praktik ini, mahasiswa belajar mengidentifikasi jenis error, menelusuri alur eksekusi program, menemukan akar penyebab bug, memperbaiki kesalahan, serta memastikan hasil perbaikan melalui pengujian ulang (*retest*).

---

## Algoritma Tugas

1. **Menjalankan Program Awal**: Jalankan program `praktik_4_debugging.py` tanpa mengubah kode untuk mengetahui output aktual dan menemukan kemungkinan kesalahan.

2. **Menyusun Test Case**:
   - Buat minimal lima test case untuk menguji fungsi rata-rata, status kelulusan, dan nilai tertinggi.
   - Gunakan input yang bervariasi, termasuk data normal, nilai batas, dan data dengan jumlah elemen berbeda.
   - Bandingkan hasil yang diharapkan (*expected result*) dengan hasil aktual (*actual result*).

3. **Mengidentifikasi Bug**:
   - Temukan kesalahan pada fungsi `hitung_rata_rata()`, `status()`, dan `nilai_tertinggi()`.
   - Catat gejala, lokasi kesalahan, test case yang membuktikan bug, serta akar penyebabnya.
   - Gunakan tracing manual, traceback, atau debugger VS Code untuk membantu proses investigasi.

4. **Memperbaiki Program**:
   - Perbaiki pembagi pada fungsi rata-rata agar menyesuaikan jumlah data.
   - Perbaiki kondisi kelulusan agar nilai 60 dinyatakan lulus.
   - Perbaiki logika pencarian nilai tertinggi agar dapat menemukan nilai terbesar dengan benar.
   - Lakukan perubahan kode seminimal mungkin sesuai akar penyebab bug.

5. **Melakukan Retest**:
   - Jalankan kembali seluruh test case setelah program diperbaiki.
   - Pastikan hasil aktual sesuai dengan hasil yang diharapkan.
   - Pastikan perbaikan tidak menimbulkan kesalahan baru (*regresi*).

6. **Dokumentasi dan Pengumpulan**:
   - Dokumentasikan kasus, test case, bug report, hasil retest, dan refleksi dalam README.
   - Simpan perubahan kode menggunakan Git.
   - Unggah repositori ke GitHub dengan commit yang menunjukkan proses sebelum dan sesudah perbaikan.

---

## Hasil Pengujian (Test Case Wajib)

| ID | Fungsi yang Diuji | Input | Hasil yang Diharapkan | Status |
| :--- | :--- | :--- | :--- | :-: |
| T1 | Rata-rata | `[80, 60, 90, 70]` | `75.0` | PASS |
| T2 | Rata-rata | `[100, 80]` | `90.0` | PASS |
| T3 | Status kelulusan | `60` | `Lulus` | PASS |
| T4 | Status kelulusan | `59` | `Tidak lulus` | PASS |
| T5 | Nilai tertinggi | `[80, 60, 90, 70]` | `90` | PASS |

---

## Bug Report

| Bug ID | Fungsi | Gejala | Akar Penyebab | Perbaikan |
| :--- | :--- | :--- | :--- | :--- |
| B01 | `hitung_rata_rata()` | Hasil rata-rata tidak sesuai jumlah data | Pembagian selalu menggunakan angka 5 | Menggunakan `len(nilai)` sebagai pembagi |
| B02 | `status()` | Nilai 60 dinyatakan tidak lulus | Menggunakan operator `>` | Mengubah operator menjadi `>=` |
| B03 | `nilai_tertinggi()` | Nilai tertinggi tidak ditemukan dengan benar | Kondisi perbandingan terbalik | Mengubah kondisi menjadi `x > tertinggi` |

---

## Cara Menjalankan

Buka terminal pada direktori utama repositori, kemudian jalankan program menggunakan perintah berikut:

```bash
python3 praktik/praktik_4_debugging.py
```

---

## Refleksi
Melalui praktik ini, saya memahami bahwa program yang berhasil dijalankan belum tentu menghasilkan output yang benar. Kesalahan logika dapat terjadi meskipun tidak terdapat syntax error maupun runtime error. Oleh karena itu, proses debugging perlu dilakukan secara sistematis melalui penyusunan test case, tracing, dan pemeriksaan alur eksekusi program.

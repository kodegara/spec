# Spesifikasi Gara

Repositori ini berisi kode yang yang memastikan interpreter Gara bekerja sesuai ekspektasi. Kode-kode tersebut juga dapat menjadi contoh bagi pembaca yang ingin mengetahui seperti apa bahasa pemrograman Gara tersebut.

Repositori ini terdiri atas 2 cabang utama:

- `main`: berisi kode spesifikasi Gara untuk versi Gara yang telah dirilis untuk khalayak umum
- `lokal`: berisi kode spesifikasi untuk versi Gara yang sedang dalam tahap pengembangan

## Konvensi Penulisan

- Gunakan `sidang` dan kelas yang akan disidang
- Gunakan `tentang` dan metode/perilaku yang akan disidang
- Gunakan `saat` untuk menyidang perilaku yang sangat spesifik
- Gunakan `ia` untuk melakukan penyidangan tingkah laku sesuai kondisi
- Fungsi statis dideskripsikan dengan tanda `#`:

  ```gr
  tentang("#dariKata/1", fn () {
      ia("dapat berkata-kata", fn () {
          // ...
      })
  })
  ```

- Fungsi instansi dideskripsikan dengan tanda "."
- Fungsi yang sedang dites perlu dideskripsikan aritasnya, misal: `#baru/1`, `.desimal/1`
- Untuk ekspektasi masalah, gunakan `coba` - `tahan` sebagai berikut:

  ```gr
  tuntut coba {
      sesuatuYangBermasalah()
      salah
  } tahan (e) {
      tuntut e.pesan == "pesan"
  } == benar
  ```
- Tes fungsi diurutkan secara alfabetis

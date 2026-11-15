LAYAR — INTEGRASI YOUTUBE DATA API v3

CARA MENGGUNAKAN
1. Buka Google Cloud Console: https://console.cloud.google.com/
2. Buat/pilih project dan aktifkan YouTube Data API v3.
3. Buat API key.
4. Batasi API key:
   - Application restrictions: Websites / HTTP referrers
   - Tambahkan domain produksi dan domain testing yang digunakan.
   - API restrictions: Restrict key ke YouTube Data API v3.
5. Jalankan website, buka Koleksi > YouTube Movies.
6. Tempel API key ke kolom YouTube API Key lalu tekan Simpan key.

CARA KERJA
- Search API meminta video berdurasi panjang (>20 menit), embeddable, dan berlisensi Creative Commons.
- Detail video diambil melalui videos.list.
- Pemutaran memakai YouTube IFrame Player resmi.
- Tab Internet Archive tetap tersedia seperti versi sebelumnya.

CATATAN PENTING
- YouTube Data API tidak menyediakan file video untuk diunduh/di-host sendiri.
- Filter Creative Commons tidak membuktikan bahwa pengunggah memiliki hak atas seluruh isi film. Periksa kanal, deskripsi, dan bukti hak/lisensi sebelum menampilkan film sebagai resmi atau legal.
- Video yang dihapus, dibatasi wilayah/usia, atau embedding-nya dinonaktifkan bisa gagal diputar.
- API key di frontend dapat dilihat pengunjung. Pembatasan HTTP referrer dan API sangat disarankan. Untuk penggunaan publik yang lebih aman, pindahkan panggilan API ke backend dan jangan pernah menyimpan key privat di repositori.
- Kuota default search.list adalah 100 panggilan per hari. videos.list menggunakan kuota endpoint terpisah.
- Jangan menghapus branding, iklan, atau kontrol standar YouTube Player.

Dokumentasi:
https://developers.google.com/youtube/v3
https://developers.google.com/youtube/iframe_api_reference

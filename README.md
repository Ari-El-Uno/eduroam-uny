# Konfigurasi eduroam UNY
Konfigurasi untuk terhubung dengan jaringan eduroam Universitas Negeri Yogyakarta secara manual via wpa_supplicant.
Contoh implementasinya adalah pada Raspberry Pi, yang tidak mengizinkan untuk secara mudah terhubung ke eduroam via network manager.

## Langkahnya
- Unduh file **wpa_supplicant.conf** atau bisa Anda buat sendiri menggunakan aplikasi editor teks apa saja, pastikan isinya sama dengan yang ada di repository ini, atau boleh ditambah yang lain (misalnya untuk jaringan lain selain eduroam).
- Ganti **username** dengan username Anda, username yang sama yang digunakan pada email UNY milik Anda.
- Ganti **sandi** dengan kata sandi yang Anda gunakan untuk membuka email UNY milik Anda.
- Letakkan file tersebut ke dalam direktori /etc/wpa_supplicant.
- Jalankan perintah `wpa_supplicant -i wlan0 -c /etc/wpa_supplicant/wpa_supplicant.conf` untuk menginisialisasikan konfigurasi ke interface. Nama interface wlan0 bisa saja berbeda, tergantung hardware mana yang akan digunakan untuk terhubung ke eduroam, untuk memastikan bisa cek dengan perintah `iwconfig`.
- Restart daemon dhcpcd atau reboot saja.

### Selamat berselancar menggunakan jaringan eduroam UNY

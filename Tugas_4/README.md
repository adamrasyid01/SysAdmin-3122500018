# TUGAS 4

**DAFTAR ISI**

1. [Bagaimana Internet Bekerja (pribadi)](#bagaimana-internet-bekerja)
2. [DNS Query (pribadi)](#2-dns-query)
3. [BIND9 Kelompok 8](#3-config-bind9)

# Disusun Oleh

| NAMA | NRP |
| ---- | --- |
| [Zahrotul Hidayah](https://github.com/zah1703)| 3122500004 |
| [Leody Zelvon Herliansa](https://github.com/Leodyz)| 3122500010 |
| [Adam Rasyid Nurmuhammad](https://github.com/adamrasyid01)| 3122500018 | 

## 1. Bagaimana Internet bekerja?

***Jawaban dibawah adalah ekosistem internet menurut saya berdasarkan materi dari bapak Ferry Astika***

Jaringan internet bekerja berdasarkan rangkaian protokol komunikasi dan teknologi infrastruktur yang memungkinkan perangkat. Berikut adalah langkah sederhana bagaimana proses tersebut berlangsung:

- Perangkat Anda (seperti komputer): Ketika memasukkan alamat situs web, komputer Anda akan pertama-tama mencari alamat IP dari situs tersebut melalui sistem Domain Name System (DNS).

- Koneksi ke Server: Setelah mendapatkan alamat IP, komputer akan meminta koneksi ke server situs tersebut. Kemudian, permintaan ini dikirim melalui peralatan jaringan lokal Anda. Lalu, ke penyedia layanan internet (ISP) dan selanjutnya ke server tujuan.

- Pertukaran Data: Server akan merespons permintaan Anda dengan cara mengirimkan data halaman web yang Anda inginkan kembali ke komputer.

- Tampilan di Browser: Kemudian, data yang diterima oleh komputer ini akan diinterpretasikan oleh browser dan ditampilkan sebagai halaman web.

## 2. DNS Query

***Bagaimana Cara kerja dari iterative dan recursive dari DNS Query, ada 8 step, dari PC anda! misal akses detik.com***

Berdasarkan referensi [Penjelasan DNS](https://www.hostinger.co.uk/tutorials/what-is-dns)

**Query DNS**
![Gambar Cara kerja DNS](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_4/assets/how-does-dns-work-1024x590.png)

- Langkah 1 : Klien memasukkan www.detik.com ke dalam browser dan menekan Enter. Sebuah DNS query untuk alamat IP (record a) dikirim oleh resolver sistem operasi ke server DNS.

- Langkah 2 : Server DNS menerima query dan mulai mencari melalui tabelnya (cache) untuk mencari alamat IP untuk www.detik.com. Namun, entri tersebut tidak ada dalam tabelnya.

- Langkah 3 : Server DNS akan memberikan respons berupa rujukan ke server root. 

- Langkah 4 : Resolver kemudian akan melakukan query ke server root untuk alamat IP tersebut.

- Langkah 5 : Resolver melakukan query ke server DNS TLD yang diberikan oleh server root untuk mencari informasi lebih lanjut mengenai alamat IP untuk "detik.com".

- Langkah 6 : Server DNS TLD memberikan informasi mengenai server DNS otoritatif yang bertanggung jawab atas domain "detik.com".

- Langkah 7 : Resolver melakukan query ke server DNS otoritatif untuk mendapatkan alamat IP yang diinginkan.

- Langkah 8 : Server DNS otoritatif merespons dengan memberikan alamat IP untuk "detik.com" kepada resolver.


> Perbedaan utama antara iterative DNS dan recursive DNS adalah pada proses pencarian informasi DNS. Iterative DNS meminta klien untuk melakukan query lebih lanjut secara bertahap, sementara recursive DNS melakukan proses query secara menyeluruh untuk klien.

# 3. Config BIND9



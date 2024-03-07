# TUGAS 3

# Disusun Oleh

| NAMA | NRP |
| ---- | --- |
| [Zahrotul Hidayah](https://github.com/zah1703)| 3122500004 |
| [Leody Zelvon Herliansa](https://github.com/Leodyz)| 3122500012 |
| [Adam Rasyid Nurmuhammad](https://github.com/adamrasyid01)| 3122500018 | 

## LINUX APT COMMAND

### UNTUK USER

| Command           | Description     |
|-----------        |-----------|
|apt show foo       |Menampilkan informasi paket foo      |
|apt search foo     | Mencari paket bernama/berkaitan foo         |
|apt-cache policy foo| Menampilkan versi tersedia paket foo       |


### Command apt untuk Administrator

> **Gunakan** sudo untuk menjalankan perintah berikut (root)

| Command           | Description     |
|-----------        |-----------|
|apt update      |Update repository metadata (list versi dll)     |
|apt install foo   | Memasang paket foo dan yang terkait        |
|apt upgrade| Menghapus versi lama paket      |
|apt full-upgrade| Mengupdate/hapus paket yang beneran terbaru     |
|apt remove foo| Menghapus paket foo, tidak confignya    |

## Cara menggunakan APT command
> Mengubah Repository Apt (pastikan gunakan sudo)

![Update Dependencies](/assets/apt_sourceslist.png)

> Setelah melakukan update dan upgrade untuk depedency, kita bisa install aplikasi menggunakan Aplikasi Software Bawaan

![Software Terinstall](/assets/software_terinstall.png)

### Melihat Storage yang terpakai di linux menggukan Terminal

![Free Storage](/assets/3_disk_free.png)

### Membuat daftar Directory, diurutkan dari yang terbesar yang terkecil

> Melihat isi direktori dengan perintah du dan sort (satuan megabyte):

![Sorting Directory](/assets/4_du_sort.png)

### Perintah ncdu (NCurses Disk Usage)

    Fungsi perintah ncdu untuk memberikan tampilan interaktif dari penggunaan disk pada suatu direktori atau file di sistem file.

Install terlebih dahulu ncdu dengan menggunakan perintah

> apt update && apt install ncdu

![Install Package ncdu](/assets/5_install_ncdu.png)

Akses ncdu dengan command $ ncdu
![Tampilan ncdu](/assets/6_UI_ncdu.png)

### Perintah baobab
Digunakan untuk menganalisa ruang pada disk dengan tampilan grafis 
Ketikkan perintah $ baobab
![Tampilan baobab](/assets/7_tampilan_baobab.png)

### Membersihkan Package

**Apt/aptitude/dpkg**

Manajer paket debian biasa. Ketika  menginstal sebuah paket, sumber arsip/debnya disimpan di sistem (di folder/var/cache/apt/) untuk mengaktifkan kemungkinan instalasi ulang tanpa koneksi internet 

Untuk membersihkan "apt cache" gunakan perintah apt clean.

Setelah cache dari paket yang diinstal dibersihkan, Kita juga dapat menghapus paket yang tidak berguna dari sistem, serta file konfigurasi. Namun Ingatlah untuk memeriksa dengan cermat daftar paket yang direncanakan untuk dihapus, sebelum menerima operasi:

![Apt remove](/assets/8_apt_remove.png)

Jika sistem telah diupgrade ke versi terbaru, ada kemungkinan beberapa paket tidak lagi tersedia di repositori baru (paket tersebut sudah usang). Untuk membuat daftar dan menghapus paket-paket ini, gunakan apt dan periksa dengan cermat daftar paket yang direncanakan untuk dihapus:
![Apt remove obsolete](/assets/9_apt_remove_obsolete.png)

Terakhir, untuk membuat daftar dan membersihkan file konfigurasi yang tetap ada meskipun aplikasi telah dihapus, gunakan perintah berikut :
![Dpkg list](/assets/10_dpkg_awk_rc.png)

**deborphan**

Mencantumkan paket-paket yang diadopsi pada sistem : paket-paket yang tidak bergantung pada paket lain.

Ingatlah untuk memeriksa dengan cermat daftar paket yang direncanakan untuk dihapus, sebelum menjalankan operasi.
![Install deborphan](/assets/11_install_deborphan.png)

![Autoremove deborphan](/assets/12_autoremove_deborphan.png)

### Mengosongkan trash-bin

Tiga trash-bin (wastebasket) yang berbeda harus dipertimbangkan:

**trash-bin user**

Anda dapat mengosongkannya dengan system file manager atau dengan perintah :
![rm -Rf](/assets/13_rm_Rf.png)

**trash-bin admin**

Untuk mengosongkannya dengan cara yang benar, gunakan terminal dalam mode administrator:
![rm -Rf cache](/assets/14_rm_rf_cache.png)

**trash-bin eksternal**

biasanya diberi nama '/media/(loginname)/your_disk/.Trash_1000'.
img
![rm -Rf thumbnails](/assets/15_rm_rf_thumbnails.png)

# Menginstall Package EXTERNAL Extensi .deb

### DEBI Application

Kita dapat menginstall package External (.deb) menggunakan aplikasi Gdebi yang dapat diinstall dengan cara berikut.
![apt update apt gdebi](/assets/16_apt_install_apt_gdebi.png)

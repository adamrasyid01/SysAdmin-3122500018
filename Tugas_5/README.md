# TUGAS 5

# Disusun Oleh

| NAMA | NRP |
| ---- | --- |
| [Adam Rasyid Nurmuhammad](https://github.com/adamrasyid01)| 3122500018 | 

**DAFTAR ISI**

1. [NTP Client](#install-ntp-client)
2. [Webserver Apache 2.0](#apache-20)
3. [PHP 8.2 dan PHP-FM](#php-82-dan-php-fm)
4. [MariaDB](#mariadb)
5. [Email System](#email-system)
    - POSTFIX
    - DOVECOT
6. [RoundCube]()


## Install NTP Client

**1. Lakukan instalasi paket layanan sinkronisasi waktu**
![NTP Client](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/1.Installasi%20NTP%20Client.png)

**2. Pastikan konfigurasi timezone ke Asia/Jakarta**
![Timezone Jakarta](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/2.Set%20ke%20Jakarta.png)

**3. Melakukan konfigurasi Real Time Clock (RTC) untuk merefer ke UTC (Coordinated Universal Time)**
![RTC refer ke UTC](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/3.RTC%20ke%20UTC%20.png)

**4. Mengaktifkan NTP Client untuk sinkronisasi waktu**
![Sinkronisasi Waktu](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/4.Aktifkan%20NTP%20Client%20utk%20Sinkronisasi%20Waktu.png)

**5. Menyunting file timesyncd.conf untuk mengarah ke NTP server terdekat untuk mendapatkan waktu 
delay terpendek. Biasanya setiap organisasi atau negara mempunyai NTP Server sendiri**
![Sambungkan ke NTP server terdekat](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/5.arahkan%20ke%20NTP%20Server%20terdekat.png)

**6. Restart layanan sinkronisasi waktu dan pastikan layanan berjalan dengan benar**
![Restart dan Cek Status](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/6.Restart%20dan%20cek%20Status%20timesyncd.png)

**7. Lakukan pengecekan kesesuaian tanggal system dengan perintah**
![Restart dan Cek Status](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/7.Hasil%20timedatectl.png)

## APACHE 2.0

**1. Install Apache2**
![Restart dan Cek Status](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/8.apt_install_apache.png)

**2. Mengkonfigurasi Apache2**

- Line 12 Change
![Line 12](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/9.line12%20prod.png)

- Add file name that it can access only with directory's name
![Hanya bisa diakses](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/10.hanya%20bisa%20diakses%20directory%20name.png)

- Line 70 : add to specify server name
![Server Name www.kelompok8.com](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/11.specify%20server%20name.png)

-  Line 11 : change to webmaster's email
![Server Admin](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/12.webmaster_email.png)

- root@www:~# systemctl reload apache2
![Reload Apache2](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/13.Lakukan%20reload.png)

**3. Testing di Web Browser**
![Web Browser](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/14.lakukan%20test%20ke%20web%20browser.png)

## PHP 8.2 dan PHP-FM

**1. Install PHP 8.2**
![PHP 8.2](asyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/15.apt_php8.2.png)

**2. Cek versi PHP**
![php-v](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/16.php-v.png)

**3. Verify installation to create a test script**
![Verify](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/17.verify%20installation%20to%20create%20test%20script.png)

**4. Install PHP-FM**
![PHP-FM](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/18.install%20PHP-FM.png)

**5. Buka file /etc/apache2/sites-available/default-ssl.conf, add into <VirtualHost> - </VirtualHost>**
![PHP-FM](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/19.default-ssl.conf.png)

**6. Considering dependency proxy for proxy_fcgi:**
![Proxy fcgi](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/20.proxy_fcgi%20setenvif.png)

**7. Jalankan a2enconf php8.2-fpm**
![Enable conf](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/21.php8.2-fpm.png)

**8. Restart PHPFM dan APACHE 2**
![Restart PHPFM dan APACHE](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/22.restart%20phpfm%20dan%20apache2.png)

**9. Melakukan test validasi terhadap PHP-FM dengan membuat file info.php di root document**
![Validasi](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/23.validasi%20PHP-FM%20.png)

**10. Tes di browser**
![Tes Browser](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/24.test%20di%20browser.png)

## MARIADB

**1. Lakukan nstalasi Maria DB 10.11**
![Install MariaDB](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/25.mariadb%2010.11.png)

- Line 95 : confirm default charset di file /etc/mysql/mariadb.conf.d/50-server.cnf
![Confirm Default Charset](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/26.%20confirm%20default%20charset.png)

- Lakukan Restart
![Restart](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/27.%20restart%20mariadb.png)

**2. Inisial Konfigurasi dan testing database MariaDB Server**
![Bagian Satu](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/28.1.mysqlinstallation_bagiansatu.png)
![Bagian Kedua](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/28.2.mysqlinstallation_bagiandua.png)
![Bagian Ketiga](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/28.3%20mysqlinstallation_bagiantiga.png)

**3.  Connect to MariaDB**
![Konek MariaDB](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/29.mysql.png)

**4. Authentication is enabled by default**
![Show Grants](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/30.grants%20localhost.png)

**5. Show user list**
![Show User List](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/31.%20show%20user%20list.png)

**6. Show Databases List**
![Show DB List](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/32.show%20databases%20list.png)

**6. Create test database,table dan insert data**
![test,table,insert](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/33.create%20database%2Ctable%2C%20dan%20insert%20data.png)

**7. Show test table**
![Show Test Table](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/34.show%20test%20tables.png)

**8. Delete Test Database**
![Show Test DB](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/35.delete%20test%20database.png)

## EMAIL SYSTEM

- POSTFIX

    **1. Apt -y install postfix sasl2-bin**
    ![Install PostfFix](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/36.postfix%20sasl2-bin.png)

    **2. Cp /usr/share/postfix/main.cf.dist /etc/postfix/main.cf**
    ![main.cf]( https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/37.main.cf.png)

    - Modifikasi Line 82 dan 98**
    ![82 dan 98](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/38.%2082%20dan%2098.png)

    - Line 106 : uncomment and specify domainname
    ![106](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/39.%20Line106.png)

    - Line 127 & 141 uncomment
    ![127 dan 141](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/40.%20Line%20127%20dan%20141.png)

    - Line 189 uncomment
    ![189](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/41.%20Line%20189.png)

    - Line 232 Uncomment
    ![232](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/42.Line%20232.png)

    - Line 277 uncomment & 294 add local network
    ![277 dan 294](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/43.Line%20277%20dan%20294.png)

    - Line 416 & 427 uncomment
    ![416 dan 427](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/44.Line%20416%20dan%20427.png)

    - Line 449 uncomment
    ![449](  https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/45.%20Line%20449.png)

    - Line 585 comment out and add
    ![585](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/46.%20Line%20585.png)

    - Line 659,664,669,675 add
    ![659+](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/47.%20Line%20659%2C664%2C669%2C675.png)

    - Line 679,683,688,692 comment out
    ![679,683,688,692]( https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/48.%20Line%20679%2C683%2C688%2C692.png)

    - Add Follows to the end
    ![Add the end](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/49.%20Add%20Follows%20to%20the%20end.png)

    - Newaliases dan restart postfix
    ![Restart Postfix]( https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/50.%20newaliases.%20restart%20postfix.png)

    **3. Menambahkan konfigurasi anti spam**
    ![AntiSpam]( https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/51.%20konfigurasi%20anti%20spam.png)

    **4. Restart kembali postfix**
    ![Postfix Restart](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/52.%20restart%20postfix.png)

- DOVECOT
    
    **1. Lakukan instalasi Dovecot Server**
    ![Dovecot]( https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/53.Instalasi%20Dovecot%20Server.png)

    **2. Buka file /etc/dovecot/dovecot.conf**

    - Lakukan Uncomment di Line 30
    ![Line 30](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/54.%20uncomment%20line%2030.png)

    **3. Buka file konfigurasi /etc/dovecot/conf.d/10-auth.conf**

    - Lakukan uncomment dan change di line 10

    ![Line 10](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/55.%20line%2010.png)

    - Add di Line 100

    ![Line 100](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/56.%20line%20100.png)

    - Line 30 change to Maildir

    ![Line 30](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/57.%20line%2030%20change%20to%20Maildir.png)

    - Line 107-109 uncomment and add

    ![Line 107-109](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/58.master.conf.png)
 
   - Lakukan restart dovecot
   
    ![Restart Dovecot](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/59.%20restart%20dovecot.png)

    - Melakukan Cek terhadap Layanan Posfix
    ![Check layanan Postfix]( https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/61.Telnet%20mail.png)


## FINAL CHECK untuk semua SERVICES 
![Check Semua Services](https://github.com/adamrasyid01/SysAdmin-3122500018/blob/main/Tugas_5/assets/60.%20netstat%20-a%20LISTEN.png)



  
  





   





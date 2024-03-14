# modul_switching

![1](https://github.com/zakiramadan/modul_switching/assets/126186033/f312582b-9670-44fb-a07a-b8f7b02f321b)

1. show ip vlan pada Switch
Perintah ini tidak secara eksplisit ada dalam perangkat Cisco IOS; yang lebih umum adalah show vlan atau show vlan brief untuk switch yang menggunakan Cisco IOS. Perintah ini menampilkan informasi tentang VLAN yang dikonfigurasi pada switch, termasuk ID VLAN, nama VLAN, dan port apa saja yang termasuk dalam VLAN tertentu. Ini membantu dalam memverifikasi pembagian jaringan logis dan isolasi di dalam jaringan.

![sh vlan](https://github.com/zakiramadan/modul_switching/assets/126186033/c805c7cb-196e-4902-8ce6-8cac1950ba67)

2. show running-config pada SWITCH, ROUTER_1
Pada Switch: Perintah show running-config menampilkan konfigurasi aktif (yang sedang berjalan) pada switch. Ini mencakup semua pengaturan dan konfigurasi yang telah diterapkan, termasuk konfigurasi VLAN, pengaturan port, konfigurasi trunk, dan lain-lain.
Pada ROUTER_1: Perintah yang sama pada router akan menampilkan konfigurasi aktif dari router tersebut, termasuk antarmuka jaringan, rute statis atau dinamis, pengaturan protokol routing, konfigurasi NAT, DHCP, ACLs, dan lainnya.

![sh running-config](https://github.com/zakiramadan/modul_switching/assets/126186033/7cd9043e-8bab-4902-9f20-7575ede1b218)

3. show dhcp pool
Perintah ini digunakan pada router yang dikonfigurasi sebagai server DHCP. Ini menampilkan detail tentang pool DHCP yang telah dikonfigurasi, termasuk range alamat IP yang tersedia untuk disewakan, mask subnet, default gateway, DNS server, lease time, dan lainnya. Ini membantu dalam memahami dan memverifikasi konfigurasi DHCP di jaringan.

![sh ip dhcp pool](https://github.com/zakiramadan/modul_switching/assets/126186033/28bdb423-0c5c-40a1-94e2-2d10165f03f8)

4. show ip nat statistics
Perintah ini menampilkan statistik dari Network Address Translation (NAT) pada router, termasuk jumlah translasi aktif, jumlah hitungan untuk translasi NAT, dan sumber daya yang digunakan. Ini penting untuk memahami seberapa efektif NAT bekerja dan mendiagnosis masalah koneksi.

![show ip nat statistics](https://github.com/zakiramadan/modul_switching/assets/126186033/ec021d38-863f-4b81-af26-eb83c211e667)

![sh ip nat statistics](https://github.com/zakiramadan/modul_switching/assets/126186033/4ad1d36f-5e85-47c7-8d05-5d765d5ddd11)

5. Pengiriman Packet Data
Untuk mengirimkan paket data dari sumber ke tujuan pada masing-masing PC yang terhubung dalam VLAN yang sama atau berbeda, prosesnya melibatkan beberapa langkah:

Dalam VLAN yang Sama: Komunikasi terjadi secara langsung melalui switch, asalkan kedua PC terhubung ke port yang berada dalam VLAN yang sama. Switch hanya akan meneruskan paket pada VLAN tersebut.
Antar VLAN: Membutuhkan router atau switch layer 3 untuk melakukan routing antar VLAN (InterVLAN routing). Paket dari sumber akan dikirim ke gateway (router atau switch L3), yang kemudian akan meneruskannya ke VLAN tujuan.
Konfigurasi NAT: Jika tujuannya berada di luar jaringan lokal (misalnya, Internet), router akan melakukan NAT pada paket tersebut, mengganti alamat IP sumber internal dengan alamat IP publik router sebelum mengirimkannya ke jaringan eksternal.
Untuk setiap skenario, perangkat di jaringan harus dikonfigurasi dengan benar, termasuk VLAN, routing, dan NAT, agar komunikasi data berjalan sesuai dengan harapan.

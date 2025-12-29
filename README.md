# SIMULASI-SERANGAN-DoS-pada-DvWA-dengan-Hping3


Repositori ini berisi konfigurasi dan dokumentasi praktikum simulasi serangan DoS pada web aplikasi DVWA yang berjalan di atas web server Apache menggunakan Kali Linux sebagai mesin penyerang.

## Tujuan

- Mempelajari konsep dasar serangan DoS pada layer jaringan dan aplikasi.  
- Menggunakan tool hping3 untuk melakukan serangan SYN Flood.  
- Menggunakan tool Slowloris untuk melakukan serangan HTTP DoS.  
- Melihat dampak serangan terhadap resource server (CPU, RAM, dan koneksi).  
- Menguji langkah mitigasi sederhana menggunakan firewall (iptables) atau konfigurasi server.

## Lingkungan Uji

- Sistem operasi attacker: Kali Linux  
- Sistem operasi target: (mis. Ubuntu Server / Kali / lainnya)  
- Web server: Apache2  
- Aplikasi web: DVWA (Damn Vulnerable Web Application)  
- Jaringan: VirtualBox / VMware (mode host-only / internal network)


## Tool yang Digunakan

- `hping3` untuk serangan SYN Flood pada port HTTP.  
- `slowloris` / script `slowloris.py` untuk serangan HTTP DoS.  
- `htop` untuk memonitor penggunaan CPU dan RAM.  
- `ss` atau `netstat` untuk melihat jumlah koneksi ke port 80.  

## Langkah Singkat Pengujian

1. Pastikan DVWA dan Apache sudah berjalan di mesin target.  
2. Catat alamat IP target (mis. `10.0.2.15`).  
3. Jalankan serangan SYN Flood dengan hping3 dari mesin attacker.  
4. Jalankan serangan Slowloris dari mesin attacker.  
5. Pantau resource server dengan `htop` dan jumlah koneksi dengan `ss`/`netstat`.  
6. Terapkan aturan firewall atau konfigurasi lain sebagai mitigasi, lalu ulangi pengujian.

## Struktur Direktori

Contoh struktur :

- `laporan/` : Berisi laporan PDF/DOCX praktikum.  
- `script/` : Berisi script bash.  
- `screenshot/` : Berisi tangkapan layar hasil serangan dan monitoring.  

## Catatan Etika

Seluruh pengujian pada repositori ini hanya ditujukan untuk **pembelajaran dan penelitian di lingkungan lab tertutup**. 

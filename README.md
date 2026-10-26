# Aplikasi Perpustakaan Sederhana dengan Spring Boot

## Fitur
- Melihat daftar buku dan mencari buku berdasarkan judul.
- Menambahkan buku dengan validasi ID agar tidak duplikat dan stok tidak negatif.
- Melihat daftar anggota.
- Menambahkan anggota dengan validasi ID dan email agar tidak duplikat.

## Teknologi
- Java 17
- Spring Boot 3.3.5
- Spring MVC untuk route web
- Thymeleaf untuk halaman HTML
- Spring Data JPA untuk akses database
- H2 untuk database latihan

## Menjalankan di Windows
1. Pastikan JDK 17 atau lebih baru terpasang. Periksa melalui PowerShell: `java -version`.
2. Buka folder proyek di VS Code atau terminal.
3. Jalankan `.\mvnw.cmd spring-boot:run` jika Maven Wrapper tersedia. Jika tidak tersedia, instal Maven lalu jalankan `mvn spring-boot:run`.
4. Buka `http://localhost:8080/buku` untuk buku atau `http://localhost:8080/anggota` untuk anggota.

Database saat ini menggunakan H2 in-memory. Data contoh dari `data.sql` dimuat saat aplikasi mulai, dan perubahan data akan hilang saat aplikasi dimatikan.

## Struktur utama
- `entity`: bentuk data/tabel database.
- `repository`: operasi database.
- `service`: logika dan validasi bisnis.
- `controller`: mengatur URL dan menerima input form.
- `templates`: halaman HTML Thymeleaf.
- `application.properties`: konfigurasi aplikasi dan database.

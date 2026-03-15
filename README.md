Praktikum Sistem Embedded 2: External Interrupt with Button
Repositori ini berisi kode sumber dan dokumentasi untuk praktikum sistem embedded yang berfokus pada implementasi External Interrupt menggunakan tombol (push button) pada dua platform mikrokontroler: ESP32 dan STM32 (Bluepill/F103C8T6).

Deskripsi Proyek
Proyek ini mendemonstrasikan cara menangani input dari perangkat eksternal secara asynchronous menggunakan fitur Interrupt. Berbeda dengan metode polling yang memeriksa status pin secara terus-menerus di dalam loop utama, Interrupt memungkinkan prosesor untuk langsung merespons perubahan sinyal pada pin tertentu secara instan.

Fitur Utama
Implementasi Interrupt pada ESP32 menggunakan framework Arduino.

Implementasi Interrupt pada STM32 menggunakan Arduino Core/STM32Cube.

Konfigurasi mode Pull-Up dan Pull-Down (Internal dan Eksternal).

Penanganan software debouncing untuk memastikan kestabilan pembacaan tombol.

Komponen yang Digunakan
Mikrokontroler: ESP32 DevKit V1 / STM32F103C8T6 (Bluepill).

Input: Push Button.

Output: On-board LED atau External LED.

Kabel: Jumper wires.

Breadboard.

Skema Rangkaian
1. ESP32
Button: Terhubung ke GPIO 4 (Konfigurasi Internal Pull-Up).

LED: Terhubung ke GPIO 2 (Built-in LED).

2. STM32 Bluepill
Button: Terhubung ke Pin PA0 (Konfigurasi EXTI0).

LED: Terhubung ke Pin PC13 (Built-in LED).

Cara Penggunaan
Clone Repositori:
git clone [https://github.com/annabil-dev/PRAKTIKUM-SISTEM-EMBEDDED-2.git](https://github.com/annabil-dev/PRAKTIKUM-SISTEM-EMBEDDED-2.git)

Persiapan Environment:
Pastikan board library untuk ESP32 dan STM32 sudah terpasang pada Arduino IDE atau PlatformIO.

Upload Kode:
Buka file pada folder masing-masing board dan lakukan proses Compile serta Upload.

Monitoring:
Gunakan Serial Monitor dengan baud rate 115200 untuk melihat log pemicuan interrupt.

Konsep Dasar: Polling vs Interrupt
Polling: CPU memeriksa status pin secara berulang dalam setiap siklus loop. Metode ini tidak efisien jika loop memiliki banyak proses berat.

Interrupt: CPU akan menghentikan sementara tugas utama hanya saat ada sinyal masuk (trigger) pada pin interrupt, menjalankan ISR (Interrupt Service Routine), lalu kembali ke tugas utama.

Struktur Repositori
ESP32_Interrupt/ : Folder berisi file .ino untuk board ESP32.

STM32_Interrupt/ : Folder berisi file .ino untuk board STM32.

Documentation/ : Folder berisi skema rangkaian dan data pendukung.

README.md : Dokumentasi utama proyek.

Kontributor
Annabil Hisyam Muyassar
40040324630066 TRO 24

# Project-Magang-UASC
Project Divisi Low Voltage

Percobaan Pertama:
Komponen Percobaan Pertama:
ESP32
Buzzer
LED
Resistor 220 Ohm (untuk LED)
Sensor DHT22
Cara Menyambungkan Rangkaian:
Sambungkan pin VCC dari DHT22 ke 3.3V pada ESP32.
Sambungkan pin GND dari DHT22 ke GND pada ESP32.
Sambungkan pin Data dari DHT22 ke pin GPIO (misalnya GPIO 4) pada ESP32.
Sambungkan satu kaki LED ke resistor 220 Ohm, lalu sambungkan resistor ke  18 pada ESP32.
Sambungkan kaki lainnya LED ke GND.
Sambungkan pin positif buzzer ke GPIO 19 pada ESP32.
Sambungkan pin negatif buzzer ke GND.
Note:
Untuk program terdapat pada file schematic.
Penjelasan Program:
Penjelasan Kode: Library dan Pin Setup: Pertama, kita mengimpor library yang diperlukan dan mendefinisikan pin yang digunakan. Setup: Menginisialisasi sensor DHT22, LED, dan buzzer. Loop: Membaca suhu dan kelembapan dari sensor DHT22 setiap 2 detik. Jika suhu di bawah 25°C atau di atas 30°C, atau kelembapan di bawah 70% atau di atas 90%, maka LED dan buzzer akan menyala. Jika tidak, LED dan buzzer akan mati. Kode ini akan memastikan bahwa LED dan buzzer aktif sesuai dengan kondisi suhu dan kelembapan yang ditentukan.

Percobaan Kedua:
Komponen Percobaan Kedua:
ESP32
Sensor HC-SR04
Layar OLED (misalnya, SSD1306)
Rangkaian:
Sambungkan pin VCC dari HC-SR04 ke 5V pada ESP32.
Sambungkan pin GND dari HC-SR04 ke GND pada ESP32.
Sambungkan pin Trig dari HC-SR04 ke GPIO  5 pada ESP32.
Sambungkan pin Echo dari HC-SR04 ke GPIO 18 pada ESP32.
Sambungkan pin VCC dari OLED ke 3.3V pada ESP32.
Sambungkan pin GND dari OLED ke GND pada ESP32.
Sambungkan pin SDA dari OLED ke GPIO 21 pada ESP32.
Sambungkan pin SCL dari OLED ke GPIO 22 pada ESP32.\
Note:
Untuk program terdapat pada file schematic.
Penjelasan Program:
Penjelasan Kode: Library dan Pin Setup: Mengimpor library yang diperlukan untuk mengontrol layar OLED dan sensor HC-SR04. Setup: Menginisialisasi serial komunikasi, pin untuk sensor HC-SR04, dan layar OLED. Loop: Mengirimkan sinyal ultrasonik, menghitung durasi pantulan sinyal, menghitung jarak berdasarkan durasi tersebut, dan menampilkan hasilnya pada layar OLED serta serial monitor.

Percobaan Ketiga:
Komponen Percobaan Ketiga:
ESP32
LED RGB
Resistor 220 ohm
Rabgkaian:
Koneksi Komponen:
Hubungkan pin merah, hijau, dan biru dari LED RGB ke pin GPIO ESP32.
Hubungkan pin GND dari LED ke GND ESP32.
Berikut adalah contoh konfigurasi pin:
Red: GPIO 14
Green: GPIO 12
Blue: GPIO 27
Note:
Untuk Program terdapat pada file schematic.
Penjelasan Program:
Program ini mengontrol LED RGB menggunakan server web yang dijalankan di ESP32. Untuk menghubungkan ESP32 ke jaringan WiFi, digunakan library WiFi dan WebServer. Program dimulai dengan mengimpor kedua library tersebut dan menginisialisasi server web pada port 80. Pin GPIO ESP32 yang digunakan untuk mengendalikan masing-masing warna LED RGB adalah pin 14 untuk merah, pin 12 untuk hijau, dan pin 27 untuk biru. Fungsi `setColor` menerima nilai intensitas untuk warna merah, hijau, dan biru, kemudian mengaplikasikan nilai tersebut ke pin yang sesuai menggunakan `analogWrite`.

Halaman HTML utama disimpan dalam variabel `htmlPage`, yang berisi form untuk mengatur nilai warna merah, hijau, dan biru. Fungsi `handleRoot` mengirimkan halaman HTML ini ke klien saat root URL ("/") diakses. Fungsi `handleSetColor` mengambil nilai warna yang dikirimkan dari form, mengonversinya menjadi integer, dan memanggil `setColor` untuk mengatur warna LED. Setelah itu, server merespons dengan pesan konfirmasi yang menampilkan nilai warna yang diatur. 

Pada fungsi `setup`, komunikasi serial diinisialisasi dan ESP32 terhubung ke jaringan WiFi "Wokwi-GUEST". Setelah terhubung, alamat IP ditampilkan di serial monitor. Pin GPIO untuk LED RGB diatur sebagai output, dan rute handler untuk permintaan root serta pengaturan warna ditetapkan. Server web kemudian dimulai. Fungsi `loop` berjalan terus-menerus untuk menangani permintaan klien yang masuk ke server web. Dengan program ini, pengguna dapat mengontrol warna LED RGB melalui halaman web yang diakses melalui alamat IP ESP32 di jaringan WiFi "Wokwi-GUEST".



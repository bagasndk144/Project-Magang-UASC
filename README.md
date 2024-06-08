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
Komponen Percobaan Ketiga


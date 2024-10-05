# Kelompok 4 (P1) - Node RED

# Anggota Tim
| Nama                                      | NIM          |
|-------------------------------------------|--------------|
| [I Gusti Ngurah Sucahya Satria Adi Pratama](https://github.com/ngurahsucahya)| G6401221031  |
|                        |   |
|                          |  |

# Sekilas Tentang
<details>
</details>

# Instalasi
<details>

### Alat dan Spesifikasi
1. Raspberry Pi 4 Model B
2. Rangkaian RFID menggunakan ESP32 Board seperti pada gambar di bawah</br>
![rangkaian.png](rangkaian.png)
3. Ubuntu 24
4. Raspberry OS 

### Menghubungkan PC dengan Raspberry (SSH)
```
ssh -X sucahya@192.168.1.102
```
![ssh.png](images/ssh.png)</br>

### Menginstal Node.js
Node RED berjalan di atas Node.js. Maka dari itu kita harus menginstal Node.js terlebih dulu
```
sudo apt update
sudo apt install nodejs
node -v
sudo apt install npm
```
![nodejs1.png](images/nodejs1.png)</br>
![nodejs2.png](images/nodejs2.png)</br>
![nodejs3.png](images/nodejs3.png)</br>

### Menginstal Mosquitto (MQTT Broker)
```
sudo apt update
sudo apt install -y mosquitto
sudo systemctl status mosquitto
sudo apt install -y mosquitto-clients
```
Jika ingin menjalankan atau menutup broker jalankan perintah berikut
```
sudo systemctl start mosquitto
sudo systemctl stop mosquitto
```
![mosquitto1.png](images/mosquitto1.png)</br>
![mosquitto2.png](images/mosquitto2.png)</br>

### Menginstall Node RED
```
sudo npm install -g --unsafe-perm node-red
```
![nodered1.png](images/nodered1.png)</br>

### Setup MQTT ESP32
</details>

# Konfigurasi
<details>

Kita akan menjadikan Raspberry Pi 4 sebagai server. Jadi kita perlu mendaftar dan menginstall localtonet.
### Melakukan registrasi pada localtonet.com
1. Kunjugi website localtonet.com dan isi email untuk registrasi. </br>
![regislocaltonet1.png](images/regislocaltonet1.png)</br>
2. Setelah itu copy authtoken yang diberikan secara otomatis</br>
![regislocaltonet2.png](images/regislocaltonet2.png)</br>
3. Buat server dengan menulis alamat localhost tempat kita menyimpan Node RED (127.0.0.1:1800).
4. Setelah itu jalankan servernya dengan klik tombol start.</br>
![regislocaltonet3.png](images/regislocaltonet3.png)</br>
### Menginstal localtonet 
Localtonet berjalan di berbagai maam arsitektur. Raspberry Pi 4 yang saya pakai berjalan dengan arsitektur aarch64 sehingga saya unduh versi yang sesuai.
```
wget https://localtonet.com/download/localtonet-linux-arm.zip
unzip localtonet-linux-arm.zip
chmod 777 ./localtonet
./localtonet authtoken PASTE_HERE_COPIED_AUTHTOKEN 
```
Sehingga muncul tampilan seperti ini</br>
![localtonet1.png](images/localtonet1.png)</br>
Jangan lupa jalankan Node RED.</br>
Sekarang server sudah berjalan melalui Raspberry Pi 4. Server akan tetap hidup selama Raspberry Pi 4 juga menyala. 
</details>
</br>

# Maintenance
<details>
</details>

# Cara Pemakaian
<details>

### Membuka Node RED pertama kali
Memulai Node RED dengan mengetik command di bawah
```
node-red
chromium-browser
```
![nodered2.png](images/nodered2.png)</br>

Setelah server Node RED berjalan dan browser terbuka, maka tulis http://127.0.0.1:1880/ pada laman pencarian. Nanti akan muncul tampilan seperti di bawah ini

![nodered3.png](images/nodered3.png)</br>
![nodered4.png](images/nodered4.png)</br>

### Pengenalan fitur
1. Node
2. Flow </br>
   - Tab
   - Group
   - Label
3. Configuration
4. Debug
5. Plug-in

### Memulai projek

</details>

# Pembahasan
<details>
</details>

# Referensi
<details>
</details>
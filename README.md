# Kelompok 4 (P1) - Node RED

# Anggota Tim
| Nama                                      | NIM          |
|-------------------------------------------|--------------|
| [I Gusti Ngurah Sucahya Satria Adi Pratama](https://github.com/ngurahsucahya)| G6401221031  |
|                        |   |
|                          |  |


# Instalasi
### Alat dan Spesifikasi
1. Raspberry Pi 4 Model B
2. Rangkaian RFID seperti pada gambar di bawah</br>
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

# Cara Pemakaian
Memulai Node RED dengan mengetik command di bawah
```
node-red
chromium-browser
```
![nodered2.png](images/nodered2.png)</br>

Setelah server Node RED berjalan dan browser terbuka, maka tulis http://127.0.0.1:1880/ pada laman pencarian. Nanti akan muncul tampilan seperti di bawah ini

![nodered3.png](images/nodered3.png)</br>
![nodered4.png](images/nodered4.png)</br>
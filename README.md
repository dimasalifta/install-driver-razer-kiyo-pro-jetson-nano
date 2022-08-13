# Tutorial install driver kiyo pro linux
Ikuti tahap 1,2 dan 3 secara berurut
## 1.Pertama kita harus menambahkan ppa repository razer
```
sudo add-apt-repository ppa:openrazer/stable
sudo apt-get update
```

## 2. Lalu install driver kamera razer
```
sudo apt-get upgrade -y
sudo apt autoremove -y
sudo apt install openrazer-meta -y
sudo gpasswd -a $USER plugdev
```

## 3. terakhir cek apakah kamera razer kiyo pro sudah terbaca dengan menggunakan v4l2 utils
```
sudo apt install v4l-utils -y
v4l2-ctl --list-devices
```

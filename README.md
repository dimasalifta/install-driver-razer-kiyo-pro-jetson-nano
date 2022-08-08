# Tutorial install driver kiyo pro linux
Ikuti tahap 1,2 dan 3
apabila ada error di tahap 1 maka lakukan tahap 1a
## 1.Pertama kita harus menambahkan ppa repository razer
```
sudo add-apt-repository ppa:openrazer/stable
sudo apt-get update
sudo apt-get upgrade
```
## 1a. apabila terjadi error ikuti panduan dibawah ini
#### Apparently it is related to the information that dpkg saves and it conflicts in the installation
So wee needed move /var/lib/info/ and create new /var/lib/dpkg/info
```
sudo mv /var/lib/dpkg/info/ /var/lib/dpkg/backup/
sudo mkdir /var/lib/dpkg/info/
```
#### Next update repos and force install .
```
sudo apt-get update
sudo apt-get -f install
```
#### Move the new structure dpkg/info to old info
```
sudo mv /var/lib/dpkg/info/* /var/lib/dpkg/backup/
```
#### Remove the new dpkg structure folder and back the old
```
sudo rm -rf /var/lib/dpkg/info
sudo mv /var/lib/dpkg/backup/ /var/lib/dpkg/info/
```
#### If this is not done, it will complain in the script and its installation will always fail

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

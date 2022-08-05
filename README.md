# Tutorial install driver kiyo pro linux

'sudo add-apt-repository ppa:openrazer/stable'
'sudo apt-get update'
'sudo apt-get upgrade'

'sudo mv /var/lib/dpkg/info/ /var/lib/dpkg/backup/'
'sudo mkdir /var/lib/dpkg/info/'
'sudo apt-get update'
'sudo apt-get -f install'
'sudo rm -rf /var/lib/dpkg/info'
'sudo mv /var/lib/dpkg/backup/ /var/lib/dpkg/info/'


'sudo apt-get upgrade -y'
'sudo apt autoremove -y'
'sudo apt install openrazer-meta -y'
'sudo gpasswd -a $USER plugdev'

'sudo apt install v4l-utils -y'
'v4l2-ctl --list-devices'

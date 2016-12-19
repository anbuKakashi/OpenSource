#anbuKakashi
# OpenSource
##CATATAN SAYA BERHASIL MENGGUNAKAN UBUNTU 14.04 LTS 64BIT

sudo add-apt-repository ppa:noobslab/themes
sudo apt-get update
sudo apt-get install mbuntu-y-ithemes-v4
sudo apt-get install mbuntu-y-icons-v4

sudo add-apt-repository ppa:noobslab/apps
sudo add-apt-repository ppa:noobslab/apps
sudo add-apt-repository ppa:docky-core/ppa
sudo add-apt-repository ppa:noobslab/themes

sudo apt-get update

#install synapse
sudo apt-get install indicator-synapse

#install slingclod
sudo apt-get install slingscold

#install docky
sudo apt-get install docky

#install tema docky
sudo apt-get install mbuntu-y-docky-skins-v4

cd && wget -O config.sh http://drive.noobslab.com/data/Mac-14.10/config.sh
chmod +x config.sh;./config.sh

#ini untuk screen saat booting
sudo apt-get install mbuntu-y-bscreen-v4

#ketikkan lagi perintah ini
cd && wget -O config.sh http://drive.noobslab.com/data/Mac-14.10/config.sh
chmod +x config.sh;./config.sh

##NANTI TAMPILANNYA SUDAH LANGSUNG DI SET


#lanjut
#ini untuk ganti ubuntu panel jadi macOs (yang ada di kiri atas)
cd && wget -O Mac.po http://drive.noobslab.com/data/Mac-14.10/change-name-on-panel/mac.po
cd /usr/share/locale/en/LC_MESSAGES; sudo msgfmt -o unity.mo ~/Mac.po;rm ~/Mac.po;cd

#ini untuk tmpilan lock screen
sudo xhost +SI:localuser:lightdm

sudo su lightdm -s /bin/bash
gsettings set com.canonical.unity-greeter draw-grid false;exit

sudo mv /usr/share/unity-greeter/logo.png /usr/share/unity-greeter/logo.png.backup
cd;wget -O logo.png http://drive.noobslab.com/data/Mac-14.10/ubuntu_logo.png

sudo mv logo.png /usr/share/unity-greeter/;gsettings set com.canonical.unity-greeter draw-grid false

#ini buat ganti logo launcher yang ubuntu jadi gambar apple

wget -O launcher_bfb.png http://drive.noobslab.com/data/Mac-14.10/launcher-logo/apple/launcher_bfb.png

sudo mv launcher_bfb.png /usr/share/unity/icons/

#ini untuk font apple

wget -O mac-fonts.zip http://drive.noobslab.com/data/Mac-14.10/macfonts.zip
sudo unzip mac-fonts.zip -d /usr/share/fonts; rm mac-fonts.zip
sudo fc-cache -f -v

kalo sudah setting fontnya,,, pake gnome-tweek-tool
ketikkan apple

#ini untuk layar login 

sudo add-apt-repository ppa:noobslab/themes
sudo apt-get update
sudo apt-get install mbuntu-y-lightdm-v4

##KALO SUDAH COBA DI REBOOT

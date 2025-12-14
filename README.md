# device

# i.can.penguin Kids Prototype

<img width="3065" height="1848" alt="image" src="https://github.com/user-attachments/assets/81d64604-d8e7-4219-a235-68af281ee8b7" />

Specification | Feature |
|:--|:--|
| 5 inch MIPI Display | 1280x720 |
| Luckfox Lyra Zero W | 512mb RAM | 
| Wireless  | see NOTE |
| Keyboard  | Solder Party KeebDeck Basic |
| Default Storade | SDcard/tf |
| Console 80x25 Default  | 16x28 Font |
| GUI | XFCE4 |
| Rotated Console| 270 Degrees |
| Default Brigness| 50 |
| Case | Still to look into | 
| Power Options | Still to look into |

# i.can.penguin Adult Prototype

<img width="1435" height="836" alt="image" src="https://github.com/user-attachments/assets/da619689-db2f-40ec-8f92-00e3b63a52a9" />

Specification | Feature |
|:--|:--|
| 10.1 inch MIPI Display | 1280x800 |
| Luckfox Lyra Pi W | 512mb RAM | 
| Wireless  | see NOTE |
| Keyboard  | Solder Party KeebDeck Basic |
| Default Storade | EMMMC | 
| Console 80x25 Default | 16x28 Font |
| GUI | XFCE4 |
| Rotated Console| 270 Degrees |
| Default Brigness| 50 |
| Case | Still to look into | 
| Power Options | Still to look into |

<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/6295b83a-7a8e-4d2b-b0ba-6c5242364663" />

```
Default User Login Credentials

User:     root
Password: root

User:     lyra
Password: luckfox

ADB shell requires no password and can be used to set or change existing passwords
```

# NOTE IMPORTANT FOR LYRA BOARDS WITH WIFI
```
adb shell "cd /home/lyra/aic800/ && make install; reboot"

#test
adb shell nmcli dev wifi list

#connect
nmtui
```

```
git clone -b develop https://github.com/i-can-penguin/device

cd device/device/rockchip/.chips/rk3506
ln -s .chips/rk3506 ../../rk3506
ln -s .chips/rk3506 ../../.chip
cd ../../../../

# 32a9f7e30ea47f678453f8a37e8a8e8cd2faa30d0e6d3af4c00f3f023a6adad4  os.tar.gz

git clone https://github.com/markbirss/os.git
cd os
rm -fr .git
7z x os.7z.001
rm -f os.7z*
# sha256sum os.tar.gz

mv os.tar.gz ../
cd ../
mkdir ubuntu
mv os.tar.gz ubuntu/ubuntu_24.04.3.tar.gz

#./build.sh lunch
# sudo ./build.sh
# sudo ./rkflash.sh update

```

#IMPORTANT NOTE
This SDK is provided for non commercial use only

UBUNTU require official autorization for commerical use

This SDK is provided without any warranty
Use at your own risk

Support my work and consider **buying  me a coffee**

https://buymeacoffee.com/mark.birss

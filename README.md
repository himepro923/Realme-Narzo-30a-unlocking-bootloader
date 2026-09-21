# Realme-Narzo-30a-unlocking-bootloader
this repo is for unlocking the bootloader and installing TWRP on the realme narzo 30a

THIS IS ONLY FOR RMX 3171 aka Realme narzo 30a
ALL YOUR DATA WILL BE GONE THIS GUIDE COMES WITH NO WARRANTY I IM NOT RESPONBLE FOR WHAT HAPPENS TO YOUR PHONE

if you broke your phone from a bad flash or it wont turn on or something go to the bottom of the readme you will fine help

Requirement:
1. Realme narzo 30a (Duh)
2. Type c USB cable
3. PC any OS (I use linux)
4. Python 3

So if you have a old 30a sitting around and you want to unlock and root it this this the best way i took all my research and info into this repo

Enable DEV MODE in anroind and go to oem unlocking and enable it and enable usb debugging

so first you need to get mtk client 
[Link to REPO](https://github.com/bkerler/mtkclient)

just clone the repo with
git clone https://github.com/bkerler/mtkclient
```bash
git clone https://github.com/bkerler/mtkclient
```

then just enter the folder and run

```bash
sudo python3 mtk_gui.py
```

after that this screen will show
<img width="1006" height="642" alt="image" src="https://github.com/user-attachments/assets/f0aa2f27-5db8-4076-a8bc-c777809fc607" />

now you have to get the phone and to use it with mtk client to do that

1. Press and hold both Volume buttons at the same time
2. while you hold the button connect the USB cable and keep holding until this screen show up

<img width="1011" height="630" alt="image" src="https://github.com/user-attachments/assets/41a86841-d16b-4643-bca3-51efa47f8f48" />

after that screen shoes NOW YOU HAVE TO MAKE A BACKUP DO NOT SKIP THIS 

1. go to the (Read partitions)
2. click on all the box exempt for USERDATA and CACHE
3. press read partitons

now use the folder you want to save them too and wait

after that go to Flash Tools and press Unlock bootloader and wait
<img width="1003" height="639" alt="image" src="https://github.com/user-attachments/assets/614ff5c5-1a5b-4c1c-ac41-f158d1d30cd7" />

and close mtk client and wait for the phone to restart it will take a while do not panic (mines took 48mins)

after you get back in your os find your you just backup vbmeta.bin (or .img) amd get your phone into fastboot by:
1. adb devices
2. accept the prompt on your phone
3. adb reboot fastboot
and you will get into fastboot

now type this in:
```bash
fastboot --disable-verity --disable-verification flash vbmeta PATH_TO/vbmeta.bin
```

now download from this repo the file named (TWRP_RMX-3171.bin)
and go to the write partitions on mtk client
<img width="989" height="629" alt="image" src="https://github.com/user-attachments/assets/d05fc22d-7cc4-49d6-958b-d08d95106c7d" />

go to the recoverey section and click SET and chose the file you just downloaded (TWRP_RMX-3171.bin)
[Link to FILE](https://drive.google.com/file/d/1wynoAtM29PUy1_R3o4dvipLyOkrpAbW_/view?usp=sharing)
and click (Write partitions)
then go to Read partitions and check (recovery)
and click read place it anywhere but DO NOT USE THE SAME FOLDER YOU USE FOR YOU MAIN BACKUP

after it says DONE close mtk client and disconnect the USB cable 
and hold power + volume down (for this part i dont now if it my phone or everyone but i have to hold power + volume down and let it vibrate 3 times then
remove my hand from power while still having my hand on volume down and letting it vibrate 3 more time then TWRP shows)

Do what i did if your phone doesn't boot TWRP that way then do the normal way of holding power + volume down until it vibrate and remove your hand

after that you will get this screen
<img width="3072" height="4096" alt="PXL_20260921_175050338" src="https://github.com/user-attachments/assets/78fedef7-4c38-4ab1-85c3-00cd0b9f7bc6" />

<img width="3072" height="4096" alt="PXL_20260921_175107316" src="https://github.com/user-attachments/assets/3bfcbe8f-9870-421c-9e94-8c92537c83c9" />

and that it you just unlock the bootloader and installed TWRP

THANKS ALL FOR READING THIS!!!

RESTOREING FROM A BACKUP:

Just go to the Write partitions of mtk client then click set directory and chose were you placed your backup and wait after it done just power on your phone

If you get i sign that you cant boot your phone and it auto power off it most likey your phone bootloader was relock just go to mtk client
and go to flash tools and unlock the bootloader and disconnect the USB cable and wait for your phone to boot

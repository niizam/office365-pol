# office365-pol
Panduan instalasi Microsoft Office 365 di sistem operasi berbasis Linux

Install playonlinux, winbind (samba), winetricks, dan mscorefonts

Untuk distro Debian dan turunannya (Ubuntu, Mint, Pop!_OS, dsb)
```bash
sudo apt install playonlinux winbind ttf-mscorefonts-installer winetricks
``` 

Untuk distro Arch dan turunannya (Manjaro, Endeavour, Garuda, dsb)
```bash
yay -S playonlinux samba ttf-ms-fonts winetricks
``` 

Unduh `wine.tar.xz` dari halaman [Releases](https://github.com/niizam/office365-pol/releases)
Kemudian ekstrak `wine.tar.xz` menggunakan perintah ini
```bash
mkdir -p /home/$USER/.PlayOnLinux
tar -C /home/$USER/.PlayOnLinux -xvf wine.tar.xz
```

Anda harus punya akun Microsoft yang memiliki lisensi Office365 agar bisa mendownload installernya

Anda juga membutuhkan plugin ([Firefox](https://addons.mozilla.org/en-US/firefox/addon/user-agent-string-switcher/) / [Chrome](https://chrome.google.com/webstore/detail/user-agent-switcher-and-m/bhchdcejhohfmigjafbampogmaanbfkg)) untuk mengubah user agent browser dari Linux ke Windows 7
1. Ubah user agent browser anda ke Windows 7 dengan plugin
### ![image](https://github.com/niizam/office365-pol/assets/45286708/339f6eba-81bb-4d37-b0bf-9aee5965e13e)

2. Buka dan login https://portal.office.com/account/?ref=MeControl
3. Klik View apps & devices
### ![image](https://github.com/niizam/office365-pol/assets/45286708/fa669123-4c66-4d96-8bc5-44c96dc26200)
4. Pilih bahasa yang diinginkan dan pilih versi 32 bit
5. Kemudian klik Install Office untuk mengunduh installernya yang bernama `OfficeSetup.exe`

### ![image](https://github.com/niizam/office365-pol/assets/45286708/d8ad64ed-0a8c-441b-b62d-61115996a44a)


Unduh skrip PlayOnLinux [office365-pol.sh](https://raw.githubusercontent.com/DonutsBl/office365-pol/main/office365-pol.sh) dengan mengklik kanan kemudian Save As 

Buka PlayOnLinux, kemudian pilih menu `Tools`, dan pilih `Run a Local script`, selanjutnya klik Next dan pilih skrip `office365-pol.sh` yang tadi diunduh.
### ![image](https://github.com/niizam/office365-pol/assets/45286708/a68c9d15-e254-4c27-b9a3-0eb8cc9660ac)

Selanjutnya centang I agree
### ![image](https://github.com/niizam/office365-pol/assets/45286708/ca8cf9b0-f172-420a-bd8c-16d98d617546)
Pilih `OfficeSetup.exe` yang sudah diunduh
### ![image](https://github.com/niizam/office365-pol/assets/45286708/5abedbfb-16e4-4049-99ce-38d56bebda56)
Selanjutnya akan muncul jendela konfigurasi wine, ubah versi Windows 8 ke Windows 7.
### ![image](https://github.com/niizam/office365-pol/assets/45286708/e4761fef-f95f-4fff-bae9-4465d679293e)


Proses unduhnya mungkin akan memakan waktu yang lama. Jika sudah selesai menginstal, Office365 sudah dapat dijalankan.
### ![image](https://github.com/niizam/office365-pol/assets/45286708/a6590b16-4b79-4f99-af59-160b5356ba33)



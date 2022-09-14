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
tar -C /home/$USER/.PlayOnLinux -xvf wine.tar.xz
```

Anda harus punya akun Microsoft yang memiliki lisensi Office365 agar bisa mendownload installernya

Anda juga membutuhkan plugin ([Firefox](https://addons.mozilla.org/en-US/firefox/addon/user-agent-string-switcher/) / [Chrome](https://chrome.google.com/webstore/detail/user-agent-switcher-and-m/bhchdcejhohfmigjafbampogmaanbfkg)) untuk mengubah user agent browser dari Linux ke Windows 7
1. Ubah user agent browser anda ke Windows 7 dengan plugin
2. Buka dan login https://portal.office.com/account/?ref=MeControl
3. Klik View apps & devices
4. Pilih bahasa yang diinginkan dan pilih versi 32 bit
5. Kemudian klik Install Office untuk mengunduh installernya yang bernama `OfficeSetup.exe`

Unduh skrip PlayOnLinux [office365-pol.sh](https://raw.githubusercontent.com/DonutsBl/office365-pol/main/office365-pol.sh) dengan mengklik kanan kemudian Save As 

Buka PlayOnLinux, kemudian pilih menu `Tools`, dan pilih `Run a Local script`, selanjutnya klik Next dan pilih skrip `office365-pol.sh` yang tadi diunduh.
Selanjutnya centang I agree, dan pilih `OfficeSetup.exe` yang sudah diunduh, selanjutnya akan muncul jendela konfigurasi wine, ubah versi Windows 8 ke Windows 7.

Jika sudah selesai menginstal, Office365 sudah dapat dijalankan.

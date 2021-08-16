# office365-pol
An experimental PlayOnLinux script that utilizes the version of Wine made for CrossOver to run Microsoft 365 Apps / Office 365 on Linux-based systems without requiring any paid CrossOver components

## Fair warning
At his point in time, this script is not recommended for beginner users since it requires you to manually compile the CrossOver version of Wine (also known as winecx). The method explained [here](https://github.com/DonutsBl/office365-pol/blob/main/docs/build-wine.md) utilizes Docker to create a clean compiling environment, so it really should work every time. But it's still a fairly complicated process with a lot of command prompt wizardry involved.

## Installation guide
- Install PlayOnLinux (obviously) as well as winbind, which is required for the Office installer to work. If you can't find  (a decently recent version of) PlayOnLinux in your distribution's package repositories, you can visit [the official PlayOnLinux website](https://www.playonlinux.com/en/download.html) for installation instrucions. If you can't find winbind, try installing samba, which sometimes contains winbind.
- Compile and install winecx according to the instructions [here](https://github.com/DonutsBl/office365-pol/blob/main/docs/build-wine.md).
- Install the Windows fonts if you haven't done this yet. Note that you'll need fonts that typically don't come with the "Microsoft corefonts" packages that some Linux distributions offer. There's a guide on installing all fonts that ship with Windows [here](https://github.com/DonutsBl/office365-pol/blob/main/docs/windows-fonts.md).
- Download the Microsoft 365 Apps / Office 365 setup. Note that the offline installer won't work, as it currently requires at least Windows 8.1, while this script only works while emulating Windows 7. The 64-bit version is not compatible either. To download the 32-bit online installer, go to https://portal.office.com/account/?ref=MeControl, log in with the account that your Office license is linked to, then click on "View apps & devices". Now, you should see the options for downloading Office, but you probably won't, as they only display when using Windows to visit the website. So, you'll either have to use a Windows device for the download or change your user agent to pretend you're using Windows. Once you can see the options, select the 32-bit version, then select the language you want and click on the "Install Office" button to start the download.
- Download the installation script from https://raw.githubusercontent.com/DonutsBl/office365-pol/main/office365-pol.sh by right-clicking the link and then choosing the "save as" option.
- Open up PlayOnLinux, choose Tools | Run a local script, select the script you downloaded and get past the warnings regarding the script not being authorized by the PlayOnLinux team. After that, the script should start and you can follow its instructions.

## License
Unless otherwise specified, everything in this repository is licensed under the Zero-Clause BSD license.
```
Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```
This does necessarily apply to every dependency that's needed to use this software, but isn't contained in its repository.
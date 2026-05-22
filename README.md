**You can use the [Flatpak instead](https://flathub.org/apps/details/com.brave.Browser), which probably is more secure and easier way to install Brave**

# brave package for Void Linux

This package provides Brave Browser, the browser based on Chromium with privacy in mind and a built in ad blocker. This package merely takes the .deb release version from the authors, extracts and installs the files as is. Plus, ensures the dependencies are there. **Note:** This repackages binaries instead of building from source. It is named brave (instead of brave-bin) specifically to sync and overlap with the Noid Linux repository.

The template file is prepared for use with [xbps-src](https://wiki.voidlinux.org/Xbps-src) in Void Linux.


## Installation & update

```
# Setup - do it once if not done already:
git clone https://github.com/void-linux/void-packages
cd void-packages
./xbps-src binary-bootstrap
git clone https://github.com/Ruintar/brave ./srcpkgs/brave

# To install and update Brave:
git -C ./srcpkgs/brave pull
./xbps-src pkg brave
sudo xbps-install --repository hostdir/binpkgs brave
```


## Auto update

The repository is automatically updated to the latest Brave stable release using Github Actions schedule.
By repeating installation commands described above you can update your Brave installation.

## Updating template version (repository development only!)

Template version can be updated by running `update-template.sh` script.

Dependencies:

1. `/bin/sh` (shell) (or any POSIX compliant shell that /bin/sh is linked to)
2. `gh` (GitHub CLI)
3. `sha256sum`
4. `envsubst` (part of `gettext`)

---

## Project Status & Maintenance Notice

This repository is maintained primarily for personal use and convenience. It is publicly available and anyone is welcome to use it; however, please be aware of the following:

- I am a relatively new maintainer.
- Updates are performed according to my own needs and availability.
- No guarantees are provided regarding long-term maintenance, response time to issues, or compatibility across all Void Linux configurations.
- This repository is unofficial and not affiliated with the Void Linux project.

If you prefer a more established third-party repository with broader maintenance guarantees, you may consider:

**Abyss Packages**  
https://codeberg.org/mobinmob/abyss-packages

Projects such as Abyss may follow stricter review processes and long-term maintenance practices. Their update cadence may differ.

By using this repository, you acknowledge that:

- This package repackages upstream `.deb` binaries.
- It is not built from source.
- You assume responsibility for verifying its suitability for your system.

**Noid Linux Repository**
https://github.com/noid-linux/xbps-repo
This is the repository where the `brave` package is also maintained. By naming this package `brave`, it allows for seamless version overlapping between this repository and Noid's.

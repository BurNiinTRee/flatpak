# BurNiinTRee's flatpaks
This repository contains a bunch of flatpak manifests for programs I use that aren't on flathub or elsewhere.

## Usage
Clone this repository recursively:
```bash
$ git clone --recursive https://github.com/BurNiinTRee/flatpaks
```
To build and install a specific flatpak, use `flatpak-builder`:
```bash
$ flatpak-builder build-dir --user --install <manifest>
$ # Or for subsequent builds
$ flatpak-builder --force-clean build-dir --user --install <manifest>
```
When prompted that some sdks or runtimes are missing, install those with
```bash
$ flatpak install flathub <id>
```

## Pianoteq
To install Pianoteq, you need to download it seperately from Modartt's website and place the extracted archive into this folder. You might need to adapt the source entry in the manifests (`com.modartt.Pianoteq.yml` and `org.freedesktop.LinuxAudio.Plugins.Pianoteq.yml`) or rename the extracted folder to match.

For the standalone application you also need to provide an icon as `com.modartt.Pianoteq.png`. I use the `v7-logo-black.png` from the presskit, which I extended to be 512 by 512 pixels. If you choose a different size, you need to adapt the icon folder in the manifest.

I don't know how copyright in regards to logos is typically handled, so I've elected not to include any
## Copying
I have no idea what license flatpak manifests are typically distributed as. If you have any suggestions, please let me know.
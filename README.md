# lf configuration forked from [cirala/lfimg](https://github.com/cirala/lfimg)
I liked a lot ranger, but in old machines lf is quite faster than ranger, so I have been migrating to lf, looking for a configuration similar to my ranger config without much additional work I have found cirala's one, that I have found perfect for my scope. I have adapted for some debian packages and to my layout preferences. 

# Image preview support for lf (list files) using Überzug

This set of scripts is used along lf to generate image previews and much like [vifmimg](https://github.com/cirala/vifmimg) it is able to handle image, video and ebook previews.

![image](https://raw.githubusercontent.com/f1se4/lfimg/master/screenshot.png)

When a SSH-connection has been established, [chafa](https://github.com/hpjansson/chafa) will be used instead.

## Prerequisites

Besides lf and Überzug you will need to install the following packages:

* ffmpegthumbnailer
* ImageMagick
* poppler
* epub-thumbnailer
* wkhtmltopdf
* bat (optional - color highlight for text files)
* chafa (optional - for image preview over SSH or inside Wayland session)
* unzip (optional - for .zip and .jar files)
* 7z (optional - for .7z files)
* unrar (optional - for .rar files)
* catdoc (optional - for .doc files)
* docx2txt (optional - for .docx files)
* odt2txt (optional - for .odt and *.ods files)
* gnumeric (optional - for .xls and .xlsx files)
* exiftool (optional - for music files)
* transmission (optional - for .torrent files)
## Installation in Debian Distro

```
sudo apt install p7zip odt2txt poppler-data poppler-utils ffmpegthumbnailer imagemagick wkhtmltopdf unzip unrar catdoc docx2txt gnumeric transmission
sudo pip install ueberzug
```

In the project directory you can run the following command:

```
make install
cp ./lfrc ~/.config/lf/lfrc
```

To install this to your system, or you can do it manually by following the guide below:

1. Extract the following files: **cleaner**, **preview** to **~/.config/lf/**.
2. Extract **lfrun** to a directory that is in your $PATH variable (such as /usr/bin).
3. Copy source lfrc to your **~/.config/lf/lfrc** or edit yours file and add the following lines:

```
set previewer ~/.config/lf/preview
set cleaner ~/.config/lf/cleaner
```
4. In order to launch lf with image preview support from now on, you will need to use the supplied **lfrun** script.

Is recommended that you make an alias in your shell that points to lfrun.

## Credits
* [lfimg](https://github.com/cirala/lfimg) original source which I have forked from.
* [lf](https://github.com/gokcehan/lf/)
* [Seebye's Überzug](https://github.com/seebye/ueberzug)

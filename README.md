OpenSubtitlesDownload.py
========================

[![GitHub release](https://img.shields.io/github/release/emericg/OpenSubtitlesDownload.svg?style=flat-square)](https://github.com/emericg/OpenSubtitlesDownload/releases)
[![GitHub contributors](https://img.shields.io/github/contributors/emericg/OpenSubtitlesDownload.svg?style=flat-square)](https://github.com/emericg/OpenSubtitlesDownload/graphs/contributors)
[![GitHub issues](https://img.shields.io/github/issues/emericg/OpenSubtitlesDownload.svg?style=flat-square)](https://github.com/emericg/OpenSubtitlesDownload/issues)
[![License: GPL v3](https://img.shields.io/badge/license-GPL%20v3-brightgreen.svg?style=flat-square)](http://www.gnu.org/licenses/gpl-3.0)

## Introduction

**OpenSubtitlesDownload.py** is a small software written in Python, built to help you **quickly find and download subtitles** for your favorite videos. It can be used as a nautilus script, or as a regular application working under GNOME or KDE desktop environments. You can also use it in full CLI mode (Command Line Interface) on your NAS, Raspberry Pi or anywhere you want really, as long as you have a working Python interpreter.

The subtitles search is done by precisly **identifying your video files** by computing unique movie hash sums. This way, you have more chance to find the **exact subtitles for your videos**, avoiding synchronization problems between the subtitles and the soundtrack. But what if that doesn't work? Well, a search with the filename will be performed, but be aware: results are a bit more... unpredictable (don't worry, you will be warned! and you can even disable this feature if you want).

The subtitles search and download service is powered by [opensubtitles.org](https://www.opensubtitles.org). Big thanks to their hard work on this amazing project! Be sure to [give them your support](http://www.opensubtitles.org/en/support) if you appreciate the service provided, they sure need donations for handling the ever growing hosting costs!

### Features

- Use a GNOME/GTK or KDE/Qt GUI depending on your favorite desktop environment
- Or just use the CLI! Great for automation, and it works on Linux, macOS and Windows
- Query subtitles in more than 60 different languages for documentaries, movies, TV shows and more...
- Query subtitles in multiple languages at once
- Query subtitles for multiple video files and folders at once
- Detect valid video files (using mime types and file extensions)
- Detect correct video titles by computing unique movie hash sums in order to download the right subtitles for the right file!
- If the video detection fails, a backup search using filename is performed
- Download subtitles automatically if only one is available, choose the one you want otherwise
- Download the subtitles file right next to the video file (need read/write permissions)
- Rename downloaded subtitles to match the video file. Possibility to add a language code (ex: movie_en.srt).

## Installation

#### Requirements

- Python 3 (you can use legacy versions to continue on Python 2)
- zenity (only needed for GNOME based desktop environments)
- kdialog (only needed for KDE based desktop environments)
- Common unix tools (only needed for GUIs): wget & gzip (GUI subtitles downloading), ps & grep (GUI autodetection)

#### Quick installation (nautilus script, with GNOME desktop environment)

For more installation options, check [the wiki](https://github.com/emericg/OpenSubtitlesDownload/wiki#installation-1)!

```bash
$ mkdir -p ~/.local/share/nautilus/scripts/
$ cd ~/.local/share/nautilus/scripts/
$ wget https://raw.githubusercontent.com/emericg/OpenSubtitlesDownload/master/OpenSubtitlesDownload.py
$ chmod u+x OpenSubtitlesDownload.py
```

#### IMPORTANT: use an opensubtitles.org account

Following a recent policy change from opensubtitles.org, the API is now available only for logged users. More informations can be found on [this discussion](https://github.com/emericg/OpenSubtitlesDownload/issues/51).  
If you are concern by this issue, the symptoms are **401 unauthorized** error messages. If you try too many times without a valid account, know that your IP address will be banned for 24 H.  

To continue using OpenSubtitlesDownload you simply need to:

- [Create an account](https://www.opensubtitles.org/en/newuser) on opensubtitles.org website
- [Use that account](https://github.com/emericg/OpenSubtitlesDownload/wiki/Adjust-settings#log-in-with-a-registered-user) with the script 

## Screenshots!

Start the search with a simple right click on a video file.
![Start subtitles search](https://i.imgur.com/gO02lb5.png)

If multiple subtitles are available, choose the one you want from the list!
![Multiple subtitles selection](https://i.imgur.com/v6C9QP4.png)

The download will only take a moment.
![Download selected subtitles](https://i.imgur.com/CI99lyx.png)

Enjoy your subtitled video!
![Enjoy your subtitled video!](https://i.imgur.com/9KKvISR.jpg)

## Get involved

#### Users
You can help us find and report bugs, propose new features, help with the documentation and more! Visit the [Issues](https://github.com/emericg/OpenSubtitlesDownload/issues) section to start!

#### Developers
You can browse the code on the GitHub page, submit patches and pull requests! Your help would be greatly appreciated ;-)

## Contributors

- Emeric Grange <emeric.grange@gmail.com> maintainer
- Thiago Alvarenga Lechuga <thiagoalz@gmail.com> for his work on the 'Windows CLI' and the 'folder search'
- jeroenvdw for his work on the 'subtitles automatic selection' and the 'search by filename'
- Gui13 for his work on the arguments parsing
- Tomáš Hnyk <tomashnyk@gmail.com> for his work on the 'multiple language' feature
- Carlos Acedo <carlos@linux-labs.net> for his work on the original script
- And [many others](https://github.com/emericg/OpenSubtitlesDownload/graphs/contributors)!

## Website

You can browse the project website at <https://emeric.io/OpenSubtitlesDownload>  
You can browse the project GitHub page at <https://github.com/emericg/OpenSubtitlesDownload>  
Learn more about OpenSubtitlesDownload.py installation and configuration on the wiki at <https://github.com/emericg/OpenSubtitlesDownload/wiki>  

## License

OpenSubtitlesDownload.py is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.  
Read the [LICENSE](LICENSE) file or [consult the license on the FSF website](https://www.gnu.org/licenses/gpl-3.0.txt) directly.

> Emeric Grange <emeric.grange@gmail.com>

#Arch Linux PKGBUILDs for GOG games
These PKGBUILDs are provided for people who want a quick and dirty way to install their GOGs on Arch Linux.

##Usage
These PKGBUILDs probably shouldn't be used until they are pushed to the AUR, but you are free to pull this
repository and do whatever you want with them.

Note that each PKGBUILD assumes you **already have the GOG downloaded** and no PKGBUILD will attempt to download
a GOG automatically.

##Contributors
If you would like to contribute, just contact any of the current contributors.

Contributors should pull and work with the git in its entirety.

 - git pull git://github.com/Tea23/arch-gog.git
 - mkdir gamename
 - cd gamename
 - mkdir base
 - cd base
 - touch PKGBUILD

.gitignore should contain *at least*:

    *.pkg*
    *.exe
    src/
    pkg/
    
Do **not** push game datafiles or packages!!
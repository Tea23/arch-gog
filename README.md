#Arch Linux PKGBUILDs for GOG.com Games
These PKGBUILDs are provided for people who want a quick and dirty way to install their GOGs on Arch Linux.

See http://gogwiki.com/wiki/AUR for more information. You may also wish to see [this](http://www.gog.com/en/forum/general/project_arch_linux_pkgbuild_installers_for_gogs)
GOG forum thread for more discussion.

##Usage
These PKGBUILDs probably shouldn't be used until they are pushed to the AUR, but you are free to pull this
repository and do whatever you want with them.

Note that each PKGBUILD assumes you **already have the GOG downloaded** and no PKGBUILD will attempt to download
a GOG automatically.

Packages installed from this git are *unsupported*. Only those in the official AUR should be used. However if you
would like to use these packages, you can pull this repo. Here we'll install Broken Sword:

    $ git clone git://github.com/Tea23/arch-gog.git
    $ cd arch-gog/products
    $ mkdir brokensword/src
    $ mv /path/to/setup_broken_sword.exe brokensword/src
    $ cd brokensword
    $ makepkg
    # pacman -U gog-brokensword-1.0.0.7-1-any.pkg.tar
    
And then to run it, check your XDG games menu or run `brokensword`.

##Contributors
If you would like to contribute, just contact any of the current contributors.

Contributors should pull and work with the git in its entirety.

    $ git clone https://github.com/Tea23/arch-gog.git
    $ cd arch-gog/products
    $ cp -Rv ../template gamename
    $ cd gamename
    $ mv PKGBUILD.dosbox PKGBUILD (whichever meta package is appropriate)
    $ rm PKGBUILD.* (plus any launcher packages that won't be used)
    
Do **not** push game datafiles or packages!! .gitignore in the root should protect against this, but please
add your own .gitignore rules where appropriate.

When you've finished making your PKGBUILD, you've built it and you've tested it, go back to the gitroot and:

    $ git add gamename/
    $ git commit -m "added a super awesome game yo"
    $ git push -u origin master

Have fun.

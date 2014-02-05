<!-- 
.. link: 
.. description: 
.. tags: LiveCD,Arch Linux,News
.. date: 2014/01/30 00:17:32
.. title: MATE desktop Live CD
.. slug: 2014-01-30-mate-desktop-live-cd
.. author: Martin Wimpress
-->

We've made a Live CD that boots into a full MATE desktop.

This Live CD was created so that potential new users can evaluate the MATE 
desktop in a non-destructive fashion. The image can be burned to a DVD, 
mounted as an ISO file, or be directly written to a USB stick using a utility 
like `dd`. You can download it below:

### BitTorrent download (recommended)

If you can spare the bytes, please leave the client open after your download 
is finished, so you can seed it back to others. *A web-seed capable client is 
recommended for fastest download speeds.*

  * [matelivecd-14.029.2321.iso.torrent](http://repo.mate-desktop.org/livecd/matelivecd-14.029.2321.iso.torrent)

### HTTP direct download

In addition to the BitTorrent link above, Live CD .iso can also be 
downloaded via HTTP. Please ensure the downloaded file matches the SHA1 
checksum.

  * [matelivecd-14.029.2321.iso](http://repo.mate-desktop.org/livecd/matelivecd-14.029.2321.iso) [ ~889MB ]
    * SHA1: `d925500e782d1821d1ebecbab4f81e8fa931fea3`

## Compatibility

The Live CD is built using [Arch Linux](http://www.archlinux.org) and MATE 
1.6. The Live CD is 32-bit so should work on any i686 or x86_64 computer
with at least 512MB RAM. Xorg drivers are included for Intel (`i915`),
AMD/ATI (`radeon`) and nvidia (`nouveau`) with a fall back to VESA.
Drivers for Virtual Box and VMware are also included so that evaluation
using these virtualization solutions is simple.

All common file systems, including [ZFS](http://open-zfs.org), are supported 
and some data recovery and backup tools are included. If you plug in your 
mobile device it will most likely be recognised and you'll be able to access 
the data on it. NetworkManager is included along with all the VPN clients it 
supports.

## Usernames and passwords

The MATE Desktop Live CD has the following accounts configured.

  * `root` - password is `livecd`.
  * `mate` - password is `livecd`.

The `root` account is obviously `root`. The `mate` account it a regular user 
that has with full password-less `sudo` rights. The Live CD will auto-login 
using the `mate` account.

## Applications

The Live CD is primarily designed to showcase the MATE desktop, however we've 
included some additional applications that are not part of the MATE desktop in 
order to make the LiveCD a little more useful and enjoyable.

  * [Firefox](https://www.mozilla.org/firefox/)   - Standalone web browser from mozilla.org
  * [GParted](http://gparted.sourceforge.net)   - A Partition Magic clone, frontend to GNU Parted
  * [HardInfo](http://hardinfo.berlios.de/wiki/index.php/Main_Page)  - A system information and benchmark tool
  * [Hexchat](http://hexchat.github.io/)   - IRC client configured to auto-connect to [#mate@freenode](https://webchat.freenode.net/?channels=#mate)
  * [Orca](http://www.gnome.org/projects/orca)      - Screen reader for individuals who are blind or visually impaired
  * [Pidgin](http://pidgin.im/)    - Multi-protocol instant messaging client
  * [Truecrypt](http://www.truecrypt.org/) - Free open-source cross-platform disk encryption software
  * [Xnoise](http://www.xnoise-media-player.com/)    - Media player with a slick GUI, great speed and lots of features

## Creative Commons content

We have bundled the following Creative Commons licensed content.

  * [Think Python](http://www.greenteapress.com/thinkpython/)                        - To read with Atril
  * [Nine in Nails Ghosts I - IV](http://ghosts.nin.com/main/home) album   - To listen to with Xnoise
  * [Nine in Nails Ghosts I - IV](http://ghosts.nin.com/main/home) photos  - To view with Eye of MATE

## Changing language

Be default the Live CD is configured to use the `en_US` locale but if you want 
to activate another language here is how to do it. In the example below, we 
will enable Italian.

Edit `/etc/locale.gen` an uncomment your locale, in this case `it_IT.UTF-8 UTF-8`
and rebuild the locales.

    sudo locale-gen

Edit `/etc/locale.conf` and change the `LANG=` to reflect your locale, in this 
case `LANG=it_IT.UTF-8`. Finally restart the display manager and you will be 
logged back into a MATE session using your prefered language.

    sudo systemctl restart lightdm

## Feedback

We hope you give the Live CD a test drive and enjoy the speed and simplicity 
the MATE Desktop provides. Once you've taken the MATE Desktop Live CD for a 
spin let us know what you think in the comments or use the Live CD to join us 
in the [#mate IRC channel](https://webchat.freenode.net/?channels=#mate).

<div class="alert alert-success">
<strong>Discussion</strong> <a href="http://forums.mate-desktop.org/viewtopic.php?f=20&t=2917" class="alert-link">Comments</a>
</div>
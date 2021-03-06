---
layout: post
tags: 
- ds
- fileformats
title: Nintendo DS File Formats
image: /public/consoles/Nintendo DS.png
thumbnail: /public/consoles/Nintendo DS.png
permalink: /DSFileFormats
breadcrumbs:
  - name: Home
    url: /
  - name: Nintendo DS
    url: /ds
  - name: Nintendo DS File Formats
    url: #
recommend: 
- ds
- fileformats
editlink: /ds/DSFileFormats.md
---

# TAD (similar to a Wii WAD)
TAD files are installable applications for the Nintendo DSi, similar in function to the WAD file for the Wii console.

Developers would create these files by converting an SRL ROM to TAD format with a tool called **maketad**.

It is not common to see TAD files out in the wild as they tend to be used by developers. However in the Platinum leak there was a huge archive of DSi applications in TAD format. Some of these are even debug versions so may contain full debug symbols useful for reverse engineering.

Developers would use an application called **TwlNmenu** to install TAD files on their DSi hardware.

However there doesn't seem to be a tool capable of installing TAD files on a modified DSi as of September 2020. There also doesn't seem to be a way to extract the contents or even emulate them.

Interestingly it is possible to resign a TAD file using the Wii resigning tools, but it won't be able to be installed on a modified DSi due to anti-tampering methods [^1].

[TwlNmenu - RGDWiki](https://wiki.mariocube.com/index.php?title=TwlNmenu&mobileaction=toggle_view_desktop)

## TwlNmenu on 3DS?!
Do not run TwlNmenu on 3DS unless you have backed up your TWLN partition and you find a way to get valid certificates. In theory if you got valid certificates you would be able to install the TAD files but noone has yet managed to do it.

You can see a video of running TwlNmenu on a 3DS below:
<iframe width="560" height="315" src="https://www.youtube.com/embed/gm5_nZOm_kM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
# SRL Format
SRL is the extension Nintendo uses for Nintendo DS ROMS and is the same as the NDS format. You can rename .srl files to .nds and they should play in an emulator [^3].

Also it seems that on the Wii U Nintendo used the .srl file extension for their Nintendo DS emulated ROMs.

You can convert SRL files to TAD format with the SDK tool called **maketad**.

---
# TMD Format (Title metadata)
A TMD file is simply just a meta data file that stores information about an App such as the contents and SHA1 hashes for verification. The format is also used for 3DS and Wii titles.

For more information check out the DSiBrew page:
[Title metadata - DSiBrew](https://dsibrew.org/wiki/Title_metadata)



---
# References
[^1]: [TwlNmenu - RGDWiki](https://wiki.mariocube.com/index.php?title=TwlNmenu&mobileaction=toggle_view_desktop)
[^2]: [TWL Dev Apps working on retail 3DS! - YouTube](https://www.youtube.com/watch?v=gm5_nZOm_kM)
[^3]: [How do you convert Nintendo DS .SRL into decrypted .NDS?](https://gbatemp.net/threads/how-do-you-convert-nintendo-ds-srl-into-decrypted-nds.400279/)

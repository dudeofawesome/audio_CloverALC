![alt text](https://github.com/toleda/audio_RealtekALC/blob/master/sound.jpeg)
#audio\_cloverALC

**OS X/Clover Patched AppleHDA Realtek ALC Audio**

Native AppleHDA/Persistent

The Clover Patched Realtek ALC method enables OS X AppleHDA onboard audio with or without HDMI and DP audio. The script adds codec specific layout and platform files and injects binary patch and pin configuration data to the native installed AppleHDA.kext.

**Versions: audio_cloverALC-110**

1. Easy: .command, see C. Installation
2. Bash: .sh, see D. Terminal

**Updates**

1. 11-8-15 - Skylake/Series 100 Update, Add 1150/Audio ID: 3
2. 7-19-15 - 283 Update
3. 6-15-15 - 10.11 - El Capitan Realtek ALC AppleHDA.kext Initial Support

**A. Requirements**

1.  OS X/Clover_v2696 or newer
    1.  10.11/El Capitan, set boot flag: rootless=0
    2.  10.10/Yosemite, set boot flag: kext-dev-mode=1
    3.  10.9/Mavericks
    4.  10.8/Mountain Lionon
2.  Native AppleHDA.kext
    1.  [Need native?](https://github.com/toleda/audio_ALC_guides/blob/master/Restore%20native%20AppleHDA%20%5BGuide%5D.pdf)
3.  Supported Realtek onboard audio codec
    1.  [Unknown codec?](https://github.com/toleda/audio_ALC_guides/blob/master/Identify%20Audio%20Codec%20%5BGuide%5D.pdf)

**B. Realtek ALCxxx** (verify codec and Audio ID)

-  Supported codecs
    - 269 (BRIX only)
    - 283 (BRIX Pro and NUC only)
    - 885
    - 887
    - 888
    - 889
    - 892
    - 898
    - 1150
-  Supported Audio IDs
    1. supports 269, 283, 885, 887, 888, 889, 892, 898, 1150
        - up to 5.1 surround sound output channels
        - 1, 2, 3, 5, or 6 motherboard audio ports
        - Intel HD5000, AMD, Nvidia HDMI audio (requires DSDT edit)
    2. supports 887, 888, 889, 892, 898, 1150
        - up to 5.1 surround sound output channels
        - 3 motherboard audio ports
        - Intel HD5000, AMD, Nvidia HDMI audio (requires DSDT edit)
    3. supports 887, 888, 889, 892, 898, 1150
        - up to 2.1 output channels
        - 3, 5, or 6 motherboard audio ports
        - Intel HD3000, Intel HD4000, AMD, Nvidia HDMI audio (requires DSDT edit)

**C. Installation**

1.  Clover patched AppleHDA

    1.  [Download (View Raw) audio\_cloverALC-110.command](https://github.com/toleda/audio_CloverALC/blob/master/audio_cloverALC-110.command.zip)
    2.  Double click: Downloads/audio_cloverALC-110.command
    3.  Password:
    4.  Confirm Codec ALCxxx: (885, 887, 888, 889, 892, 898, 1150 only)
    5.  Clover/Legacy: answer y to Confirm Clover Legacy Install (y/n)
    6.  Clover Audio ID Injection (y/n):
    7.  Use Audio ID: x (y/n):
    8.  Optional: Terminal/Terminal Saved Output
2.  Restart
3.  Verify ALC onboard audio
    1.  System Preferences/Sound/Output/select audio device

**D. Terminal**

1. [audio_cloverALC-110_v1.0.4](https://github.com/toleda/audio_RealtekALC/blob/master/audio_realtekALC-110.sh): 887/888 legacy detection, bug fixes
2. v1.0.3: First release

**E. More Information**

1. [Details](https://github.com/toleda/audio_RealtekALC/blob/master/DETAILS.md)
    1.  Onboard Audio Solutions
    2.  Requirements - Supported/Unsupported
    3.  Notes
    4.  Guides
    5.  Tools
    6.  Problem Reporting
2. Terminal Saved Output
    1.  [Clover/EFI](https://github.com/toleda/audio_CloverALC/blob/master/Terminal%20Saved%20Output_v1.0.4-efi.txt)
    2.  [Clover/Legacy](https://github.com/toleda/audio_CloverALC/blob/master/Terminal%20Saved%20Output_v1.0.4-leg.txt)

Credit
THe KiNG, bcc9, RevoGirl, PikeRAlpha, SJ\_UnderWater, RehabMan, TimeWalker75a, lisai9093, [abxite](http://applelife.ru/threads/patchim-applehda-s-pomoschju-zagruzchika.39406/#post-353647)

toleda https://github.com/toleda/audio_cloverALC

# TB-330FU
Playing with Lenovo Tab M11 (TB-330FU)
## Stock paramters
- Lenovo ZUI 16.0.070
- Android 14
- 8GB Ram and 128GB Storage
- CPU:
## Used software
 - [mtkclient](https://github.com/bkerler/mtkclient)

# Playing
  - Playing was on Linux so if you Windows or MacOS user huh good luck.

## BROM mode
 - Execute `./mtk_gui.py`
 - USB wire must be diconnected.
 - Hold down all three keys (power, volume up and volume down) at the same time, then connect the USB wire to the computer and at that moment release the keys
 - The MtkClientUI will show your device connected.

## Unlocking bootloader with UI
 - Enable Devoleper options (click on `About tabled -> Software verion` many times).
 - Unlock OEM `General Settings -> Devoleper options -> OEM unlocking`.
 - Power off the tablet
 - Enter to the [BROM mode](#brom-mode)
 - In the MtkClientUI go to `Flash Tools`
 - Click to the button `Unlock bootloader`
 - Done bootloader is unlocked and you can unplug USB wire. 

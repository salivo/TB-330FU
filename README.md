# TB-330FU
### Stock paramters
- Lenovo ZUI 16.0.070
- Android 14
- 8GB Ram and 128GB Storage
- CPU:
## Used software
 - [mtkclient](https://github.com/bkerler/mtkclient)
# DISCLAIMER
Be careful what you do, if you don't know what this command will do, I advise you not to execute it. This is not a tutorial, just my experience, so again, be careful
### CREATE DUMP FROM YOUR DEVICE!
 - If you want to do something from this you must create dump first.
 - To do that you must folow [Dump](#dump-all)

# Playing
  - Playing was on Linux so if you Windows or MacOS user huh good luck.
### DUMP All
 - Enter to the [BROM mode](#brom-mode)
 - Chouse in the `Read partiction(s)` section and click at the `Select all partictions`.
 - If you dont want to save your data you cant unselect `userdata` partiction.
 - Click to the `Read partiction(s)` button and choose folder where to save.
   
### BROM mode
 - Execute `./mtk_gui.py`
 - USB wire must be diconnected.
 - Hold down all three keys (power, volume up and volume down) at the same time, then connect the USB wire to the computer and at that moment release the keys
 - The MtkClientUI will show your device connected.

### Unlocking bootloader with UI
 - Enable Devoleper options (click on `About tabled -> Software verion` many times).
 - Unlock OEM `General Settings -> Devoleper options -> OEM unlocking`.
 - Power off the tablet
 - Enter to the [BROM mode](#brom-mode)
 - In the MtkClientUI go to `Flash Tools`
 - Click to the button `Unlock bootloader`
 - Done bootloader is unlocked and you can unplug USB wire.

### Fix dm-verity corruption
 - Solution I found here [XDA forum](https://xdaforums.com/t/lenovo-tab-m11-tb-330xu-dm-verity-corruption.4666236/#post-89652789).
#### Fix that button press is needed to boot 
 - Install [lkpathcer](https://github.com/R0rt1z2/lkpatcher).
 - Then get `lk_a.bin` and `lk_b.bin` from [Dump](#dump-all).
 - Patch they, don't forget to set your path to the file `lk_a.bin` and `lk_b.bin`.
```console
python3 -m lkpatcher -o pathed_lk_a.bin lk_a.bin
python3 -m lkpatcher -o pathed_lk_b.bin lk_b.bin
```
 - Then flash with MtkClentUI.
 - In the `Write partiction(s)` section set path to the `pathed_lk_a.bin` and `pathed_lk_a.bin` for `lk_a` and `lk_b` respectively.
 - Click to the `Write partiction(s)` button


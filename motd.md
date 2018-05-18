<!--- 2018-05-17T10:00:00.0000000-05:00 -->

## Thursday, May 17th

---

Thank you everyone who's been upgrading to this latest version!

### Known Issues with v1.2.5

---

#### Recently fixed:

- `MD5 checksum failed` on `Install/Repair` trying to flash custom kernel.
- Settings being reset when installing hmods.
- Inability to restore original kernel from file.
- Failure to update hakchi scripts using `Install/Repair`
- **C8 error** when installing games with non-standard codename.

#### Ongoing:

- Newly added games into one games collection will not be automatically selected in other collections sharing the same files, i.e. `snes-usa`, `snes-eur` and `snes-jpn`
- `UnauthorizedAccessException` or `IOException The media is write protected` on USB key export. This error is caused by having run the app as Administrator previously, hence requiring higher permissions to access the files afterwards. You can use this utility [Reset files permissions](http://lallouslab.net/2013/08/26/resetting-ntfs-files-permission-in-windows-graphical-utility/) to repair your files.
- If you want your **autoplay** or **pixelart** folders in your custom added games to work, you have to disable `Settings > Use linked sync` for the time being.
- If you **really** cannot make network mode work (this is the default mode when installing hakchi scripts from a clean slate), you can install the legacy component *clovershell*, which is available in user_mods, through the `Modules > Install extra modules` menu item. You may have to use the hidden `Settings > Developer tools > Force clovershell memboots` option as well, and if you do, you have to press `CTRL-F12` to make this menu visible. Use these options with caution.

---

**We are always working on improving hakchi2 CE**

*Team Shinkansen*

---

### Trending Questions

---

**Q:** After rebooting, I get a dialog saying my NES/SNES Mini is taking a long time to reboot and it never comes back online.

**A:** There are many possible reasons for this, but a common issue is with the drivers not installing correctly. You can either try manually installing the driver located in `hakchi2_CE/driver` names `nesmini_driver.exe`, or if this does not work, you can also try an open-source utility called `Zadig`. You can download it at this address: [Zadig - USB driver installation made easy] (https://zadig.akeo.ie/).

---

**Q:** My NES/SNES Mini is in `Recovery mode`, I can't do anything, what is that?

**A:** This mode is when your console does not boot completely, or if you've attempted a kernel operation that might have failed. It will also happen if you select `Kernel > Advanced -> Boot recovery kernel from RAM` of course. To get out of this mode, if you don't know how to use the shell, is to click `Tools > Reboot` or, if this does not work, turn off the NES/SNES Mini power switch, and unplug its USB power cable manually.

---

**Q:** Where is the dump kernel menu option?

**A:** While the new releases of hakchi do NOT require any manual dump of your original kernel, we have still decided to re-add the option in  `Kernel > Advanced > Dump original kernel (legacy)`. You can use this for backwards compatibility with other hakchi2 releases.

---

**Q:** Where is the `Folders Manager` menu item that was present in the `Tools` menu before?

**A:** For consistency, it's been moved to `Structure > Custom - Use folders manager` button-menu. Select this option and click on it again to access the folders manager.

---

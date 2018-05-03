<!--- 2018-05-03T10:15:00.0000000-05:00 -->

## Monday, May 3rd

---

Thank you everyone who's been upgrading to this latest version!

### Known Issues with v1.2.4

---

#### Newly added:

- When uninstalling hakchi from a NES/SNES Mini that has not been installed from scratch with v1.2.x, there is a bug preventing restore using a kernel image file at the moment. It has been fixed in source and will make its way into the next release. In the meantime, you can use v1.1.0 to restore to stock/uninstall with an existing kernel image file.

#### Recently fixed:

- **Failure to update** hakchi scripts on your NES/SNES Mini or **Write error** appearing after clicking `yes` on the update prompt, or by using `Kernel > Install/repair` menu option.
- **C8 error** when installing games with non-standard codename. Use standard NES/SNES Mini convention for directory and .desktop file names: `CLV-A-BCDEF`

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

**Q:** My NES/SNES Mini is in `Recovery mode`, I can't do anything, what is that?

**A:** This mode is when your console does not boot completely, or if you've attempted a kernel operation that might have failed. It will also happen if you select `Kernel > Advanced -> Boot recovery kernel from RAM` of course. To get out of this mode, if you don't know how to use the shell, is to click `Tools > Reboot` or, if this does not work, turn off the NES/SNES Mini power switch, and unplug its USB power cable manually.

---

**Q:** Where is the dump kernel menu option?

**A:** While the new releases of hakchi do NOT require any manual dump of your original kernel, we have still decided to re-add the option in  `Kernel > Advanced > Dump original kernel (legacy)`. You can use this for backwards compatibility with other hakchi2 releases.

---

**Q:** Where is the `Folders Manager` menu item that was present in the `Tools` menu before?

**A:** For consistency, it's been moved to `Structure > Custom - Use folders manager` button-menu. Select this option and click on it again to access the folders manager.

---

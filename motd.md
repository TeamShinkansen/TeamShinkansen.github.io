<!--- 2018-04-27T10:40:00.0000000-05:00 -->

## Thursday, April 27th

---

### Known Issues with v1.2.3

---

#### Newly added:

- We're still noticing a failure to update hakchi scripts on your NES/SNES Mini after clicking `yes` on the update prompt, or by using `Kernel > Install/repair` menu option. We are working on it. In the meantime, you can either use `Kernel > Reset` which will start you from a clean slate, or `Kernel > Install/repair`, but while the NES/SNES Mini is shut down, and then follow the prompts. Those methods seem to work so far. **[Apr 27th, 2018]**

#### Ongoing:

- `UnauthorizedAccessException` or `IOException The media is write protected` on USB key export. This error is caused by having run the app as Administrator previously, hence requiring higher permissions to access the files afterwards. You can use this utility [Reset files permissions](http://lallouslab.net/2013/08/26/resetting-ntfs-files-permission-in-windows-graphical-utility/) to repair your files.
- If you want your **autoplay** or **pixelart** folders in your custom added games to work, you have to disable `Settings > Use linked sync` for the time being.
- If you **really** cannot make network mode work (this is the default mode when installing hakchi scripts from a clean slate), you can install the legacy component *clovershell*, which is available in user_mods, through the `Modules > Install extra modules` menu item. You may have to use the hidden `Settings > Developer tools > Force clovershell memboots` option as well, and if you do, you have to press `CTRL-F12` to make this menu visible. Use these options with caution.

#### Recently fixed:

- **C8 error** when installing games with non-standard codename. Use standard NES/SNES Mini convention for directory and .desktop file names: `CLV-A-BCDEF`
- **Write error** when updating. Use `Kernel > Install/Repair` instead.

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

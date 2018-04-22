<!--- 2018-04-21T22:35:00.0000000-05:00 -->

## Saturday, April 21st

---

### Known Issues

---

- **C8 error** when installing games with non-standard codename. Use standard NES/SNES Mini convention for directory and .desktop file names: `CLV-A-BCDEF`
- **Write error** when updating. Use `Kernel > Install/Repair` instead.

---

### FAQ / Trending Questions

---

**Q:** My NES/SNES Mini is in `Recovery mode`, I can't do anything, what is that?

**A:** This mode is when your console does not boot completely, or if you've attempted a kernel operation that might have failed. It will also happen if you select `Kernel > Advanced -> Boot recovery kernel from RAM` of course. To get out of this mode, if you don't know how to use the shell, is to click `Tools > Reboot` or, if this does not work, turn off the NES/SNES Mini power switch, and unplug its USB power cable manually.

---

**Q:** Where is the `Folders Manager` menu item that was present in the `Tools` menu before?

**A:** For consistency, it's been moved to `Structure > Custom - Use folders manager` button-menu. Select this option and click on it again to access the folders manager.

---

**Q:** Where is the dump kernel menu option?

**A:** It's gone! If you have a kernel dump in hand, you should still keep it safe, as uninstalling will require using it. However, if you're ever installing hakchi again on a NES/SNES mini which has its factory kernel installed, the backup is automatically done by the install script and saved somewhere safe, directly in the console's NAND memory.

---

**Q:** How can I give my games a "save icon" in the NES/SNES mini menu?

**A:** Use the `Save Count` property on the main hakchi2 CE interface. Setting it to zero means no icon, and any number from 1 to 3 will display an icon.

---

**Q:** My games are not sorted the way I want them to be! How can I change this?

**A:** The `Sort name` field in hakchi2 CE's main interface exists solely for this purpose. You can alter the default string generated there and it will affect sort order.

---

**Q:** My games are broken. The command line seems to point to an non-existent file. Is there anything I can try besides manually repairing them?

**A:** Yes. For games that don't work anymore, you can try the `Repair games` option that appears in the main games list context menu.

**Q:** Help! My original games don't show up in my games list!!!

**A:** This can happen if you either deleted the files in the `games_originals/` folder, or if you've selected `View > Original games > Hidden (Unselected)` in the menu. In the former case, use `File > Restore original games` menu item. In the latter, simply select a different option within that submenu, it should restore your original games in list!

---

**Q:** When I sync my games on my NES/SNES mini, it always takes a long time and the differential sync doesn't seem to help!

**A:** This can happen if you either use any of the automatic folders/pages generating options, because whenever you add or remove games, it substantially modifies the folders and file structure, so the differential sync cannot help much. There are two methods to help alleviate this: first we suggest you use the **"Linked sync"** option, this usually reduces the amount of data needed to transfer by a BIG margin. And second, if you manage your folders manually using the **"Custom - Use folders manager"** structure option, if you keep your folder structure very similar, it should not happen too often.

---

**Q:** When I sync my games on USB, it always takes a long time and the differential sync feature doesn't seem to help!

**A:** See above answer, this partly applies to USB export as well, however, in this case, the best scenario is to use the **"Linked export"** feature, accessible in the export dialog. This only requires that hakchi2 CE be installed on the USB drive. Keeping folder structure similar between exports will also help.

---

**Q:** Why can't I sync my NES (USA/Europe) games collection to my Super Famicom (Japan) console? I've read that this new version supports HSQS image files and multiboot!

**A:** In order to use *multiboot*, you simply have to make sure `Settings > Separate games for multiboot` is checked. Switching between enabling and disabling this option will *delete the previous games collection(s)* that were managed using either technique.

---

**Q:** I can't seem to use my games on my USB drive via my OTG device. It worked before!

**A:** One thing to verify first if it the menu option `Settings > Enable USB host` is enabled. This setting is stored on the NES/SNES mini and you either need to sync your games, or press the `Settings > Save settings to my NES/SNES mini now` option to save it.

---

**Q:** I'm getting occasional Clovershell timeouts during game syncs or other operations  

**A:** Clovershell ocasionally crashes. Your best bet is to reboot your console and maybe restart H2CE for good measure.

---

**Q:** Often when I try to drag a selection in the main games list, my mouse goes crazy and the list ends up scrolled past its limit.

**A:** This is a Windows API bug in the ListView control. Hard to tell when this bug was introduced, but it's present on any software using its built-in ListView control. There is someone on GitHub who released a small tool to fix this issue globally, if you're interested: https://github.com/tablacus/TablacusWindows10FCUBugFix/releases

---

### Have a nice day!

---

*Team Shinkansen*

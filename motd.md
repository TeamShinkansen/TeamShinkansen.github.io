<!--- 2018-08-01T15:17:00.0000000-05:00 -->

## Wednesday, August 1st

As many of you probably have noticed, we haven't enabled the auto-updater for v3.3.0 yet. The very reason why we did that is to iron out new bugs that might pop out with a new release, which is what has inevitably happened! The one main issue to look out for is the `Uboot` flashing issues.

We are working on fixing those issues! Hang tight!

---

### Known issues with v3.3.0

- `Kernel -> Flash Uboot` is currently having issues when verifying MD5 checksum. We've received reports of people both having success even if there was an error message, and others who've had issues afterwards, so it's better to hold on before using this function for the time being, or stick with v1.2.5.
- There is a typo in the `Shounen Jump` original games' command line, which may prevent them to work out-of-the-box when synced. The fix is to replace `/usr/bin/clover-kachikachi-wr` with `/bin/clover-kachikachi-wr`.
- `Settings -> Enabled USB host` and `Settings -> Use extended font` have no effect anymore.
- A cosmetic bug in the `Un/install modules` dialog prevents readmes from being parsed properly on some hmods.
- Font remount module (which is installed by default with `Kernel -> Install/Repair`) has some potential issues with newer versions of the Famicom/NES mini. It also has some missing Japanese characters.

---

### Noteworthy information regarding new release v3.3.0

If you've been upgrading from older versions of hakchi, it is very possible that your NES/SNES mini is still running the `Clovershell` protocol. If that is so, this new version of hakchi2 CE will not allow using `emulated FTP` or `Synchronization` as long as you are using it.

In order to use the new SSH connection protocol, you only need to first make sure your `kernel is up-to-date` and then you can go into `Modules -> Uninstall extra modules`, uncheck `clovershell` and then click `OK` at the bottom. If the uninstall goes well, when your NES/SNES mini reboots, it should be connected using the new network protocols.

---

**Have a nice day!**

*Team Shinkansen*

---

### Trending Questions

---

**Q:** After rebooting, I get a dialog saying my NES/SNES Mini is taking a long time to reboot and it never comes back online.
**A:** There are many possible reasons for this, but here are a few common causes:

- Drivers may not be installing correctly. You can either try manually installing the driver located in `hakchi2_CE/driver` named `Nintendo_Classic_USB_Driver.exe`, or if this does not work, you can also try an open-source utility called `Zadig`. You can download it at this address: https://zadig.akeo.ie/ .
- Sometimes, Windows' Firewall may be blocking the connection. Make sure to `Accept` incoming/outgoing connections when running hakchi2 CE. Windows should advise you of which program is requesting access. Only accept for hakchi2 CE. You can also, for debugging purposes, try to disable it and see if it works. Do not leave your system without a firewall afterwards though, this is there for a reason.
- A device may be confusing hakchi2 CE or your NES/SNES mini on the network, like a games console on your network, or other devices. If possible, you can try disabling your ethernet or wifi connection to see if it helps, as a temporary measure, of course.

---

**Q:** Where is the dump kernel menu option?
**A:** It's gone! If you have a kernel dump in hand, you should still keep it safe, as uninstalling will require using it. However, if you're ever installing hakchi again on a NES/SNES mini which has its factory kernel installed, the backup is automatically done by the install script and saved somewhere safe, directly in the console's NAND memory.

---

**Q:** Where is `SFROM Tool` located in hakchi2 CE? I've heard it supports it, but can't find how to use it!
**A:** You first need to visit DarkAkuma's website: http://darkakuma.z-net.us/p/sfromtool.html . And download his tool there. Also download the patches you want to apply. Then decompress the archive in the `sfrom_tool/` folder under your hakchi2 CE's personal directory (there is already a placeholder there for this use). Decompress the patches you want to use inside the `patches/` folder. And finally, in hakchi2 CE, enable `Settings > SFROM Tool` and profit! From then on, when importing SNES games, they will be converted by this tool. You can also find additional options in the games list's context menu `SFROM Tool`. Finally, there is helper code to allow dragging & dropping the install package and .cnp files onto hakchi2 CE. You can try this as well!

---

**Q:** Help! My custom games are not in the list anymore!
**A:** Make sure the menu option `Settings -> Separate games storage` is checked if you are using `/games` and `/games_snes` folders to store your NES and SNES games separately. When this option is unchecked, only games in `/games` are considered.

---

**Q:** Help! My original games are not shown in the list anymore!
**A:** A new feature is accessible through `Settings -> Always copy original games`. This will only allow using original games that have been previously cached by hakchi2 CE upon connecting the desired console. Unchecking it will show all original games, regardless of their availability. hakchi2 CE will continue to rely on those original games to be present on your NES/SNES mini when syncing games to it.

---


<!--- 2018-08-03T00:30:00.0000000-05:00 -->

## Friday, August 3rd

A new release candidate version of hakchi2 CE has been released on GitHub. This one needs testing by hardened veterans of the scene! That's because, in the midst of fixing bugs, a major upgrade in hakchi core scripts was made and the app was updated accordingly. Fingers crossed many issues are fixed and not too many introduced!

**Be advised:** You **WILL** need to use the `hold reset` method to update your kernel with this new release.

---

**Have a nice day**

*Team Shinkansen*

---

### Known issues with v3.3.0 (should be fixed in RC)

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

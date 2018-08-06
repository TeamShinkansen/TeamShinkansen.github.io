<!--- 2018-08-06T11:00:00.0000000-05:00 -->

## Monday, August 6th

**Version 3.4.1 hotfix** is out today. It fixes unforetold issues with SD card users.

**Be advised:** It's possible hakchi2 CE may not discover your NES/SNES mini when you first open up the new version. Give it more time than usual to make sure, at least 2 minutes, and if nothing happens, it's possible *you need to use the `hold reset` method* to update your kernel with this new release.

---

**Have a nice day**

*Team Shinkansen*

---

### Noteworthy information regarding new release v3.4.0

If you've been upgrading from older versions of hakchi, it is very possible that your NES/SNES mini is still running the `Clovershell` protocol. If that is so, this new version of hakchi2 CE will not allow using `emulated FTP` or `Synchronization` as long as you are using it.

In order to use the new SSH connection protocol, you only need to first make sure your `kernel is up-to-date` and then you can go into `Modules -> Uninstall extra modules`, uncheck `clovershell` and then click `OK` at the bottom. If the uninstall goes well, when your NES/SNES mini reboots, it should be connected using the new network protocols.

---

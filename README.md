# comfyArch
I will list all my arch rice config files, so you can use them without spending countless hours.
![](/pictures/comfyArch.jpg)

# Dualboot 
There's things to do before the installation:
- Disable Secure Boot in your BIOS
- Disable Fast Start-Up, it's a process that hibernates the OS rather than shutting it down to speed up boot times.
If you boot in your other OS, there's change of data loss if Windows is in hibernation.
- Detect the boot mode of Windows, Run `msinfo32` and check the value of the Bios Mode item. It's a lot easier to partition Arch if
Windows boot in BIOS/MBR mode if you've never done it.

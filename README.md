# comfyArch
I will list all my arch rice config files, so you can use them without spending countless hours.
![](/pictures/comfyArch.jpg)

# Dualboot 
There's things to do before the installation:
- Disable Secure Boot in your BIOS
- Disable Fast Start-Up, it's a process that hibernates the OS rather than shutting it down to speed up boot times.
If you boot in your other OS, there's change of data loss if Windows is in hibernation.
- Detect the boot mode of Windows, Run `msinfo32` and check the value of the Bios Mode item. It's a lot easier to partition Arch if
Windows boot in BIOS/MBR mode if you've never done it. But UEFI/GPT is the new standart and you will be able to reuse 
the EFI System Partition instead of creating a new one for the boot.

I strongly recommend you to be connected to an ethernet cable. Because if the driver your network card or adapter is not 
installed, it will be a real pain. If something like this happens, I will be glad to help you.

1. You need to make some space for Arch! run `diskmgmt.msc` and shrink one volume. It's possible that you can't shrink it as you want 
because there is file in the middle that can't be move. There's other tools like [Partition Wizard](https://www.partitionwizard.com/)
that will give you a broader management of the volume.



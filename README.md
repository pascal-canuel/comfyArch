# comfyArch
I will list all my arch rice config files, so you can use them without spending countless hours.
Why Arch? 
- It will give you a broader understanding of Linux/Unix. You will know what's going on if things break.
- The community is active. The wiki is just insane!
- It's a chance to take control of your computer.
- Rolling release and update the system with one command `pacman -Syu`
![](/pictures/comfyArch.jpg)

Sometimes it's going to be frustrating, but it's normal and it's going to take time

*“Hofstadter's Law: It always takes longer than you expect,    
even when you take into account Hofstadter's Law"*   
**- Douglas R. Hofstadter **   

# Dualboot 
There's things to do before the installation:
- Disable Secure Boot in your BIOS
- Disable Fast Start-Up, it's a process that hibernates the OS rather than shutting it down to speed up boot times.
If you boot in your other OS, there's change of data loss if Windows is in hibernation.
![](/pictures/fastBoot.PNG)
- Detect the boot mode of Windows, Run `msinfo32` and check the value of the Bios Mode item. It's a lot easier to partition Arch if
Windows boot in BIOS/MBR mode if you've never done it. But UEFI/GPT is the new standart and you will be able to reuse 
the EFI System Partition instead of creating a new one for the boot.

I strongly recommend you to be connected to an ethernet cable. Because if the driver your network card or adapter is not 
installed, it will be a real pain. If something like this happens, I will be glad to help you. For help see the page on [wireless network configuration](https://wiki.archlinux.org/index.php/Wireless_network_configuration)

1. You need to make some space for Arch! run `diskmgmt.msc` and shrink one volume. It's possible that you can't shrink it as you want 
because there is file in the middle that can't be move. There's other tools like [Partition Wizard](https://www.partitionwizard.com/)
that will give you a broader management of the volume.

2. Burn an iso of arch into an usb key with [Rufus](https://rufus.akeo.ie/)   
The parameters are for an UEFI/GPT mode. For a BIOS/MBR boot the file system needs to be FAT32
![](/pictures/rufus.PNG)

Read more than one time and carefully the [Dual boot with Windows](https://wiki.archlinux.org/index.php/Dual_boot_with_Windows) of the wiki and the [installation guide](https://wiki.archlinux.org/index.php/installation_guide). It's really important!
You will only need to create a `Swap & root & home` partition.    
Be careful, there's a lot of installation guide with outdated informations. Stick to the [wiki](https://wiki.archlinux.org/)

# Grub 

It should find your Windows boot manager too!   
`pacman -Syu grub efibootmgr os-prober`   
`grub-mkconfig -o /boot/grub/grub.cfg`   
install grub into the drive
`grub-install /dev/sdX`        
Confirm installation   
`ls -l /boot/efi/EFI/arch/`   

# Raspberry pi

Follow this [installation guide](https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-3)

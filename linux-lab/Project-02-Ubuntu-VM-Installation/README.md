# Project 02 — Ubuntu Virtual Machine Installation

## Objective

Install Ubuntu 24.04 LTS in a VirtualBox virtual machine on a macOS host to create a Linux environment for CompTIA A+ 
Core 2 study and practical lab work.

---

## Lab Environment

Host System:
- MacBook Pro
- macOS

Virtualization Software:
- Oracle VirtualBox
- VirtualBox Extension Pack

Guest Operating System:
- Ubuntu 24.04 LTS (Desktop)

---

## Steps Completed

1. Downloaded Ubuntu 24.04 Desktop ISO from the official Ubuntu website.

2. Created a new virtual machine in VirtualBox.

VM configuration:

- Name: `ubuntu-core-2-vm`
- Type: Linux
- Version: Ubuntu (64-bit)

Resource allocation:

- RAM: 4096 MB
- CPU: Default
- Storage: 25 GB (VDI, dynamically allocated)

3. Attached the Ubuntu ISO to the virtual optical drive.

4. Started the VM and launched the Ubuntu installer.

5. Completed the Ubuntu installation wizard.

Configuration during install:

- Language: English
- Keyboard: Default
- Installation type: Normal installation
- Disk setup: Erase disk and install Ubuntu (virtual disk)
- Created local user account

6. Installation completed and system rebooted into the Ubuntu operating system.

---

## Troubleshooting

During installation several issues were encountered.

### Issue 1 — Ubuntu VM Flickering / Blank Screen

Symptoms:

- Ubuntu installer would flicker between boot screen and a blank display.
- The VM appeared to freeze during boot.

Cause:

VirtualBox graphics controller was not set to the recommended setting for Ubuntu.

Resolution:

Changed the graphics controller in VirtualBox settings.

Steps:

VirtualBox → VM Settings → Display

Changed:

Graphics Controller → `VMSVGA`

This resolved the display instability and allowed Ubuntu to boot correctly.

---

### Issue 2 — macOS Host Freezing / Beachball

Symptoms:

- macOS became unresponsive while the VM was running.
- Ubuntu VM entered an aborted state.

Cause:

Resource pressure on the host system due to VM memory allocation.

Resolution:

Restarted VirtualBox and relaunched the VM after ensuring no other heavy applications were running.

VM relaunched successfully.

---

### Issue 3 — Ubuntu Boot Menu Appearing

After installation the GRUB boot menu appeared:

```
Ubuntu
Ubuntu (safe graphics)
Test memory
```

Resolution:

Selected **Ubuntu** to boot into the installed operating system.

System booted successfully.

---

## Final Result

Ubuntu 24.04 LTS successfully installed in a VirtualBox virtual machine.

The VM is now available for:

- Linux command line practice
- Operating system administration labs
- CompTIA A+ Core 2 study exercises
- General IT troubleshooting practice

---

## Skills Practiced

- Virtual machine creation
- Operating system installation
- VirtualBox configuration
- Basic virtualization troubleshooting
- Linux environment setup

---

## Next Steps

Planned future labs using this VM:

- Linux command line fundamentals
- File permissions and user management
- Package management using `apt`
- System monitoring and process management
- Networking commands and troubleshooting

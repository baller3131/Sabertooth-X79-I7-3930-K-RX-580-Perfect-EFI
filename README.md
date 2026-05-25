# Sabertooth-X79-I7-3930-K-RX-580-Perfect-EFI

So i wanna publish my Efi if you have an Sabertooth X79 I7 3930-K RX 580 2304SP.

# Why 2304SP?
Because it has a REAL RX 580.

If you have an RX 580 2048SP. you have to do spoof type stuff.

# Sata SSD Mustly NEEDED!

# What native macOS works?

Use Monterey if you want full native use. But if you want to use modern macOS like Sequoia 15, you have to use OCLP to Root Patch.

# TAHOE DOES NOT WORK!

Why? Because Cpu doesnt have avx2 and THERES NO GRAPHIC ACCELERATION PATCH YET!

# What if you want to use or experience old macOS?

if you really want to experience and old macOS. use High Sierra if you want to test an old macOS. Sierra and lower will not WORK!

# What about bios settings for Sabertooth X79?

### Disable These
* **Fast Boot** -> Disabled (Prevents USB and hardware initialization issues)
* **Secure Boot** -> Disabled / Other OS (Allows OpenCore to load)
* **SerialPort / COM Port** -> Disabled (Prevents early boot freezes)
* **Intel VT-d** -> Disabled (If you need it enabled for Windows, make sure `DisableIoMapper` is set to `True` in config.plist)
* **Asmedia USB 3.0 Controller** -> Disabled (Optional, but recommended if you face USB freeze on boot)

### Enable These
* **SATA Mode Selection** -> AHCI (Crucial for macOS to recognize your SATA SSD)
* **Intel Virtualization Technology (VT-x)** -> Enabled
* **Hyper-Threading** -> Enabled
* **Execute Disable Bit** -> Enabled
* **EHCI Hand-off** -> Enabled (Crucial for USB 2.0 stability on X79)

⚠️ **Important Note:** X79 motherboards have an **MSR Lock (CFG Lock)**. If your CPU power management panics, make sure `AppleCpuPmCfgLock` is checked in your OpenCore config.

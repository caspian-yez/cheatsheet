Windows Command Line
====================

# Turn off Hibernate

```bat
@powercfg -h off
```

# Get all File Path

```bat
DIR /A /B /S > result.txt
```

We can make this command a bat file.

Just put the bat file in desired folder and run it.

# Extract Content of `*.chm`

```bat
hh.exe -decompile \path-to-save-folder \path-to-chm-file
```
# VHD Attach

```bat
@echo off
echo select vdisk file="C:\Virtual Disk for Cache.vhd" >vhdsel
echo attach vdisk>>vhdsel
echo list disk>>vhdsel
diskpart /s vhdsel
del /f /q vhdsel
exit
```

# Get timestamp in ISO format in powershell

```powershell
Get-Date -Format "o"
```

# Delete Empty Directories

```bat
for /f "delims=" %d in ('dir /s /b /ad ^| sort /r') do rd "%d"
```

# Powershell registry search

```powershell
Get-ChildItem -Path Registry::HKEY_CLASSES_ROOT\xmp.*
```

# pnputil list devices

```bat
pnputil /enum-devices /bus PCI /deviceids   # list PCIe bus devices
pnputil /enum-devices /bus USB              # list USB bus devices
```

# Reboot into BIOS

```bat
shutdown /r /fw /t 0
```

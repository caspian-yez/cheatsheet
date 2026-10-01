command line
============

Search using grep

```sh
grep -rnw ./ -e "str"
```

emmc check

```sh
mmc cid read /sys/class/mmc_host/mmc1/mmc1\:0001/
mmc extcsd read /dev/mmcblk1 | grep -i back
```

Reset gonme app picker layout

```sh
gsettings reset org.gnome.shell app-picker-layout
```

ARP scan

```sh
sudo arp-scan -I <interface> -l
sudo arp-scan -I <interface> -l --ouifile=/usr/share/arp-scan/ieee-oui.txt
```

images to pdf

```sh
img2pdf -S A4 -o output.pdf 1.jpg 2.png
```

serial log

```sh
nohup grabserial -Q -d /dev/ttyUSB1 -T --timeformat="%Y-%m-%dT%H:%M:%S.%f" -o "~/Serial.%Y-%m-%dT%H:%M:%S.log" &
```

gcc get default include path

```sh
gcc -xc -E -v -
gcc -xc++ -E -v -
```

show nvme device logical sector size

```sh
nvme id-ns -H /dev/nvme0n1
```

change hard disk drive device logical sector size

```sh
hdparm --set-sector-size 4096 --please-destroy-my-drive /dev/sda
```

Redirect telnet output to file

```sh
telnet 10.124.122.199 2014 | tee -a -i ./log.log
```

export pdf to image

```sh
pdftoppm -png Linux_For_Beginners.pdf Linux_For_Beginners
```

debian static ip

```sh
# Wired Ethernet Interface
auto eth0
# iface eth0 inet dhcp
iface eth0 inet static
address 10.0.22.250
gateway 10.0.22.1
netmask 255.255.255.0
up route add -net 10.0.0.0 netmask 255.0.0.0 gw 10.0.22.1 dev eth0
```

Capture standard output, add timestamp and save to log

```sh
stdbuf -oL script -f >(ts "%F %.T" > session.log)
```

pandoc convert markdown to pdf

```sh
pandoc --pdf-engine=xelatex -V papersize:a4 -f markdown -t pdf document.md -o output.pdf
```

ls error when file start with `-`

```sh
ls -1 *.csv # will report error if any csv file start with -
ls -1 -- *.csv # this will work
```

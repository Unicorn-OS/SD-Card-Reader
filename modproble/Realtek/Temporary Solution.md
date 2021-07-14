# Remove module, insert SD card, then re=add!
```
sudo rmmod rtsx_pci_sdmmc
sudo rmmod rtsx_pci

# Add SD card now
sudo modprobe rtsx_pci_sdmmc
sudo modprobe rtsx_pci
```

# Prime: https://archived.forum.manjaro.org/t/sd-card-reader-not-working-after-kernel-update/129538/8

> A temporary solution is to run lspci, but it needs to be run manually every time an sd card is added/removed.

```
sudo modprobe rtsx_pci

# Instert a card and then run:
lspci -nnk
# it'll appear in Disks!
```

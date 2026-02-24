# mt76 driver with support for mt7902

This code is not tested on with a mt7902 wifi card, but is confirmed to still work fine on mt7921k.

This repository is a fork of openwrt/mt76 with the following changes:

- Applied the patchset from upstram [enabling mt7902](https://lore.kernel.org/linux-wireless/20260219004007.19733-1-sean.wang@kernel.org/)
- Fixed build on on 6.17, probably works on 6.18, 6.19 and 7.0
- Added dkms build scripts
- Added firmware from linux-firmware for mt7902

# Build instructions


```
cd /usr/src
git clone https://github.com/zekica/mt76-mt7902-backport.git mt76-1.0
dkms add -m mt76 -v 1.0
dkms build -m mt76 -v 1.0
dkms install -m mt76 -v 1.0
```

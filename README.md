## Openwrt extra package feed.

### Description

This is a repository for [OpenWrt](https://openwrt.org/) packages feed containing unmerged [**rrredir**]fork(https://github.com/lars18th/rrredir.git).

#### Advanced (already setup OpenWrt sdk)
To use these packages, add the following line to your ```feeds.conf``` or ```feeds.conf.default``` in the OpenWrt buildroot:

```src-git extra https://github.com/Andy2244/openwrt-extra.git```

Than include and install all packages from your ```feeds.conf```, while ensuring all extra packages are prefered via:
```
./scripts/feeds clean
./scripts/feeds update -a
./scripts/feeds uninstall -a
./scripts/feeds install -f -p extra -a
./scripts/feeds install -a
```
Make sure the install line notes the extra feed and afterwards run:
```make menuconfig``` or ```make defconfig``` to expand, create the ```.config```

The packages should appear under **Network->Samba4**, **Network->VPN->softethervpn5-server** and **Network->Filesystem->smbd-server**.

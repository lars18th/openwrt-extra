## Openwrt extra package feed.

### Description

This is a repository for [OpenWrt](https://openwrt.org/) packages feed containing unmerged [**rrredir**](https://github.com/lars18th/rrredir.git) fork with inetd support.

#### Advanced (already setup OpenWrt sdk)
To use these packages, add the following line to your ```feeds.conf``` or ```feeds.conf.default``` in the OpenWrt buildroot:

```src-git extra https://github.com/lars18th/openwrt-extra.git```

Than include and install all packages from your ```feeds.conf```, while ensuring all extra packages are prefered via:
```
./scripts/feeds clean
./scripts/feeds update -a
./scripts/feeds uninstall -a
./scripts/feeds install -f -p extra -a
./scripts/feeds install -a
```

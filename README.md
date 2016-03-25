# mwlwifi-bin

Compiled packages for [mwlwifi project](https://github.com/kaloz/mwlwifi)

This project will keep tracking on mwlwifi project, compile latest driver for OpenWrt stable releases (currently it's both for 15.05 final and 15.05.1).

## How to install or upgrade

Simply `opkg install` it. No need to remove or delete anything.

## Step-by-step

Install git on your router:

```
opkg update
opkg install git-http
```

Clone the project:

```
cd /tmp
git clone --depth 1 https://github.com/NemoAlex/mwlwifi-bin.git
```

Install:

```
cd mwlwifi-bin/15.05
opkg install kmod-mwlwifi_3.18.20\+10.3.0.14-20151107-1_mvebu.ipk
```

Reboot your router:

```
reboot
```

Then done. Check the version of it:

```
strings /lib/modules/*.*/mwlwifi.ko | grep "^10.3"
```

If everything's OK, you will see the version number.

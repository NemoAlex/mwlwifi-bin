# mwlwifi-bin
Compiled packages for https://github.com/kaloz/mwlwifi

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

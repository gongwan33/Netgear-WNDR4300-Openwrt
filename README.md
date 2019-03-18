## Netgear-WNDR4300-Openwrt
WNDR4300 version of openwrt. Enlarge ubiroot to 113M

## Clone 
git clone git@github.com:gongwan33/Netgear-WNDR4300-Openwrt.git

## Checkout branch
git checkout openwrt-18.06 origin/openwrt-18.06

## feed installation
./scripts/feeds update -a

./scripts/feeds install -a

## Config
make menuconfig

* Target System => Atheros AR7xxx/AR9xxx
* Subtarget  => Generic devices with nand flash
* Target Profile => Netgear WNDR4300v1
* You may need LuCi Web admin interface. Please choose LuCi/Collections/luci

## make
make -j1 V=sc

(If you are in China, you may encounter some errors caused by GFW. Try to use a proxy to solve the problem.)

## Complete
The image will be in ./bin/targets/ar71xx/nand

For more information, please refer to https://geekwagner.blogspot.com/2019/03/compile-specific-openwrt-version-and.html

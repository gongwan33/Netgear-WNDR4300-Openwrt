## Netgear-WNDR4300-Openwrt/ZBT-WE1626 (Butterfly Router Home)
WNDR4300 version of openwrt. Enlarge ubiroot to 113M - branch openwrt-18.06

Support ZBT-WE1626 (Butterfly Router Home) - branch zbt-we1626

## Clone 
git clone git@github.com:gongwan33/Netgear-WNDR4300-Openwrt.git

## Checkout branch
### For Netgear WNDR4300
git checkout openwrt-18.06 origin/openwrt-18.06

### For ZBT-WE1626 (Butterfly Router Home)
git checkout zbt-we1626 origin/zbt-we1626

## feed installation
./scripts/feeds update -a

./scripts/feeds install -a

## Config
### For Netgear WNDR4300
make menuconfig

* Target System => Atheros AR7xxx/AR9xxx
* Subtarget  => Generic devices with nand flash
* Target Profile => Netgear WNDR4300v1
* You may need LuCi Web admin interface. Please choose LuCi/Collections/luci

### For ZBT-WE1626 (Butterfly Router Home)
make menuconfig

* Target System => MediaTek Ralinks MIPS
* Subtarget  => MT1620 based boards
* Target Profile => Zbtlink ZBT-WE1626
* You may need LuCi Web admin interface. Please choose LuCi/Collections/luci

## make
make -j1 V=sc

(If you are in China, you may encounter some errors caused by GFW. Try to use a proxy to solve the problem. Please refer to https://geekblog.mybluemix.net/ or https://geekwagner.blogspot.com/ for some possible solutions.)

## Complete
### For Netgear WNDR4300
The image will be in ./bin/targets/ar71xx/nand
### For ZBT-WE1626 (Butterfly Router Home)
The image will be in ./bin/targets/ramips/mt7620

For more information, please refer to https://geekwagner.blogspot.com/2019/03/compile-specific-openwrt-version-and.html

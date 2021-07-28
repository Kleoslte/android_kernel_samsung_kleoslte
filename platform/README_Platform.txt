How to build Module for Platform
- It is only for modules are needed to using Android build system.
- Please check its own install information under its folder for other module.

[Step to build]
1. Get android open source.
: version info - Android Kitkat 4.4.4_r1

( Download site : http://source.android.com )

2. Copy module that you want to build - to original android open source
If same module exist in android open source, you should replace it. (no 
overwrite)


# It is possible to build all modules at once.


3. You should add module name to 'PRODUCT_PACKAGES' in 'build\target\product\
core.mk' as following case.

case 1) libexifa : should add 'libexifa' to PRODUCT_PACKAGES
case 2) libjpega : should add 'libjpega' to PRODUCT_PACKAGES
case 3) ip6tables : should add 'ip6tables' to PRODUCT_PACKAGES
case 4) iptables : should add 'ip6tables' to PRODUCT_PACKAGES
case 5) e2fsck : should add 'e2fsck' to PRODUCT_PACKAGES
case 6) blkid : should add 'blkid' to PRODUCT_PACKAGES
case 7) libhyphenation : should add 'libhyphenation' to PRODUCT_PACKAGES
case 8) libwebcore : should add 'libwebcore' to PRODUCT_PACKAGES
case 9) core-junit : should add 'core-junit' to PRODUCT_PACKAGES
case 10) KeyUtils : should add 'libkeyutils' to PRODUCT_PACKAGES
case 11) brctl : should add 'brctl' to PRODUCT_PACKAGES
case 12) ebtables : should add 'ethertypes' and 'ebtables' to PRODUCT_PACKAGES

ex.) [build\target\product\core.mk] - add all module name for all follow cases at once

PRODUCT_PACKAGES += \
    libexifa \
    libjpega \
    ip6tables \
    iptables \
    e2fsck \
    blkid \
    libhyphenation \
    libwebcore \
    core-junit \
    libkeyutils \
    brctl \
    ethertypes \
    ebtables

4. excute build command
./build_platform.sh user





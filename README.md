# android_device_xiaomi_miuicamera-zeus

Build Xiaomi 12 Pro "zeus" along with MIUI camera.

### How to use?

Simply clone this repo to device/xiaomi/miuicamera-zeus as well as importing its vendor from Zeus-Junk-Yard repo to vendor/xiaomi/miuicamera-zeus:
```bash
# Execute this inside the build directory

git clone https://github.com/akrrac/android_device_xiaomi_miuicamera-zeus.git -b 14 device/xiaomi/miuicamera-zeus

# Import its vendor to vendor/xiaomi/miuicamera-zeus

git clone https://gitlab.com/zeus-junk-yard/android_vendor_xiaomi_miuicamera-zeus.git -b 13 vendor/xiaomi/miuicamera-zeus
```

Then, include these trees inside **lineage_zeus.mk** or **awaken_zeus.mk** etc. (depending on which custom ROM you are building with):
```mk
# Miui Camera for zeus

$(call inherit-product, device/xiaomi/miuicamera-zeus/device.mk)
$(call inherit-product, device/xiaomi/miuicamera-zeus/BoardConfig.mk)
```

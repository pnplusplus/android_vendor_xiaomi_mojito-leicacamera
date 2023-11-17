## Leica Camera Configuration for Redmi Note 10

### How to?

1. Add this line to your BoardConfig.mk
```
BUILD_BROKEN_DUP_RULES := true
BUILD_BROKEN_ELF_PREBUILT_PRODUCT_COPY_FILES := true
```
```
# Inherit from proprietary files for Leica Camera
-include vendor/xiaomi/mojito-leicacamera/BoardConfigVendor.mk
```
2. And this line to your device.mk
```
# Call the Leica Camera setup
$(call inherit-product-if-exists, vendor/xiaomi/mojito-leicacamera/mojito-leicacamera-vendor.mk)
```
3. Clone this repository to vendor/xiaomi/mojito-leicacamera
4. Apply necessary *.patch in patch folder to respective ROM sources folder and enjoy! (Search in Google if you don't know how to apply a *.patch)

### Source
- https://xdaforums.com/t/useful-mods-for-custom-roms-mojito-sunny.4494371/

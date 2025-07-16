Copyright (C) 2021-2025 DerpFest

Device configuration for Xiaomi Redmi Note 10 Pro/Pro Max
=========================================

The Xiaomi Redmi Note 10 Pro/Pro Max (codenamed _"sweet"_) is a mid-range smartphone from Xiaomi.

It was announced in March 2021.

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Dual-core 2.3 GHz Kryo 470 Gold & Hexa-core 1.8 GHz Kryo 470 Silver
Chipset | Qualcomm SM7150 Snapdragon 732G
GPU     | Adreno 618
Memory  | 6/8 GB RAM
Shipped Android Version | 11.0
Storage | 64/128 GB (UFS 2.2)
Battery | Non-removable Li-Po 5020 mAh
Display | 1080 x 2400 pixels, 6.67 inches (~395 ppi pixel density)
Camera  | 64/108 MP wide camera, 8MP ultra wide-angle camera, 5MP macro camera, 2MP depth camera, LED flash

## DerpFest Build Instructions

To build DerpFest for sweet:

```bash
# Initialize DerpFest source
repo init -u https://github.com/DerpFest-AOSP/manifest.git -b 14
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

# Clone device tree
git clone https://github.com/DerpFest-Devices/device_xiaomi_sweet.git -b 14 device/xiaomi/sweet

# Clone common tree (if needed)
git clone https://github.com/DerpFest-Devices/device_xiaomi_sm6150-common.git -b 14 device/xiaomi/sm6150-common

# Clone vendor blobs
git clone https://github.com/DerpFest-Devices/vendor_xiaomi_sweet.git -b 14 vendor/xiaomi/sweet
git clone https://github.com/DerpFest-Devices/vendor_xiaomi_sm6150-common.git -b 14 vendor/xiaomi/sm6150-common

# Setup environment
source build/envsetup.sh
lunch derp_sweet-userdebug

# Build
mka derp
```

## Device picture

![Xiaomi Redmi Note 10 Pro/Max](https://cdn.dxomark.com/wp-content/uploads/medias/post-79073/Xiaomi-Redmi-Note-10-Pro-_Yoast-image-packshot-review.jpg)

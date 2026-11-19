# android_manifest_x6886-a16

Local manifest for building the Infinix X6886 (MT6789) trees on LineageOS 24.0.

## Usage

```
repo init -u https://github.com/LineageOS/android -b lineage-24.0
repo sync -c
mkdir -p .repo/local_manifests
curl -L -o .repo/local_manifests/x6886.xml \
  https://raw.githubusercontent.com/BeruCrypt02/android_manifest_x6886-a16/Manifest.Lineage.24.0/x6886.xml
repo sync -c
```

## Projects

| Path | Repo | Revision |
|---|---|---|
| device/infinix/x6886 | BeruCrypt02/android_device_infinix_X6886-a16 | lineage-24.0 |
| vendor/infinix/x6886 | BeruCrypt02/android_vendor_infinix_X6886-a16 | lineage-24.0 |
| device/infinix/x6886-prebuilts | BeruCrypt02/android_device_transsion_infinix_X6886-prebuilts | main |
| hardware/mediatek | LineageOS/android_hardware_mediatek | lineage-24.0 |
| device/mediatek/sepolicy_vndr | LineageOS/android_device_mediatek_sepolicy_vndr | lineage-24.0 |
| hardware/transsion | mt6789-transsion/hardware_transsion | lineage-23.0 |
| vendor/mediatek/ims | malachite-project/android_vendor_mediatek_ims | lineage-24.0 |

The vendor, prebuilts and IMS projects use `clone-depth="1"` to keep the sync small.

`hardware/google/interfaces`, `hardware/google/pixel*` and `hardware/lineage/compat` come from the LineageOS default manifest; do not add duplicates.

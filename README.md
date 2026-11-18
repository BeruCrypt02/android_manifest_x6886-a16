# android_manifest_x6886-a16

Local manifest for building the Infinix X6886 (MT6789) trees.

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

| Path | Repo | Revision | Notes |
|---|---|---|---|
| device/infinix/x6886 | BeruCrypt02/android_device_infinix_X6886-a16 | lineage-24.0 | device tree |
| vendor/infinix/x6886 | BeruCrypt02/android_vendor_infinix_X6886-a16 | lineage-24.0 | vendor blobs |
| device/infinix/x6886-prebuilts | BeruCrypt02/android_device_transsion_infinix_X6886-prebuilts | main | kernel prebuilts |
| hardware/mediatek | LineageOS/android_hardware_mediatek | lineage-24.0 | MT6789 HALs |
| device/mediatek/sepolicy_vndr | LineageOS/android_device_mediatek_sepolicy_vndr | lineage-24.0 | MTK sepolicy |
| hardware/transsion | mt6789-transsion/hardware_transsion | lineage-23.0 | Transsion HALs; no lineage-24.0 branch exists yet |
| vendor/mediatek/ims | mmetem55/android_vendor_mediatek_ims | android-17 | IMS |
| vendor/infinity | ProjectInfinity-X/vendor_infinity | 16 | common_full_phone.mk for `infinity_X6886` |

`hardware/google/interfaces`, `hardware/google/pixel*` and `hardware/lineage/compat` come from the LineageOS default manifest; do not add duplicates.

## Notes

- `hardware/transsion` only ships `lineage-23.0`; compatibility with lineage-24.0 is unverified.
- Stock dump carries its own Dolby stack (`vendor.dolby.dms@2.0`, `libcodec2_store_dolby`, `vendor.dolby.media.c2-default-service-dax`, `vendor.dolby.dms.service`) which is not yet in the vendor tree. Wiring Dolby is a separate decision; it is not in this manifest.

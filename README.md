# TWRP for Amazon Kindle eInk ereader devices
### State
TWRP builds and is fully functional (hopefully).

### Known working devices
- Kindle Basic 8th Generation (kt3)

### Installation
1) use my modified u-boot and enter fastboot;
2) in cmd do `fastboot flash recovery <path_to_recovery_image>`

### How to enter recovery
TODO

### How to enter fastboot
TODO

### How to build TWRP
1. `repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-5.1`
2. `repo sync`
3. `clone this repo to <twrp_repo>/device/amazon/eanab`
4. apply patches from `<twrp_repo>/device/amazon/eanab/patches` directory
5. open terminal in `<twrp_repo>` directory;
6. `. build/envsetup.sh`
7. `lunch omni_eanab-userdebug`
8. `mka recoveryimage`

if you want to enable A2 mode:
1. uncomment `TW_IMX_EINK_MONOCHROME` in `BoardConfig.mk`

if everything is successful you should find built recovery by path <twrp_repo>/out/target/product/eanab/recovery.img

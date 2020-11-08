# Basic Bringup and Sync device source

Files to change for AOSP Android 10 Bringup
* AndroidProducts.mk
* romname_devicecodename.mk (eg: lineage_tulip.mk)

Example Bringup Commits:

Bringup for DU: 
https://github.com/AtlanPrime/decommonised_device_xiaomi_miatoll/commit/7077b40c32f45f730bbf3604375b5a8a7a1dc39b

Here, all you have to do is edit the AndroidProducts.mk file and romname_devicecodename.mk according to
the rom u want to build.
Use the example commit as a reference

We can either do the bringup locally on any low spec pc or after syncing the trees within the source too!

for that clone the trees to the specific folders as shown in example below:

```bash
#Enter the synced ROM's directory
cd lineage

#Clone the device tree
git clone https://github.com/xiaomi-sdm660/android_device_xiaomi_tulip -b ten device/xiaomi/tulip

here the text after "-b" defines the branch you want to clone, if no branch is specified
the default branch will be synced and the text after branch name, "device/<manufacturer>/<codename>", 
specifies the location to clone it to.

#Clone the common device tree if it exists
git clone https://github.com/xiaomi-sdm660/android_device_xiaomi_sdm660-common -b ten device/xiaomi/sdm660-common

#Clone the kernel tree
git clone https://github.com/xiaomi-sdm660/android_kernel_xiaomi_sdm660 -b 10.0-eas kernel/xiaomi/sdm660

#Clone the vendor tree
Sometimes devs decides to put the common vendor tree and vendor tree in a single repo..
so it would be vendor_xiaomi..
but in this specific case we have the vendor and the common vendor tree as seperate repos so..

git clone https://github.com/xiaomi-sdm660/android_vendor_xiaomi_sdm660-common vendor/xiaomi/sdm660-common

git clone https://github.com/xiaomi-sdm660/android_vendor_xiaomi_tulip vendor/xiaomi/tulip

notice that I did not specify branches here, because the default one will be synced!
```


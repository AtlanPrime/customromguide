#Downloading a ROM Source

* This is important to do before cloning the device specific trees

Some Popular ROMs

* [**DirtyUnicorns**](https://github.com/DirtyUnicorns)
* [**LineageOS**](https://github.com/LineageOS)
* [**AOSPA**](https://github.com/AOSPA)

Find the GitHub org of the ROM you need to build and sync it like shown below

```bash
# we need to make a folder for the ROM first (Example LineageOS)
mkdir Lineage

# Connect your Github account.
git config --global user.name "FIRST_NAME LAST_NAME" git config --global user.email "YOUR EMAIL"

# Go to ROM folder.
cd lineage

# Now we need to initialize LineageOS Source
# For that, go the LineageOS git and find the manifest (https://github.com/LineageOS/android this may vary from ROM to ROM)
# Choose the Branch (this is actually the version of android)
# Let's choose Android 10, so as an example the branch here would be "lineage-17.1"

# So it goes like:
repo init -u git://github.com/LineageOS/android.git -b lineage-17.1

# And to Sync it
repo sync
```

This would actually depend on your internet speed.. the size of the LineageOS repo would be around 60GB or more, probably

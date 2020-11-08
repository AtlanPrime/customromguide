# Lets build it!

Instructions to build are pretty straight and most of the time it's specified in the manifest (android- in case of lineageos)

* First thing to do is set up build enviromnent

```bash
. build/envsetup.sh
```

* Now we need to lunch

"lunch lineage_$device-userdebug",
"lunch lineage_$device-eng",
"lunch lineage_$device-user" 

These are the three types of lunch commands..
"userdebug" is the normal lunch type for release builds
"eng" is an even more deuggable version

In our case we use userdebug, so

```bash
lunch lineage_tulip-userdebug
```

* Now, to start building we use,

```bash
mka bacon
```

# Now wait till the rom is compiled!
# Happy Waiting!

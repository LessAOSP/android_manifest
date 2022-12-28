![](LESSAOSP.png)

# HOW TO BUILD LESSAOSP ROM?

create a directory called as **lessaosp**

## Initialize local repository inside lessaosp folder
```## Initialize local repository
repo init -u https://github.com/LessAosp/android_manifest -b Thirteen
```

## For users below 250GB Storage Limit use below shallow clone to save some space
```## for users below 250GB use below shallow clone 
repo init -u https://github.com/LessAosp/android_manifest -b Thirteen --depth=1
```
## Sync
```## Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
# Build Process
```## Set up environment
. build/envsetup.sh
```

## Choose a target
```## Choose a target
lunch aosp_$device-userdebug
```
## Build the code
```## Build the code
make bacon -jX
```
# Credits
* [LineageOS](https://github.com/LineageOS)
* [PixelExperience](https://github.com/PixelExperience)
* [Project-Elixir](https://github.com/Project-Elixir)
* [ArrowOS](https://github.com/ArrowOS)
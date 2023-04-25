# local-manifest

### Create a directory for the source files

* You can name this directory however you want, just remember to replace
* WORKSPACE with your directory for the rest of this guide.
* This can be located anywhere (as long as the fs is case-sensitive)
```
mkdir WORKSPACE
```
```
cd WORKSPACE
```

### Install Repo in the created directory
```bash
repo init -u https://github.com/The-Bot-BB/local-manifest.git main
```
### shallow clone
```
repo init --depth=1 -u https://github.com/The-Bot-BB/local-manifest.git b main
```

### Download the source
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Set up environment for Build
```
. build/envsetup.sh
```
### Choose a target
```
lunch aosp_$device-userdebug
```
### Build the code
```
mka bacon -jX
```

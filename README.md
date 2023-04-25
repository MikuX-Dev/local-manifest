# local-manifest

To get started, you'll need to get
familiar with [Repo](https://source.android.com/source/using-repo.html) and [Version Control with Git](https://source.android.com/source/version-control.html).
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
repo init -u https://github.com/The-Bot-BB/local-manifest.git -b main
```
### shallow clone
```
repo init --depth=1 -u https://github.com/The-Bot-BB/local-manifest.git -b main
```

### Download the source
```bash
repo sync --no-clone-bundle -jX
```

### Set up environment for Build
```
source build/envsetup.sh
```
### Choose a target
```
lunch lineage_$device-userdebug
```
### Build the code
```
mka eos -jX
```

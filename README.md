BotOS
=====

Getting started
---------------

To get started with BotOS, you'll need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).

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
repo init -u https://github.com/The-Bot-BB/manifest.git -b BotOS-1.0
```

### Download the source
```bash
repo sync 
```

### Set up environment for Build
```
. build/envsetup.sh
```
### Choose a target
```
lunch lineage_$device-userdebug
```
### Build the code
```
mka eos -jX
```

Please see the [/e/ documentation](https://doc.e.foundation/how-tos/#build-e-for-a-device) for building instructions, by device.

please note this is based on [/e/os](https://e.foundation/e-os/)
=================================================================

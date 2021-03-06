# firefox-flatpak
This is a set of patches, scripts and a manifest to build latest Firefox using Flatpak. It is using GNOME 3.22 as base runtime.

# Usage

Run ```./setup_runtime.sh``` to download and install GNOME 3.20 SDK and GNOME 3.22 SDK for Flatpak.

Currently there are three builds available:
* org.mozilla.FirefoxNightly - to build latest nightly
* org.mozilla.FirefoxNightlyWayland - to build nightly with wayland support
* org.mozilla.FirefoxDevEdition - Firefox Developer Edition (branded aurora build)

To build specific build run:
```
./build.sh BUILD_NAME
```
for example 
```
./build.sh org.mozilla.FirefoxNightly
``` 
will build Firefox from master branch.

After the build is finished you can install the app by:
```
./install.sh BUILD_NAME
```

To start Firefox use:
```
flatpak run BUILD_NAME
```

For example:
```
flatpak run org.mozilla.FirefoxNightly
```

# Repository

Created repository with some additional instructions can be found there: https://firefox-flatpak.mojefedora.cz/

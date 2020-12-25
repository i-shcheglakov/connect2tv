# connect2tv
The tool simplifies RPM package deployment for Tizen devices.

The workflow is to build with `gbs` and install RPMs on a target device with `connect2tv vnc`, `rdp` or `knox`.
To specify IP address of the target device use `-i=<addr>` option.
To explicitly specify package directory use `-d=<directory>` option.
If no directory specified it defaults to RPMs directory of currently active `gbs` profile.

Usage:
```
connect2tv [-i=<addr>] [-d=<directory] [-v=<version>] [vnc|rdp|knox]
```

## Install
```
sudo make install
```
Default installation path is `/usr/local/bin`. The symbolic link is created.

To uninstall:
```
sudo make uninstall
```
## Usage examples
Install `knox` packages to the target device:
```
connect2tv -i=192.168.1.127 knox
```
Connect only:
```
connect2tv
```
See `--help` for available options.

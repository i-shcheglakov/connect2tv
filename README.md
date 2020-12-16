# connect2tv
The tool simplifies RPM package deployment for Tizen devices. It automatically discovers
IP address of the target device based upon currently active GBS profile in `~/.gbs.conf` and re-installs `vnc`, `rdp` or `knox` packages.

Default workflow is to build using `gbs` and install artifacts on a target device with `connect2tv vnc`, `rdp` or `knox`.
To explicitly specify IP address of the target device use `-i=<addr>` option.

Usage:
```
connect2tv [-i=<addr>] [-p=<profile>] [-d=<directory] [-v=<version>] [vnc|rdp|knox]
```

## Install
Clone repository to `/path/to/the/repo`.
```
cd /path/to/the/repo
sudo make install
```
Default installation path is `/usr/local/bin`.

To uninstall:
```
sudo make uninstall
```
In order to fetch the most recent updates use `git pull`.

## Usage examples
Copy knox packages to the target device:
```
connect2tv knox
```
Connect only:
```
connect2tv
```
See `--help` for available options.

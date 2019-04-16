# connect2tv
The script simplifies B2B development workflow. It automatically discovers
IP address of the target device based upon currently active GBS profile in `~/.gbs.conf` and re-installs `vnc` or `rdp` packages.

Default workflow is to build using `gbb` and copy artifacts using `connect2tv vnc` or `rdp`.
To explicitly specify IP address of the target device use `-i=<addr>` option.

Usage:
```
connect2tv [-i=<addr>] [-p=<profile>] [vnc|rdp]
```

## Install
Clone repository to `/path/to/the/repo` and create symbolic link in `~/.local/bin` to the script:
```
mkdir -p ~/.local/bin
ln -s /path/to/the/repo/connect2tv ~/.local/bin/connect2tv
```
Make sure `~/.local/bin` is in `$PATH`:
```
echo '$PATH=$HOME/.local/bin:$PATH' >> $HOME/.bashrc
source $HOME/.bashrc
```
In order to fetch the most recent updates use `git pull`.

## Usage examples
Copy VNC or RDP packages to the target device:
```
connect2tv vnc
```
Connect only:
```
connect2tv
```
See `--help` for available options.

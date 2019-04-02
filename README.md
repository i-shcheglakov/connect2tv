# connect2tv
The script simplifies B2B development workflow. It automatically discovers
currently active GBS profile in `~/.gbs.conf` and IP address of the target device accordingly.

The default workflow is to build using `gbb` and copy artifacts using `connect2tv vnc` or `rdp`. To directly specify IP address of the target device use `--ip-addr` option.

## Install
Clone repository:
```
git clone https://github.sec.samsung.net/i-shcheglako/connect2tv.git /path/to/the/script
```
Create symbolic link to the script:
```
mkdir -p ~/.local/bin
ln -s /path/to/the/script ~/.local/bin/connect2tv
```
Make sure `~/.local/bin` is in `$PATH`:
```
echo '$PATH=$HOME/.local/bin:$PATH' >> $HOME/.bashrc
source $HOME/.bashrc
```
In order to fetch recent updates use `git pull`.

## Usage examples
Copy VNC or RDP packages to the target device:
```
connect2tv vnc
```
Connect only, no copying:
```
connect2tv --connect-only
```
See `--help` for available options.

# connect2tv

## Install
Create symbolic link to the script:
```
ln -s /path/to/the/script ~/.local/bin/connect2tv
```
Make sure that the destination is in `$PATH`:
```
echo '$PATH=$HOME/.local/bin:$PATH' >> $HOME/.bashrc
source $HOME/.bashrc
```

## Usage example
```
connect2tv --connect-only
```
See `--help` for available options.

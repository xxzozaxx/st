# Ahmed's build of st (aka suckless\simple Terminal)

Forked form [luck smith](https://github.com/LukeSmithxyz/st) which is Forked from [shiva](https://github.com/shiva/st), which is the [suckless terminal (st)](https://st.suckless.org/) with some additional features:

+ Copy to clipboard (C-M-c), and past from it (C-M-v)
+ Zoom in/out with C-M-(k/j) or (u/d) for larger intervals.
+ Optional colors, using [terminal.sexy](http://terminal.sexy/)

The following additional bindings were added before I forked this:


+ Scroll through history -- Shift+PageUp/PageDown or Shift+Mouse wheel
+ Increase/decrease font size -- Shift+Alt+PageUp/PageDown
+ Return to default font size -- Shift+Alt+Home
+ Paste -- Shift+Insert
+ updated to latest version 0.8.1

## Installation for newbs

```
make
sudo make install
```

Obviously, `make` is required to build. `fontconfig` is required for the
default build, since it asks `fontconfig` for your system monospace font.  It
might be obvious, but `libX11` and `libXft` are required as well. Chances are,
you have all of this installed already.

On OpenBSD, be sure to edit `config.mk` first and remove `-lrt` from the
`$LIBS` before compiling.
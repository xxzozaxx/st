# Ahmed's build of st (aka suckless Terminal) with Monochrome theme

Forked form [luck smith](https://github.com/LukeSmithxyz/st) which is Forked from [shiva](https://github.com/shiva/st), which is the [suckless terminal (st)](https://st.suckless.org/) with some additional features:

+ Copy to clipboard (C-M-c), and past from it (C-M-v)
+ Zoom in/out with C-M-(k/j) or (u/d) for larger intervals.
+ Optional Monochrome colors, using [terminal.sexy](http://terminal.sexy/)

The following additional bindings were added before I forked this:

+ Compatibility with `Xresources` and `pywal` for dynamic colors
+ Default font is system "mono" at 14pt, meaning the font will match your system font.
+ Hold Alt and press either ↑/↓ or the vim keys k/j to move up/down in the terminal.
+ Shift+Mouse wheel will as well.
+ Vertcenter
+ Alt-PageUp and Alt-PageDown will do the same.
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

Obviously, `make` is required to build. `fontconfig` is required for the default build, since it asks `fontconfig` for your system monospace font.  It might be obvious, but `libX11` and `libXft` are required as well. Chances are, you have all of this installed already.

## Custom changes (`config.def.h` or `config.h`)

Now by default, the terminal is transparent and uses an Xresources patch that
looks for your Xresources colors for the colors of st. You can disable the
Xresources patch by reversing it as below:

```
patch -R < xresources.patch
```

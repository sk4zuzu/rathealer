rathealer
=========

Simple mousewheel binding solution for rxvt-unicode terminal emulator.

Let's consider a typical *urxvt* setup with [urxvt-font-size] module enabled:

```
urxvt.font:           xft:Monaco:pixelsize=18
urxvt.boldFont:       xft:Monaco:pixelsize=18
urxvt.italicFont:     xft:Monaco:pixelsize=18
urxvt.boldItalicFont: xft:Monaco:pixelsize=18

urxvt.iso14755:    false
urxvt.iso14755_52: false

urxvt.perl-ext-common: default,font-size,rathealer
urxvt.keysym.C-Up:     perl:font-size:increase
urxvt.keysym.C-Down:   perl:font-size:decrease
urxvt.font-size.step:  2

urxvt.rathealer.modifier:     C-
urxvt.rathealer.button_up:    4
urxvt.rathealer.button_down:  5
urxvt.rathealer.keycode_up:   111
urxvt.rathealer.keycode_down: 116
```

Such standard setup allows only for binding keyboard shortcuts.  
Rathealer allows you to translate mousewheel up/down motion to normal keyboard shortcuts.

In the example above wheelup (Pointer\_Button4) is being translated to Up (keycode 111) and wheeldown (Pointer\_Button5) to Down (keycode 116) with Control key (C-) as a modifier. The result is dynamic resize of *urxvt's* window on demand with mousewheel.

Installation
------------

Just copy the ```rathealer``` perl module file to *urxvt's* module directory and reconfigure your ```~/.Xdefaults ``` or ```~/.Xresurces``` file.

[urxvt-font-size]:https://github.com/majutsushi/urxvt-font-size


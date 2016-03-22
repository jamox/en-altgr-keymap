This repository contains a keymap for US keyboards that enables the following:

    AltGr+A -> ä
    AltGr+O -> ö
    AltGr+U -> ü
    AltGr+S -> š
    (plus the capitalized versions)

## X11 installation

Drop the file into `/usr/share/X11/xkb/symbols` (or the equivalent in your distro). Select it with `setxkbmap ee_altgr`.

## Windows installation

Use the Microsoft Keyboard Layout Creator to compile the klc file or [download the compiled package](http://goo.gl/h7jTOJ).



TODO: reloading w/o root could maybe be done (I have't tried this yet):
> setxkbmap -device $remote_id -print|sed 's/\(xkb_symbols.*\)"/\1+custom([layout])"/' | xkbcomp -I[path] -i $remote_id -synch - $DISPLAY 2>/dev/null    
>#remote_id on muuttuja, jossa on se näppäimistön id jolle ton haluaa applyttää [ainakin toimii tolla skriptillä joka mul on; path alla on hakemisto symbols, jossa on layoutkuvauksia

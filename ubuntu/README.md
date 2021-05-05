Using Ubuntu
-----------

Add it to you systems keyboard and restart your computer.

```
cp real-prog-dvorak >> ~/.config/xkb/real-prog-dovark
```

Then you have to update the `sudo vim /usr/share/X11/xkb/rules/evdev.xml` with the following, add it near the other English keyboards

```
<variant>
    <configItem>
        <name>real-prog-dvorak</name>
        <description>English (Real Programmers Dvorak)</description>
        <vendor>MichaelPaulson</vendor>
    </configItem>
</variant>
```


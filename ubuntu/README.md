Using Ubuntu
-----------

Add it to you systems keyboard and restart your computer.

```
cat real-prog-dvorak >> /usr/share/X11/xkb/symbols/us
```

Then you have to update the evdev.xml with the following, add it near the other English keyboards

```
<variant>
    <configItem>
        <name>real-prog-dvorak</name>
        <description>English (Real Programmers Dvorak)</description>
    </configItem>
</variant>
```


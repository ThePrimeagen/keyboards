## Using Ubuntu

Add it to your systems keyboard and restart your computer.

```
cp real-prog-dvorak ~/usr/share/X11/xkb/symbols/real-prog-dovark
```

Then you have to update the `sudo vim /usr/share/X11/xkb/rules/evdev.xml` with the following, add it inside the `<layoutList>` tag. After that you have to restart your computer. After that the layout should be available in the keyboard settings. `Settings > Keyboard > Input Sources > + > English (Real Programmers Dvorak)`

```
<layout>
  <configItem>
    <name>real-prog-dvorak</name>
    <shortDescription>Real Programmers Dvorak</shortDescription>
    <description>English (Real Programmers Dvorak)</description>
    <languageList>
      <iso639Id>eng</iso639Id>
    </languageList>
  </configItem>
  <variantList/>
</layout>

```

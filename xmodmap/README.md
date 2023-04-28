Using Xmodmap
-----------

Put the xmodmap file anywhere on your system and run 

``` 
xmodmap path_to_xmodmap
```
To start it with the X server put the command into your ~/.xinitrc or your ~/.xprofile

Alternative
------------

On some systems, xmodmap with this particular layout can be slow.
A certain user (André Kugland) explains why in a stackexchange discussion: 
> When xmodmap runs, it calls XChangeKeyboardMapping once for each key it modifies, which generates MappingNotify events. 
> In some configurations (mine included), this burst of events causes the system to hang for some time

Using the script he answered the question with, I generated the corresponding output after setting my own layout using `xmodmap real-prog-dvorak` beforehand.
The output itself is also a script that can be, in turn, compiled into an executable that changes the layout automatically without generating all those events.

You can compile the script with the command `gcc <file> -lX11`

Afterwards you can run this script with your X server just like above.

[discussion link](https://unix.stackexchange.com/questions/94336/xmodmap-hanging-the-system-for-20-secs-and-not-sticking)

# Gdebi-Ubuntu-26.04-Wayland-Fix
If Gdebi is crashing after entering password via pxexec, this simple edit will fix it.


Step 1: Open terminal

Step 2: Open gdebi desktop file

```
sudo nano /usr/share/applications/gdebi.desktop
```

Step 3: edit Exec= line

```
Exec=sh -c "pkexec env DISPLAY=$DISPLAY XAUTHORITY=$XAUTHORITY gdebi-gtk %f"
```

Step 4: Save and done.

Now it will work as it always has. Hope this helped you :)

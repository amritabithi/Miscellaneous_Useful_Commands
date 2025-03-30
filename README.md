# Miscellaneous Useful Commands
### These are some commands which are useful but do not deserve a dedicated repository.
<br>
<br>
<b>Change your monitor's screen brightness using a shell script:</b>
<br>
<i>Shell script contents:</i><br>

```sudo xrandr --output DVI-D-0 --brightness $1```
<br>
<i>Usage ( this example sets monitor to 50% brightness ):</i>
<br>
```sudo bash brightness 0.5```

<br>
<b>Set your computer's clock using the time returned by Google's page header:</b>

```sudo date -s "$(wget -qSO- --max-redirect=0 google.com 2>&1 | grep Date: | cut -d' ' -f5-8)Z";```

<b>Update the hardware clock to match the system time:</b>
<br>
```sudo hwclock -w;```

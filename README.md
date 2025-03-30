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
<b>Setting your computer's time:</b>
<br>
<i>Set your computer's clock using the current time returned by Google's page tags:</i>

```sudo date -s "$(wget -qSO- --max-redirect=0 google.com 2>&1 | grep Date: | cut -d' ' -f5-8)Z";```
<i>Update the hardware clock to match the system time:</i>
<br>
```sudo hwclock -w;```

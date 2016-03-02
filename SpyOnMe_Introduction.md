# Introduction #

This is tiny python script that takes screenshots in predefined interval and saves them in predefined directory.
Screenshots are identified by timestamp (f.e. 10-03-25\_10:33:57.jpg).
Execution of the script doesn't disturb you at work at all, though If your box is old enough there might be some lags visible (f.e. during games).

This is in early stage of development, thougt basic functionality is there and working. Contact me if you have any specific request for further functionality...

# Installation and running #

No installation needed and possible. Copy the script elsewhere, check/edit few parameters inside the script and make it run. Prefferrably from withing GUI/Xserver. Otherwise you will have to play with DISPLAY variable (I did not tested this scenario)

# Issues #

**- No delete-old-screenshots functionality (yet), keep it in your mind**


**- (Elimination of) annoying beeps**

xwd command (this is what is doing the screenshot ) triggers quite annoying pc speaker beeps.<br>
To eliminate them:<br>
<ol><li>check the module pcspkr is loaded:<br>
</li></ol><blockquote>$lsmod | grep pcspkr<br>
If it is:<br>
2. rmmod pcspkr # as temporary soluction<br>
3. add "blacklist pcspkr" line to your /etc/modprobe.d/blacklist file as permanent solution<br></blockquote>

If not... than the module might be compiled directly to kernel and I'm not sure what to do with this... (:
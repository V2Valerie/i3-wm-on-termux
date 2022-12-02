# i3-wm-on-termux
i3-wm on termux with vnc

# Step 1
I'm hoping that you already have Termux installed, 
so we need few things installed, we need client app, 
you can install whatever client you would like, 
my recommendation is AVNC, you can either get it from Play-store or F-droid.

# Step 2
So now we open Termux and install these applications,
```bash

apt install tigervnc
apt install i3
apt install dmenu
apt install xfce4-terminal
```
we are mostly done, you can install rofi instead of dmenu and install whatever terminal emulator you like.

# Step 3
now in your termux, cd to .vnc directory, 
then with nano or vim open xstartup, first we need to comment few things, if you have something like, <br>
twm & <br>
fluxbox & <br>
fluxbox-generate_menu <br>
just comment them, <br>
after that add this line,
```bash
i3 &
```
and save the file and exit.

# Step 4
now final step, <br>
start vnc server with this command
```bash
vncserver
```
its gonna ask you for a password, then open AVNC and hit + sign, give your server a name, host is going to be 127.0.0.1 with 5901 port,
then your username, if you dont know your username go back to termux and use whoami command to find your username, 
and give your password and your done ,hit your server and enjoy

# Few extra things
to kill server
```bash
vncserver -kill localhost:1
```
to change resolution
```bash
vncserver -geometry 800X400
```
# Thank you for reading
if you found this tutorial useful please give it a start, thank you again.

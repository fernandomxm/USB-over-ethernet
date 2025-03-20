# USB-over-ethernet
USB over ethernet
<br>
USBIP (usbip.sourceforge.net)<br>
<br>
WIN 172.27.160.1 (SERVER WINDOWS) <br>
usbipd list <br>
usbipd bind --busid=2-3 <br>
<br>
KALI 172.27.170.237 (CLIENT KALI LINUX) <br>
usbip list --remote=172.27.160.1 <br>
usbip attach --remote=172.27.160.1 --busid=2-3 <br>
lsusb

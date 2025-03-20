# USB-over-ethernet
USB over ethernet

USBIP (usbip.sourceforge.net)

WIN 172.27.160.1 (SERVER WINDOWS)
usbipd list
usbipd bind --busid=2-3

KALI 172.27.170.237 (CLIENT KALI LINUX)
usbip list --remote=172.27.160.1
usbip attach --remote=172.27.160.1 --busid=2-3
lsusb

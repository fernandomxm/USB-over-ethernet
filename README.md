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
modprobe vhci_hcd <br>
usbip list --remote=172.27.160.1 <br>
usbip attach --remote=172.27.160.1 --busid=2-3 <br>
lsusb <br>
 <br>
Extra problem scan wifi: <br>
- vim /usr/share/polkit-1/actions/org.freedesktop.NetworkManager.policy <br>
- Alterar linha (<allow_any> yes</allow_any> abaixo do id=org.freedesktop.NetworkManager.wifi.scan <br>
- systemctl restart polkit.service <br>
- pkaction --verbose --action-id org.freedesktop.NetworkManager.wifi.scan <br>
  (implicit any: yes) <br>
![USBIP](https://github.com/fernandomxm/Migrate-EC2-AWS-to-OCI/blob/main/image01.png)

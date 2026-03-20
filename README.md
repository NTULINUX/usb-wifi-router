# USB Wi-Fi Router for SystemD

NetworkManager must be stopped and disabled

Reboot required because NetworkManager will still be hogging port 53

Required services to start:

 - wpa_supplicant.service
 - dhcpcd.service
 - hostapd.service
 - dnsmasq.service

This configuration assumes you want to connect via DHCP
for the external network on a USB device while hosting
a private Wi-Fi router on another USB interface, with it's own DHCP server.

# USB Wi-Fi Router for SystemD

NetworkManager must be stopped and disabled

Reboot required because NetworkManager will still be hogging port 53

Packages required:

 - wpa_supplicant
 - dhcpcd
 - hostapd
 - dnsmasq
 - nftables (nftables-services for Fedora)
 - openresolv

Packages to remove:

 - firewalld
 - systemd-resolved

Required services to start:

 - wpa_supplicant.service
 - dhcpcd.service
 - hostapd.service
 - dnsmasq.service

This configuration assumes you want to connect via DHCP
for the external network on a USB device while hosting
a private Wi-Fi router on another USB interface, with it's own DHCP server.

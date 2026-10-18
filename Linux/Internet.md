### Add a connection to an enterprise Wlan (WPA2 Enterprise)
`nmcli con add type wifi ifname wlo1 con-name <chosen_Name> ssid <ssid_thing> wifi-sec.key-mgmt wpa-eap 802-1x.eap peap 802-1x.phase2-auth mschapv2 802-1x.identity "[it251508@fhstp.ac.at](mailto:it251508@fhstp.ac.at)" 802-1x.password "Password"`

#### Tailscale things
`tailscale up --accept-routes` accept adverticed routes with every CIDR
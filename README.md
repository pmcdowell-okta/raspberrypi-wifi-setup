# Raspberry PI Wifi Setup

This is a script that **Enables ssh** and create the **`wpa_supplicant.conf`** file
required to join a Wifi network.

# Run Script

After you image you Raspberry PI disk, just mount the SD Micro card,
and open a Terminal console, navigate to the /boot directory

For example: on my MacOs the directory is `/Volumes/boot`

Then paste this script into the Terminal window.

```
touch ssh
cat << EOF > wpa_supplicant.conf
country=us
update_config=1
ctrl_interface=/var/run/wpa_supplicant

network={
 scan_ssid=1
 ssid="your_network"
 psk="your_password"
 }
 EOF
```

# Uploads pcap files automaticly to banthex.de like the wpa-sec plugin

1. SSH into your Pwnagotchi and create a new folder for third-party Pwnagotchi plugins. I use `/root/custom_plugins/` but it doesn't really matter: `mkdir /root/custom_plugins/`
1. Grab the `display-password-banthex.py` and `display-password-banthex.toml` file from this Github repo and put it into that custom plugins directory.
1. Edit `/etc/pwnagotchi/config.toml` and change the `main.custom_plugins` variable to point to the custom plugins directory you just created: `main.custom_plugins = "/root/custom_plugins/"`
1. In the same `/etc/pwnagotchi/config.toml` file, add the following lines to enable the plugin:
```
main.plugins.display-password-banthex.enabled = true
main.plugins.display-password-banthex.orientation = "horizontal"
```
Once the above steps are completed, reboot the Pwnagotchi to ensure all changes are applied.

# Screenshot:

![banthex.py](/screenshot.png?raw=true "banthex.py")

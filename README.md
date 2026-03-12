# Local Pihole DNS Server
This is a Pihole DNS server that runs in Docker. Since this is local, it will not be acting as a DHCP server for other devices.

run: `sudo nano /etc/resolv.conf` and add these lines near the bottom, but before the text that isn't commented out:
```
nameserver 127.0.0.1
options timeout:1 attempts:2
```
When you scroll down past all the commented out parts of `/etc/resolv.conf`, it should look sommething like this:
```
nameserver 127.0.0.1
options timeout:1 attempts:2

nameserver 127.0.0.53
options edns0 trust-ad
search home
```
## Note:
After you restart your computer, you will need to do the steps above again, as it reverts back to normal after a restart.

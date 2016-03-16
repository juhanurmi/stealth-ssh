Stealth SSH server using onion service
======================================

Tor and onion service for your SSH server with password protected onion address.

This onion service cannot be port scanned.
Does not allow anyone else to port scan or fingerprint your SSH server.
Hence no risk of exposing your onion address <=> real IP address because SSH fingerprint match.

You should read the autoconfigure.sh and execute the lines by hand.

- Install Tor
- Create a hidden service
- Add HiddenServiceAuthorizeClient stealth SOMEPASS
- HiddenServicePort 22 127.0.0.1:22 # Last is your current SSH port
- service tor restart
- On client side create .ssh/config
- On client side add HidServAuth settings to /etc/tor/torrc


This is autoconfigurate script.
I still recommend to read it and make the changes manually.

```sh
$ sudo bash autoconfigure.sh
```

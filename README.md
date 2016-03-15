Stealth SSH server using onion service
======================================

Why not use Tor and onion service for your SSH server?

Short guide to the crawler installation
---------------------------------------

You should read the autoconfigure.sh and execute the lines by hand.

- Install Tor
- Create a hidden service
- Add HiddenServiceAuthorizeClient stealth SOMEPASS
- HiddenServicePort 22 127.0.0.1:22 # Last is your current SSH port
- service tor restart
- On client side create .ssh/config
- On client side add HidServAuth settings to /etc/tor/torrc


```sh
$ sudo bash autoconfigure.sh
```

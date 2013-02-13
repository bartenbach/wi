##wi
-----------
![Screenshot](http://i.imgur.com/6vBB3Wu.png)
-----------

###description
wi is a lightweight cli network manager for linux.

###status
wi is highly experimental and currently still in developement.
It is in no way recommended for a daily driver at the current
point in time.

###commands
    Usage: wi [arguments]
      -p, --profile filename          Connect using the following profile
      -o, --open interface essid      Connect to an open or unsecured wireless
                                      network via dhcp
      -e, --wep interface essid pass  Connect to a WEP secured network using the
                                      password 'pass'
      -a, --wpa interface essid pass  Connect to a WPA secured network using the
                                      password 'pass' 
      -w, --wired interface           Connect to a wired network using interface
                                      via dhcp 
      -t, --test                      Check for a current internet connection
      -s, --scan interface            Scan for wireless networks with interface
      -h, --help                      Show this menu
      --version                       Print the current version of wi

###configuration file
The following configuration file defaults to /etc/wi/wi.conf
    # wi configuration file

    # use color? true/false
    color=true
The only option the configuration file currently controls is color output.

###installation
Ensure you have the following dependencies installed:
**bash iproute2 iwconfig wireless-tools dhcpcd**
(These are relatively common packages to have)

Save wi first, and then ``chmod +x wi && mv wi /usr/local/bin``

((Assuming ``/usr/local/bin`` is in your ``$PATH``)

Then simply run ``wi`` in a shell.

# tormake
Get the latest version of Tor from https://torproject.org, compile and install all with a single command.

1. `git clone https://github.com/cbanowsky/tormake`
2. `cd tormake`
3. `sudo su`
4. `chmod +x torgrabber`
5. `./torgrabber`

Sit back and enjoy.  


### Configuring torrc

You will want to configure your torrc located in `/usr/local/etc/tor`

Change make `SocksListenAddress 127.0.0.1:9500` or any port that is open that you wish to use.
Change Nickname to something cool or random...I don't care.

To get things working quickly make this adjustment `SocksPolicy accept *` to accept connections to your SOCKS proxy server.

Save the file.



### System Settings 

Change network -> proxy to SOCKS proxy.  Host: 127.0.0.1 Port: 9500 `// or whatever port you used above`

Configure internet connected clients to use the proxy set by system.

As a non-root or sudo user simply run the command `tor` and tor will bootstrap and open up a circuit for you.  You can then go to [check tor](https://check.torproject.org) in your browser to make sure everything is working correctly.

### Maintaining this script

I will adjust the wget call on which version of tor is being grabbed, as they publish stable builds.  Feel free to use the unstable version, just simply change the wget call inside the script.



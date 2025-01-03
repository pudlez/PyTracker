PyTracker
=========
PyTracker is a reverse-engineered version of the DXX Rebirth Tracker, written in python. 
Arch wrote this using the PyCharm python IDE on top of Python 3.4 and tested it down to Python 3.2

PuDLeZ took over hosting it on March 1, 2020. The tracker is currently using Python 3.8 but will soon be targeting Python 3.12

Contributers
============
* [Arch](https://github.com/adam2104)
* [Roncli](https://github.com/roncli)
* [PuDLeZ](https://github.com/pudlez)
* [Arne](https://github.com/arbruijn)


Files
-----
This package consists of four main files:

*    dxxtoolkit.py - general toolkit for communicating with DXX Rebirth and Retro clients
*    tracker.py - the actual tracker implementation
*    web_interface.py - generates static .html pages for game stats and game archives
*    my_functions.py - a few shared functions used by tracker.py and web_interface.py

Command Line Options
--------------------

```
--int_ip
        Specify one or more internal IP addresses. These IP addresses will be 
        replaced with the external IP address of the tracker when an external 
        host queries the tracker for a game hosted by an internal host. This 
        is useful if you host the tracker on the same network used for playing 
        the game.

--ext_ip
        Required if "--int_ip" is configured. This is the IP address that will 
        be sent when the internal IP address is replaced when replying to game 
        list requests. This will accept an IP address or a hostname.

--peer_hostname
        Specifies the IP address of a peer tracker to query for its game list. 
        That game list will then be merged with the game list maintained by 
        PyTracker. This will accept an IP address or a hostname.

--peer_port
        Specifies the port number of the peer tracker. This defaults to 42420.
```

Usage
-----
```
python3 tracker.py
```

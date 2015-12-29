# The Onion Box
Web based Status Monitor for [Tor Relays](www.torproject.org)

**The Onion Box** provides a web interface to connect to a Tor relay
and monitor aspects of it's operation in "real time". That's how it looks like
in action:

![image](https://cloud.githubusercontent.com/assets/16342003/12043105/c8f17f18-ae81-11e5-8b21-c7ecf80b37f9.png)

In addition to some static information regarding the host and Tor (like version
numbers or IPs) the page displays the upload / download performance using real
time charts and allows to switch Tor's event system.

## Installation
The Box depends on some additional libraries, so make sure they are
installed:

* [psutil](https://pypi.python.org/pypi/psutil)
* [configparser](https://pypi.python.org/pypi/configparser)
* [stem](https://pypi.python.org/pypi/stem)
* [Bottle](https://pypi.python.org/pypi/bottle)

Additionally I recommend to install [CherryPy](https://pypi.python.org/pypi/CherryPy) as webserver to be used!
(The Box runs as well with a standard server yet this one has issues with IE!)

## Configuration
### ... of The Onion Box
To adapt the Box to your Tor environment edit the configuration file located
in `~/config/theonionbox.cfg`. Every configuration option is well documented there
so it shouldn't be too difficult to get along.

### ... of Tor
The Box relies on Tor's authentication process to grant access. Therefore you
**have to**
* make sure that you configured a ControlPort.
* set the `HashedControlPassword` option in Tor's config file and define a
password to access the ControlPort.

## Box Operations
Open a console and launch The Box with `python theonionbox.py`.

As of now there is no support to run The Box as a daemon. Be assured that this is part of the TODO - list.

To see your relay in action browse to the address you configured and log
into the Box using the password you defined for the ConfigPort.

Leave me a message if you encounter any issues... which might probably happen! :cold_sweat:

Enjoy!
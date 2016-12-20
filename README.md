# Tinyproxy

Tinyproxy is a small, efficient HTTP/SSL proxy daemon released under the
GNU General Public License.  Tinyproxy is very useful in a small network
setting, where a larger proxy would either be too resource intensive, or
a security risk.  One of the key features of Tinyproxy is the buffering
connection concept.  In effect, Tinyproxy will buffer a high speed
response from a server, and then relay it to a client at the highest
speed the client will accept.  This feature greatly reduces the problems
with sluggishness on the Internet.  If you are sharing an Internet
connection with a small network, and you only want to allow HTTP
requests to be allowed, then Tinyproxy is a great tool for the network
administrator.

For more info, please visit [the Tinyproxy web site](https://tinyproxy.github.io/).


## Installation

Tinyproxy uses a standard GNU `configure` script based on the automake
system.  If compiling from a git checkout, you need to first run

```
./autogen.sh
```

from the top level directory to generate the `configure` script.
The release tarball contains the pre-created `configure` script,
so when building fom a release, you can skip this step.
Then basically all you need to do is


```
./configure
make
make install
```

in the top level directory to compile and install Tinyproxy. There are
additional command line arguments you can supply to `configure`. They
include:

- `--enable-debug`: 
If you would like to turn on full debugging support.

- `--enable-xtinyproxy`: 
Compile in support for the XTinyproxy header, which is sent to any
web server in your domain.

- `--enable-filter`: 
Allows Tinyproxy to filter out certain domains and URLs.

- `--enable-upstream`: 
Enable support for proxying connections through another proxy server.

- `--enable-transparent`: 
Allow Tinyproxy to be used as a transparent proxy daemon.

- `--enable-static`: 
Compile a static version of Tinyproxy.

- `--with-stathost=HOST`: 
Set the default name of the stats host.

For more information about the build system, read the INSTALL file
that is generated by `autogen.sh` and comes with the release tar ball.



## Support


If you are having problems with Tinyproxy, please raise an
[issue on github](https://github.com/tinyproxy/tinyproxy/issues).


## Contributing

If you would like to contribute a feature, or a bug fix to the Tinyproxy
source, please clone the
[git repository from github](https://github.com/tinyproxy/tinyproxy.git)
and create a [pull request](https://github.com/tinyproxy/tinyproxy/pulls).


## Community

You can meet developers and users to discuss development,
patches and deployment issues in the `#tinyproxy` IRC channel on
Freenode (`irc.freenode.net`).

# RTP Tools

RTP Tools is a set of small applications
that can be used for processing RTP data.
Refer to the individual manpages for details.

* **rtpplay**
	play back RTP sessions recorded by rtpdump
* **rtpsend**
	generate RTP packets from textual description,
	generated by hand or rtpdump
* **rtpdump**
	parse and print RTP packets,
	generating output files suitable for rtpplay and rtpsend
* **rtptrans**
	RTP translator between unicast and multicast networks
* **multidump**
	Start multiple rtpdumps simultaneously.
* **multiplay**
	Start multiple rtpplays simultaneously.

## Installation

The RTP tools should compile on any Posix-compliant platform
supporting sockets, as well as on Windows.

### UNIX

`./bootstrap; ./configure; make` for compiling.

`make install` for installing.
`make uninstall` for uninstalling.

`make distclean; ./configure; make dist` generates a source tar file `rtptools-*tar.gz`.
  e.g. rtptools-1.22.tar.gz

`make rpm-spec` will creat spec file for generating rpm package.
  Then run `rpmbuild -ba rtptools-*.spec` or
  `rpmbuild -bb rtptools-*.spec` on rpm based distribution.

### Windows (broken at the moment)

The `*.dsp` files are project files. `*.dsw` file and workspace file.
User can open the workspace file and use 'batch compile'
to compile all the projects.

* In Visual C++ 6.0, open workspace file rtptools.dsw.
* In VC menu Build, use Batch Build to build all the tools.
* All the rtptools will be created under the "debug\" directory.

## TODO

* Improve generating html for homepage.
* Fixing type mismatch warnings.
* Fixing building on windows.
* Added file to generate debian package.
* And any other issues come up.

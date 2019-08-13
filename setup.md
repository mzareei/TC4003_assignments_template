# TC4003 Assignment Setup

### Go Installation

You will need a working Go environment for the assignments. 
Your version should be at least Go 1.9, which is the version that Grading scripts will use.
The latest version as of the Fall 2018 semester is Go 1.11. Things work in 1.9 should also work in 1.11. Learn more about semantic of versioning [here](https://semver.org/).

<h3>Manual for Various OSes</h3>
<p>
  Another option is to install Go on your own machine manually. There are instructions to install from source or with a 
  package installer for several operating systems at Google's Go site: <a href="https://golang.org/dl/">golang.org</a>.
</p>

<h3>Via Package Manager for OS X</h3>
<p>
  Finally, for Macs many people use package management software, the two most common of which are 
  <a href="http://brew.sh/">Homebrew</a> and 
  <a href="https://guide.macports.org/">MacPorts</a> 
  (these links include installation instructions for the package managers themselves). 
  Here is a walkthrough of installing Go using each of these:
<pre>
dustpuppy:~$ brew --version
0.9.5
dustpuppy:~$ go
-bash: go: command not found
dustpuppy:~$ brew install go
==> Downloading https://homebrew.bintray.com/bottles/go-1.7.1.el_capitan.bottle.
######################################################################## 100.0%
==> Pouring go-1.7.1.el_capitan.bottle.tar.gz
==> Caveats
As of go 1.2, a valid GOPATH is required to use the `go get` command:
  https://golang.org/doc/code.html#GOPATH

You may wish to add the GOROOT-based install location to your PATH:
  export PATH=$PATH:/usr/local/opt/go/libexec/bin
==> Summary
🍺  /usr/local/Cellar/go/1.7.1: 6,436 files, 250.6M
dustpuppy:~$ go version
go version go1.7.1 darwin/amd64</pre>
NB: if <tt>brew install go</tt> attempts to install an ancient version (e.g. 1.3) you will have to do <tt>brew update</tt> first to refresh your list of packages that Homebrew knows about.
<pre>
dustpuppy:~$ port version
Version: 2.3.4
dustpuppy:~$ go
-bash: go: command not found
dustpuppy:~$ sudo port install go
Password:
Warning: The Xcode Command Line Tools don't appear to be installed; most ports will likely fail to build.
Warning: Install them by running `xcode-select --install'.
--->  Computing dependencies for go
--->  Dependencies to be installed: go-1.4
--->  Fetching archive for go-1.4
--->  Attempting to fetch go-1.4-1.4.3_0.darwin_15.x86_64.tbz2 from https://packages.macports.org/go-1.4
--->  Attempting to fetch go-1.4-1.4.3_0.darwin_15.x86_64.tbz2.rmd160 from https://packages.macports.org/go-1.4
--->  Installing go-1.4 @1.4.3_0
--->  Activating go-1.4 @1.4.3_0
--->  Cleaning go-1.4
--->  Fetching archive for go
--->  Attempting to fetch go-1.7_0.darwin_15.x86_64.tbz2 from https://packages.macports.org/go
--->  Attempting to fetch go-1.7_0.darwin_15.x86_64.tbz2.rmd160 from https://packages.macports.org/go
--->  Installing go @1.7_0
--->  Activating go @1.7_0
--->  Cleaning go
--->  Updating database of binaries
--->  Scanning binaries for linking errors               
--->  No broken files found.
dustpuppy:~$ go version
go version go1.7 darwin/amd64</pre>
</p>

<h2>Tools</h2>
<p>
 There are many commonly used tools in the Go ecosystem. The three most useful starting out are:
 <a href="https://golang.org/cmd/gofmt/">Go fmt</a> and <a href="https://golang.org/cmd/vet/">Go vet</a>, which are built-ins, and <a href="https://github.com/golang/lint">Golint</a>.
</p>


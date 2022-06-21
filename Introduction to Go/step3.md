---
title : Installation and Setup
---

To save you the hassle, Go environment is already setup for this environment so, you can skip this step. Although you can use the following instructions to set up Go on your own systems.  

Start by downloading the binary for Go. You can use curl or wget to download the current binary for Go from the official download page.

```
curl -O https://storage.googleapis.com/golang/go1.18.linux-amd64.tar.gz
```

1.18 is the version of Go you’ll want to download. However, this can be replaced with any other version if necessary.

Next, use `tar` utility to unpack the package. The following command will use the tar tool to open and expand the downloaded tar.gz file and to create a folder of the package name:

```
tar -xvf go1.18.linux-amd64.tar.gz
```

Then, move the folder to `/usr/local` .

```
sudo mv go /usr/local
```

The Go package is now in `/usr/local`, which makes sure that Go is in your `$PATH` environment variable for Linux.

Now, we have to set some paths that Go needs. The paths given in this step are all relative to the location of the Go installation in `/usr/local`.

Add `/usr/local/go/bin` to the PATH environment variable.

You can do this by adding the following line to your `$HOME/.profile` or `/etc/profile` (for a system-wide installation):

```
export PATH=$PATH:/usr/local/go/bin
```

*Note : Changes made to a profile file may not apply until the next time you log into your computer. To apply the changes immediately, just run the shell commands directly or execute them from the profile using a command such as source $HOME/.profile.*

It’s always a good idea to see if your installation has been successful or not. This can be done by checking the version number of the Go language installed in your system.

```
go version
```

The version number of Go installed in your system will be displayed on the terminal.

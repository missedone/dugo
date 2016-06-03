du (Disk Usage) with golang
====

It's a simple du alike app that prints the size of the folder (and its sub-folders)


## Installation

```bash
go get -u github.com/missedone/dugo
```

## Usage

```
Usage: dugo [options...] <target_dir>

Options:
  -h  "Human-readable" output.  Use unit suffixes: Byte, Kilobyte, Megabyte, Gigabyte.
  -t  threshold of the size, any folders' size larger than the threshold will be print. for example, '1G', '10M', '100K', '1024'
  -d  list its subdirectories and their sizes to any desired level of depth (i.e., to any level of subdirectories) in a directory tree.
```

## Example

1. list with max depth as 1 (equivalent to `du -h -d 1 /opt/vagrant`
```
dugo -h -d=1 /opt/vagrant
2.3M	 /opt/vagrant/bin/
212.1M	 /opt/vagrant/embedded/
214.4M	 /opt/vagrant/
```
2. list and only show the folders larger than threshold
```
dugo -h -d=1 -t=100M /opt/vagrant
212.1M	 /opt/vagrant/embedded/
214.4M	 /opt/vagrant/
```
so in this example, `/opt/vagrant/bin/` was not shown on the output since its size is under the threshold '100M'.

## Build

use golang 1.5 or above which [comes with support for all architectures built in](http://dave.cheney.net/2015/03/03/cross-compilation-just-got-a-whole-lot-better-in-go-1-5).

```
# for mac
env GOOS=darwin GOARCH=amd64 go build -v

# for linux
env GOOS=linux GOARCH=amd64 go build -v

# for windows
env GOOS=windows GOARCH=amd64 go build -v
```

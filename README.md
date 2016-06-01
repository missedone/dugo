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
```

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

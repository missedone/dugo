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

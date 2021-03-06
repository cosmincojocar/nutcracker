# nutcracker

Tool to crack hexadecimal secrets which are used as bearer tokens (not a good idea!).

## Installation

```
go get -u github.com/ccojocar/nutcracker
```

## Usage

```
$> nutcracker -h

Usage of nutcracker:
  -parallel-attacks int
        number of parallel attacks (default 8)
  -token-length int
        size of the bearer token (default 32)
  -url string
        URL to brute force
```

You can brute force a hexadecimal secret of 16 characters as follows:

```
$> nutcracker -url https://<URL> -token-length 16 -parallel-attacks 8
```

The tool will print into the console the valid token when the brute force attack is completed.

```
Valid Token: <token value>
```

The brute force attack can be interrupted at any time with Ctrl+C.

# 🔑 ftpknocker

ftpknocker is a multi-threaded scanner for finding anonymous FTP servers

[![Code Climate](https://img.shields.io/codeclimate/maintainability/kennell/ftpknocker.svg)]() [![Codeship](https://img.shields.io/codeship/8bbeefb0-b024-0135-06e5-0696d4e76991.svg)]() [![Codecov](https://img.shields.io/codecov/c/github/kennell/ftpknocker.svg)]() [![PyPI](https://img.shields.io/pypi/v/ftpknocker.svg)]() 


## How to install

```
pip install ftpknocker
```

## Usage

```
Usage: ftpknocker [OPTIONS] [TARGETS]...

Options:
  --threads INTEGER         Number of threads to utilize
  --port INTEGER            Port to scan
  --timeout FLOAT           Seconds before timeout
  --shuffle / --no-shuffle  Shuffle target list
  --help                    Show this message and exit.
```

## Usage Examples

The syntax for specifying targets is similar to nmap. Here are some examples:

Scan three individual IPs:
```bash
ftpknocker 192.168.1.1 192.168.1.2 192.168.1.3
```

Scan an entire IP-block using [CIDR notation](http://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation). In this example, a total of 256 hosts are scanned:
```bash
ftpknocker 192.168.1.0/24
```

Feed targets from a other program using a pipe (IPs must be sperated by newlines):
```bash
cat mytargets.txt | ftpknocker
```

# DRSpy

Data analysis module for [DRS4 board](https://www.psi.ch/en/drs/evaluation-board).

**BETA** version. May not work 

---

## Installation

### Using pip

```console
user@host:~$ pip3 install DRSpy
```

### From source

```console
user@host:~$ python3 setup.py install
```

---

## Usage

Run `drspy --help` to see available options

```
Usage: drspy [OPTIONS] COMMAND [ARGS]...

  Data analysis tool for DRS4(PSI) board.

Options:
  -d, --db TEXT      Database location  [default: data.csv]
  -c, --config TEXT  Configuration file  [default: drspy.config]
  -v, --verbose      Enable verbosity mode
  --version
  -h, --help         Show this message and exit.

Commands:
  cli     Command line
  desc    Data description
  help
  macro   Load macro
  plot    Generate graphs
  run     run
  update  Update database

```


## Examples

### Creating database

```console
user@host:~$ drspy update -a <DATA_DIR>
```

```
Usage: drspy update [OPTIONS] <files or dir>

Options:
  -f, --format [xml|PtP|delay]  Input file format  [default: PtP]
  -a, --auto                    Recognize file automatically
  -t, --tag TEXT                Add <tag> to data headers
  -h, --help                    Show this message and exit.
```

### Get graphs (Channel and Delay)

```console
user@host:~$ drspy run
```

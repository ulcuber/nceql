# NCursesEQueryList

Interactive dependency browser for Gentoo packages using `equery`.

## Features

- Browse packages by repository (overlay)
- View dependency graphs with dependants count
- Keyboard-driven vim ncdu-style navigation
- Caches results for faster subsequent launches

# Installation

```bash
git clone git@github.com:ulcuber/nceql.git
sudo emerge --ask --quiet --verbose app-portage/gentoolkit
```

# Usage

```bash
./depgraph <atom>
./depgraph "@selected"
# will be slow
./depgraph "@installed"
```

# Dev

## Lint

```bash
python -m ruff format depgraph
```

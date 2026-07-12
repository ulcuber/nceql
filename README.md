# NCursesEQueryList

Interactive dependency browser for Gentoo packages using `equery`.

## Features

- Browse packages by repository (overlay)
- View dependency graphs with dependants count
- Keyboard-driven vim ncdu-style navigation
- Caches results for faster subsequent launches

# Installation

```bash
eselect repositories enable masterwolf && emerge --sync masterwolf # To enable the repository (if not already)
echo "app-portage/nceql **" > /etc/portage/package.accept_keywords/nceql  # To accept the unkeyworded pachage
emerge --ask app-portage/nceql
```
Or if you would like to manually install instead:
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

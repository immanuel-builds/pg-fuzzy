
# pg-fuzzy

An interactive PostgreSQL database selector for Linux terminals, powered by Bash, psql and fzf.

## Features

- Discover accessible PostgreSQL databases.
- Interactive fuzzy search and selection.
- Connect directly using psql.
- Support local and remote PostgreSQL servers.
- Respect existing PostgreSQL authentication settings.

## Requirements

| Dependency | Minimum version | Purpose |
|---|---|---|
| Bash | 4.0+ | Shell execution |
| PostgreSQL client (psql) | 14+ | Database discovery and connection |
| fzf | 0.38+ | Interactive database selection |

A PostgreSQL server must be accessible for database discovery.

Git is only required for development and contribution.

## Installation

Install the dependencies using your Linux distribution's package manager.

On Fedora:

```bash
sudo dnf install postgresql fzf
```

Make the executable:

```bash
chmod +x pg-fuzzy
```

Run:

```bash
./pg-fuzzy
```

## Remote connections

pg-fuzzy respects standard PostgreSQL connection environment variables.

```bash
PGHOST=db.example.com PGPORT=5432 PGUSER=developer ./pg-fuzzy
```

For a custom maintenance database:

```bash
PGFUZZY_MAINTENANCE_DB=postgres ./pg-fuzzy
```

## Usage

```bash
./pg-fuzzy
./pg-fuzzy --help
./pg-fuzzy --version
```

Navigate using arrow keys, type to filter, and press Enter to connect.

Press Escape to cancel.

## License

MIT License. See LICENSE for details.

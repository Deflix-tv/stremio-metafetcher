# stremio-metafetcher

A CLI that goes through a list of IMDb IDs and then fetches and stores their Stremio-digestible metadata from Cinemata as JSON files

## Usage

```text
Usage of stremio-metafetcher:
  -dataDir string
        Location of the data directory. It contains CSV files with IMDb IDs and a "metas" subdirectory will be used for writing metas as JSON files. (default ".")
  -version
        Prints the version of stremio-metafetcher
```

- The `dataDir` directory is expected to contain CSV files that have a "IMDb ID" header column
- `stremio-metafetcher` will go through *all* files in `dataDir` and skip those that don't end in `.csv`
- `stremio-metafetcher` will *not* fetch metadata for IMDb IDs where a JSON file already exists

This is fairly opinionated and geared towards a specific use case. Future versions will be more flexible and probably allow listing CSV files via CLI argument, as well as defining a separate output directory via CLI argument.

# ICONS-catalog

Curated application catalog and metadata index for the ICONS offline portable application engine.

## Layout

```text
ICONS-catalog/
├── .github/
│   └── workflows/
│       └── sync-catalog.yml    # Automated sync pipeline (every 6 hours)
├── bucket/                     # Curated application manifests
│   └── aria2-next.json
├── curated-sources.json        # Curated upstream sources list
└── index.json                  # Metadata index (versions, hashes, tiers)
```

## Automation

The GitHub Actions workflow runs every 6 hours and can be manually dispatched to:
1. Sync upstream manifests defined in `curated-sources.json`.
2. Generate `index.json` with versions, architecture URLs, hashes, and tier information.
3. Commit updates to the `main` branch.

# Exchange Rates Data

Historical USD to EUR exchange rates used by [GainSight](https://github.com/abdelkarim00/gainsight) for capital gains calculations in EUR.

## Purpose

This repository stores historical exchange rates to minimize API calls to exchangerate.host (limited to 100 requests/month on free tier).

## How it works

1. The GainSight app fetches `usd-eur-rates.json` from this repo first
2. Only if a date is missing, it calls the exchangerate.host API
3. A GitHub Action runs daily to add new rates automatically

## Data Source

- **API**: [exchangerate.host](https://exchangerate.host)
- **Update Frequency**: Daily via GitHub Actions
- **Format**: JSON with date keys (YYYY-MM-DD) and rate values

## Usage

Fetch the raw JSON directly:
```
https://raw.githubusercontent.com/abdelkarim00/exchange-rates-data/main/usd-eur-rates.json
```

## License

MIT - Free to use

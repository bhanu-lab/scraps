# Kaveri Data Scraper

## The Data
[remap.json](remap.json) contains a reverse mapping of Village names to their corresponding District, Taluk and Hobli names.

## 🤖 Automated Updates
The data is automatically updated using GitHub Actions that runs weekly:

- **Weekly updates**: Full data refresh every Sunday at 3 AM UTC
- **Manual triggers**: Run anytime via GitHub Actions
- **Change detection**: Only creates PR when actual changes occur
- **Smart summaries**: Clear reporting in GitHub Actions

### Setup Automation
See [AUTOMATION.md](AUTOMATION.md) for complete setup instructions including:
- GitHub Actions configuration
- Local development setup
- Credential management

## Why?
Some documents/information on the [kaveri website](https://kaveri.karnataka.gov.in/) ask you to select your Village from a dropdown. This dropdown is preceded by District, Taluk and Hobli dropdowns, each filled based on previous selections. Finding your Village requires trial and error to get the right options selected.

## The Process
1. **Authentication**: Uses browser session credentials via GitHub Secrets
2. **Data Collection**: Scrapes using internal APIs with rate limiting
3. **Hierarchy Building**: District → Taluk → Hobli → Village mapping
4. **Reverse Mapping**: Creates village-to-hierarchy lookup in [remap.json](remap.json)
5. **Change Detection**: Only creates PR when Karnataka administrative data changes
6. **Automated PRs**: Creates Pull Requests automatically via GitHub Actions for review

## Files Generated
- `district_talukas.json` - District to Taluk mapping
- `taluk_hoblis.json` - Taluk to Hobli mapping  
- `hobli_villages.json` - Hobli to Village mapping
- `village_mapping.json` - Complete village data
- `remap.json` - **Main file**: Village name → full hierarchy lookup
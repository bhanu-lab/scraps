# Scraps
A collection of web scrapers and utilities for extracting and processing data to ease government processes.

## Current Tools
### Kaveri Jurisdiction Scraper
Extracts the complete jurisdictional hierarchy (District → Taluk → Hobli → Village) with automated data updates. Includes:
- District and taluka mapping
- Hobli information for each taluka  
- Village data for each hobli
- Search interface to find jurisdiction details for any village
- **Automated updates**: Weekly data refresh via GitHub Actions

## 🤖 Automation
The Kaveri scraper now includes automated data collection that:
- Runs weekly (Sundays at 3 AM UTC)
- Creates Pull Requests when data changes
- Maintains up-to-date Karnataka administrative data
- Requires zero manual intervention

See [kaveri/README.md](kaveri/README.md) for setup instructions.

## Legal Disclaimer
This tool is for educational and research purposes only. Users are responsible for ensuring their use of this tool complies with applicable laws and terms of service. The maintainers are not responsible for any misuse of this software.

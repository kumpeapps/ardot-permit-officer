# ardot_permit_officer

A Python package to fetch ARDOT permit officer contact information from all 10 district pages.

## Features
- Scrapes name, email, and phone number for each district's permit officer
- CLI tool to print or export the data


## Usage

### Command Line

Install the package (from PyPI or locally):

```bash
pip install ardot_permit_officer
```

Run the CLI to print all permit officer info as JSON:

```bash
ardot-permit-officer
```

### Python API

You can also use the package in your own Python code:

#### Get all permit officers
```python
from ardot_permit_officer.scraper import get_all_permit_officers
officers = get_all_permit_officers()
for officer in officers:
	print(officer)
```

#### Get a single district's permit officer
```python
from ardot_permit_officer.scraper import get_permit_officer_by_district
officer = get_permit_officer_by_district(7)  # For district 7
print(officer)
```

## Publishing
Publishing to PyPI is automated via GitHub Actions. See `.github/workflows/publish.yml`.

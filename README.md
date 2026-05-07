# KM Metadata Readout Generator

## Overview

This notebook generates an Excel readout of Celonis Knowledge Model metadata. It extracts records, attributes, KPIs, filters, variables, and other KM components, then writes the selected metadata to a multi-sheet workbook.

## What it does

- Connects to a Celonis team.
- Loads a Studio space, package, and Knowledge Model.
- Extracts metadata from KM records and related components.
- Extracts KM variables and view variables where applicable.
- Writes the resulting metadata tables to an Excel workbook.

## Requirements

- Python/Jupyter Notebook environment.
- Celonis Studio access to the target space, package, and Knowledge Model.
- API key with permissions to read the KM and package content.
- Python packages:
  - `pycelonis`
  - `pandas`
  - `xlsxwriter`
  - `tqdm`

## Setup

Fill in the user input variables:

```python
team_url = ''
api_key = ''
key_type = 'USER_KEY'
space_id = ''
package_id = ''
km_id = ''
```

IDs can be found in the Celonis URL:

- `space_id`: after `space/`
- `package_id`: after `package/`
- `km_id`: after `node/`

## Usage

1. Fill in the user input section.
2. Restart the kernel.
3. Run all cells.
4. Review the generated Excel workbook.

## Output

```text
KM_Readout_FINAL.xlsx
```

The workbook contains one or more sheets with Knowledge Model metadata, depending on what components exist in the selected KM.

## Important notes

- The notebook extracts the fields that appear most relevant for KM documentation, but not necessarily every available metadata field.
- Large Knowledge Models may produce large Excel files.

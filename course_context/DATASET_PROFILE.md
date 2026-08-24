# Dataset Profile

## Dataset identified

- File: `course/Further Consolidated Data, HnL.xlsx`
- Repository path: `course/Further Consolidated Data, HnL.xlsx`
- Repository-reported size: 18,880,688 bytes

## Inspection status

The workbook is present in the Git repository, but the available GitHub connector cannot decode XLSX binary content. Consequently, the actual sheet names, row counts, columns, data types, missing values, unique categorical values, Output Power ranges, city/year coverage, timestamp intervals, duplicates, and suspicious values have **not** been verified in this stage.

No dataset statistics are fabricated here.

## Required inspection when binary workbook access is available

The validation script/process should report:

- workbook filename
- number of sheets and sheet names
- rows per sheet
- column names
- data types
- missing-value counts
- unique values for categorical fields
- Output Power min/max and distribution summaries
- city coverage
- year coverage
- approximate sample counts by city/year
- timestamp construction and time interval
- duplicate rows and duplicate timestamps
- suspicious/invalid values
- daylight/night behavior
- presence and ranges of GHI, DNI, DHI, Clearsky GHI, Clearsky DNI, and Clearsky DHI
- Cloud Type values
- Output Power behavior by city

## Fields requiring special attention

The project specification specifically calls out:

- Output Power
- Cloud Type
- GHI
- DNI
- DHI
- Clearsky GHI
- Clearsky DNI
- Clearsky DHI
- Year
- Month
- Day
- Hour
- Minute

## Specification discrepancy status

No factual dataset/specification discrepancy can be declared yet because the workbook contents have not been decoded. The written specification itself warns that the actual workbook must be checked rather than assumed to match the specification.

## Data-quality and leakage checks to perform

1. Verify chronological ordering within each city.
2. Identify duplicate timestamps/rows.
3. Check missing and nonphysical irradiance values.
4. Check Output Power for negative or otherwise suspicious values.
5. Verify whether Cloud Type is categorical and enumerate its actual values.
6. Determine whether timestamps are regular and whether gaps exist.
7. Compare city-specific Output Power scales before regression/transfer experiments.
8. Determine whether target labels are directly derived from irradiance variables that could otherwise be used as predictors.
9. Verify whether lag features cross train/test boundaries.
10. Preserve an auditable raw-data snapshot/profile before transformations.

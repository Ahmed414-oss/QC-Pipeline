# QC-Pipeline
This pipeline has been developed for IAEA / NAHRS section. The pipeline loads 14 Excel sheets from one merged Excel workbook, stores them in a list of data frames, and runs a series of automated checks to identify missing values, invalid codes, incorrect formats, implausible values, and columns that should be empty.

The output is printed directly in the R console / R Notebook using clear status messages:

- ✅ Passed / valid / empty / within range
- ⚠️ Warning / missing values / not empty
- ❌ Failed / invalid / column not found / out of range

---

## Purpose of the Pipeline

The main purpose of this pipeline is to check whether DLW dataset sheets are ready for further review or submission.

It checks:

1. Whether all mandatory variables are filled in.
2. Whether autocalculated columns are empty.
3. Whether sex is coded correctly.
4. Whether ethnicity is coded correctly.
5. Whether measurement dates are plausible.
6. Whether latitude, longitude, and elevation values are plausible.
7. Whether Country ISO codes are valid.
8. Whether age, height, and body weight are within plausible ranges.
9. Whether ko, kd, No, and Nd values are within plausible DLW ranges.
10. Whether reproductive status variables are coded correctly.

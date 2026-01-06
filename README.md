# Spell Checker for Excel Descriptions

A Python-based spell checker that automatically identifies misspelled words in Excel file cells, helping to eliminate manual checking and save time on data validation tasks.

## Overview

This tool processes Excel files containing business descriptions or other text data, checks each cell for spelling errors, and generates a report with two additional columns:
- **SpellingCorrect**: Boolean flag (TRUE/FALSE) indicating if all words are spelled correctly
- **MisspelledWords**: List of misspelled words found in that cell

## Features

- Automated spell checking for Excel cell contents
- Identifies multiple misspelled words within a single cell
- Generates comprehensive spelling report
- Saves time by eliminating manual spell checking
- Preserves original data while adding validation columns

## Requirements

```
python>=3.7
pandas
openpyxl
pyspellchecker
```

## Example Output

**Input:**

![GUI Screenshot](https://github.com/JomuRegalado007/Python_Spell_Checker/blob/main/image/Before_image.png)

**Output:**

![GUI Screenshot](https://github.com/JomuRegalado007/Python_Spell_Checker/blob/main/image/After_image.png)

## Project Structure

```
excel-spell-checker/
│
├── Requirements                  # Basic installation
├── Error checking of file path   # Checking of file path for Python to feed .xslx file
├── Python Script                 # Basic spell checker script
├── README.md                     # This file
│
├── input_files/                  # Folder for input Excel files
│   └── input_data.xlsx
│
└── output_files/                 # Folder for output Excel files
    └── output_data.xlsx
```

## Troubleshooting

### Common Issues and Solutions

**Issue**: Too many false positives
- **Solution**: Add domain-specific terms to `CUSTOM_WORDS` list

**Issue**: File not found error
- **Solution**: Ensure input file path is correct and file exists

**Issue**: Column not found error
- **Solution**: Check that `COLUMN_TO_CHECK` matches your Excel column name exactly

**Issue**: Memory error with large files
- **Solution**: Process files in chunks using `pd.read_excel(chunksize=1000)`

## Acknowledgments

- Uses [pyspellchecker](https://github.com/barrust/pyspellchecker) library
- Built with [pandas](https://pandas.pydata.org/) for Excel processing
- Inspired by the need for automated data validation in business operations

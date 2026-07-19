# Precarious Oral Histories

This repository contains the RO-Crate metadata and configuration for the Precarious Oral Histories project. The RO-Crate metadata is generated from a spreadsheet and can be used to build a static HTML site.

## Install Dependencies

Run the following command to install `ro-crate-excel` and `ro-crate-html-lite` dependencies. The current version is using the `tabular-merge` branch of `ro-crate-excel` - this will be updated when the changes are merged into the main branch.

```bash
npm install
```

## Update RO-Crate from Spreadsheet

Run the following command to update the RO-Crate metadata from the spreadsheet. If the spreadsheet data has been updated, replace the existing `ro-crate-metadata.xlsx` in the `crate` directory with the new file, keeping the same name.

```bash
rocxl crate
```

## Build Static HTML Site

Run the following command to build the static HTML site from the RO-Crate metadata.

```bash
npx roc-html -c config/detailed-config.json -s config/oral-history.css crate
```

Any edits to the configuration can be made in `config/detailed-config.json` and edits to style in `config/oral-history.css`.

The output `ro-crate-preview.html` will be generated in the `crate` directory.
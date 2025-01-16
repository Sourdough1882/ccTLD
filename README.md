# ccTLD Data Repository

This repository provides structured data on public DNS registry suffixes, including country Top-Level Domains (ccTLDs) and known Second-Level Domains (ccSLDs).\
The primary purpose of this repository is to supply JSON files for parsing and other data-handling needs.

## Files

`ccTLD.json`: A list of country-specific Top-Level Domains (TLDs) with their respective country names.\
`ccTLD_ccSLD.json`: Extends the `ccTLD.json` file by including a list of known Second-Level Domains (SLDs) under each ccTLD.

### Structure of json files

`ccTLD.json`: 
```json
[
    {
        "code": ".suffix",
        "country": "Country Name"
    }
]
```
`ccTLD_and_ccSLD.json`: 
```json
[
    {
        "code": ".suffix",
        "country": "Country Name",
        "SLD": [
            ".suffix"
        ]
    }
]
```

## Data Source

All data is sourced from <a href="https://publicsuffix.org/">publicsuffix.org</a>, which provides a comprehensive list of TLDs and some SLDs. However, this repository is not exhaustive and should not be considered a definitive or reliable source. For instance, certain ccSLDs are not included in publicsuffix.org due to limited maintenance resources for specific countries.
Limitations:

* Incompleteness: The data set does not cover all possible country-specific Second-Level Domains (ccSLDs).
* Reliance on a Single Source: Currently, all data is based solely on <a href="https://publicsuffix.org/">publicsuffix.org</a>.

## Future Improvements

- [ ] Automatic Updates
- [ ] Additional Sources
- [ ] Data Validation
- [ ] REST API Integration

## Use Cases

This repository is intended for users who require raw data for custom parsing and handling of ccTLD and ccSLD information. While libraries exist for domain parsing, they often lack raw, structured data in JSON format.

# Coverage Parcsser
Fork github: [@isAdrisal/coverage-parcsser](https://github.com/isAdrisal/coverage-parcsser)

## Overview
This utility parses the JSON output from Chrome DevTools' coverage
reports and outputs the covered CSS, JS code on a per-file basis.

## Getting Started

### Usage
```
node index.js --file coverage.json
```
This will run the parser on all `.css` | `.js` files contained within the coverage.json report, and output each of the parsed `.css` | `.js` files to the current directory.

#### Arguments:
| Argument | Description                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| --file   | Path of the input .json file (REQUIRED)                                                                                      |
| --select | If provided, parses only the report for this URL (OPTIONAL).<br>Defaults to all resource URLs. Wrap url in quotes, eg. "url" |
| --outdir | Output directory of the exported file(s) (OPTIONAL).<br>Defaults to current directory.                                       |
```
node index.js --file coverage.json --select "https://foo.bar/example.css" --outdir ./output
```
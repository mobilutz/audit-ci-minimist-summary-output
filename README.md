This repo is related to this AuditCI issue: https://github.com/IBM/audit-ci/issues/239

The problem here is, that we have duplicate output of the same vulnerability found.
```
❯ yarn ll-audit
yarn run v1.22.17
$ audit-ci --config audit-ci-config.json
audit-ci version: 6.1.1
Yarn audit report summary:
{
  "vulnerabilities": {
    "info": 0,
    "low": 0,
    "moderate": 2,
    "high": 4,
    "critical": 0
  },
  "dependencies": 189,
  "devDependencies": 0,
  "optionalDependencies": 0,
  "totalDependencies": 189
}
Found vulnerable advisory paths:
GHSA-5v2h-r2cx-5xgj|esdoc>marked
GHSA-rrrm-qjm4-v8hf|esdoc>marked
GHSA-rp65-9cf3-cjxr|esdoc>cheerio>css-select>nth-check
GHSA-rp65-9cf3-cjxr|esdoc>ice-cap>cheerio>css-select>nth-check
GHSA-rp65-9cf3-cjxr|esdoc>cheerio>css-select>nth-check
GHSA-rp65-9cf3-cjxr|esdoc>ice-cap>cheerio>css-select>nth-check
GHSA-xvch-5gv4-984h|minimist
GHSA-xvch-5gv4-984h|esdoc>minimist
GHSA-xvch-5gv4-984h|minimist
GHSA-xvch-5gv4-984h|esdoc>minimist
Failed security audit due to high, moderate vulnerabilities.
Vulnerable advisories are:
https://github.com/advisories/GHSA-5v2h-r2cx-5xgj
https://github.com/advisories/GHSA-rrrm-qjm4-v8hf
https://github.com/advisories/GHSA-rp65-9cf3-cjxr
https://github.com/advisories/GHSA-xvch-5gv4-984h
Exiting...
error Command failed with exit code 1.
```

# Domain statistics from bulksearch.domains

Daily statistics for every domain extension (about 1,450 of them), published by
[bulksearch.domains](https://bulksearch.domains), and the names first seen in certificate
transparency logs each day.

**No domain lists are published here.** Lists of registered names are part of the paid data
downloads (see https://bulksearch.domains); this repository holds counts and certificate-log names
only.

## Files

| Path | What | Updated |
|---|---|---|
| `statistics/YYYY/YYYY-MM-DD.csv` | per extension: `day`, `tld`, `names` (registered names we hold), `added` and `removed` that day, `registry_share` (share of the names we track that have a registry answer of our own) | daily, by about 03:00 UTC for the previous UTC day |
| `registrars/YYYY/YYYY-MM-DD.csv` | per extension and registrar: `registrar_iana_id`, `registrar`, `names`, `share` (of the registered names with a registry record of ours) | weekly (Monday) |
| `certificate-names/YYYY/YYYY-MM-DD.txt.gz` | registrable names first seen in certificate transparency logs that day, one per line, sorted | daily |

How the numbers are made: names enter and leave our set from zone files, registry lists, our own
DNS checks and registry lookups (https://bulksearch.domains/docs). `added` counts names entering
the set that day (first registrations and returns), `removed` names leaving it.

## Licence

The data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): use it for
anything, with attribution to "bulksearch.domains". See LICENSE.

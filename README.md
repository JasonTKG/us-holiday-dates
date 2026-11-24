# Dates of holidays observed in the United States, by year

The date of each of 35 holidays observed in the United States, for every year the site prints. One row per holiday and year.

Site: https://holiday-dates.at01.io/

## Files

| File | Rows |
|---|---|
| `holiday_dates.csv` | 1,791 |

## Columns

**`holiday_dates.csv`**

- `holiday`: the site's key for the holiday; https://holiday-dates.at01.io/<holiday>/ is its page
- `name`: name of the holiday
- `family`: federal, christian, jewish, lunar or observance
- `year`: Gregorian year
- `date`: the date, computed from the holiday's rule; for daylight-saving-time the day it starts
- `weekday`: weekday of the date
- `observed_date`: federal holidays only: the day federal employees have off when the date falls on a weekend
- `begins_evening_of`: Jewish holidays only: the evening the holiday begins, as Hebcal gives it
- `last_day`: Jewish holidays: the last day, as Hebcal gives it (diaspora schedule); for daylight-saving-time the day it ends
- `checked_against`: the published tables the date was compared with: opm, usno, census, hebcal, hko, oca, or calendar (a fixed date or weekday rule checked against a calendar)

## Sources

| Source | URL | Terms | Retrieved |
|---|---|---|---|
| U.S. Naval Observatory, Astronomical Applications Department, data services | https://aa.usno.navy.mil/data/api | U.S. government work, public domain | 2026-11-24 |
| U.S. Census Bureau, Easter Dates from 1600 to 2099 | https://www.census.gov/data/software/x13as/genhol/easter-dates.html | U.S. government work, public domain | 2026-11-24 |
| Hebcal Jewish holiday calendar (diaspora schedule), CC BY 4.0 | https://www.hebcal.com/holidays/2027 | © Hebcal.com, CC BY 4.0 | 2026-11-24 |
| Hong Kong Observatory, Gregorian-Lunar Calendar Conversion Tables | https://www.hko.gov.hk/en/gts/time/conversion.htm | Used only to compare dates; no table reproduced | 2026-11-24 |
| U.S. Office of Personnel Management, Federal Holidays | https://www.opm.gov/policy-data-oversight/pay-leave/federal-holidays/ | U.S. government work, public domain | 2026-11-24 |
| Orthodox Church in America, Lenten and Paschal Cycle | https://www.oca.org/fs/paschal-cycle | Used only to compare dates; no table reproduced | 2026-11-24 |

## How it was checked

Each date is computed by our own code from the holiday's rule (a statute, the Gregorian and Julian computus, Hebrew calendar arithmetic, or new moons on the UTC+8 meridian for Lunar New Year) and compared with a published table; the build stops on any disagreement, and a date that no second source confirms is not printed. A separate program then reads every date on every finished page and compares it with the saved copies of the sources, taking weekdays from the Hong Kong Observatory's calendar files, and a test with planted errors confirms it catches them.

## Left out

New York Stock Exchange and Federal Reserve closing schedules are shown on the site but are not in this dataset: they are copied from those bodies' own tables, which carry no open licence. The dates here are our own computation; the Hong Kong Observatory's and the Orthodox Church in America's tables were used only for comparison.

## Licence

Creative Commons Attribution 4.0 International (see `LICENSE`). The `begins_evening_of` and `last_day` columns for Jewish holidays follow Hebcal's holiday data, © Hebcal.com, CC BY 4.0: keep that attribution when you reuse them.

## Maintainer

Built and maintained by [JasonTKG](https://github.com/JasonTKG); corrections and questions: open an issue.

Exported 2026-11-24 from the data the site's pages are generated from.

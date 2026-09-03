# SOC Investigation #1 — Investigation Notes

## Initial Observation

Five failed SSH password authentication attempts were observed against the `admin` account from source IP `10.10.10.45`.

The failed attempts occurred between `09:02:11` and `09:02:24`.

A successful password authentication for the same `admin` account from the same source IP occurred at `09:03:02`.

The successful authentication occurred 38 seconds after the final failed attempt.

## Initial Assessment

The authentication pattern is suspicious and requires further investigation.

At this stage, account compromise has not been confirmed.

## Key Indicators

| Indicator | Value |
|---|---|
| Source IP | `10.10.10.45` |
| Target account | `admin` |
| Failed attempts | 5 |
| Successful authentication | Yes |
| First failed attempt | `09:02:11` |
| Last failed attempt | `09:02:24` |
| Successful authentication | `09:03:02` |
| Delay after final failure | 38 seconds |

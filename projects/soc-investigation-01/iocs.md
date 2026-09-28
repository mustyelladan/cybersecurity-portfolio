# SOC Investigation #1 — Indicators of Interest

## Primary Suspicious Indicator

### Source IP: `10.10.10.45`

- Generated 5 failed password authentication attempts against `admin`.
- The attempts occurred between `09:02:11` and `09:02:24`.
- A successful password authentication for `admin` occurred at `09:03:02`.
- The successful authentication occurred 38 seconds after the final failed attempt.
- This IP is the highest-priority suspicious indicator in the available evidence.

## Secondary Suspicious Indicator

### Source IP: `172.16.20.8`

- Generated 2 failed password authentication attempts against `root`.
- The attempts occurred at `09:17:45` and `09:18:02`.
- No successful authentication from this IP is present in the available evidence.
- This activity is suspicious but has lower priority than the `10.10.10.45` activity.

## Target Accounts

### `admin`

The `admin` account was the target of five failed password attempts followed by a successful password authentication from `10.10.10.45`.

### `root`

The `root` account was targeted by two failed password attempts from `172.16.20.8`.

## Assessment

The available evidence supports treating `10.10.10.45` as the primary suspicious source associated with the authentication anomaly.

The evidence does not independently prove that either IP address represents a malicious actor. Further investigation would be required in a real environment.

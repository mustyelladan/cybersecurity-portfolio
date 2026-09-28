# SOC Investigation #1 — MITRE ATT&CK Mapping

## Technique 1 — T1110: Brute Force

### Observed Behavior

Five failed password authentication attempts were recorded against the `admin` account from source IP `10.10.10.45`.

A successful password authentication for the same account and source IP occurred 38 seconds after the final failed attempt.

### Assessment

The observed authentication pattern is consistent with password-guessing or brute-force activity.

### Evidence

- Source IP: `10.10.10.45`
- Target account: `admin`
- Failed attempts: 5
- Successful authentication: Yes

---

## Technique 2 — T1033: System Owner/User Discovery

### Observed Behavior

After the successful authentication, the `admin` account executed:

- `/usr/bin/id`
- `/usr/bin/whoami`

through `sudo` as `root`.

### Assessment

The use of `id` and `whoami` is consistent with discovering the current user and privilege context.

### Evidence

- Account: `admin`
- Privilege context: `root`
- Commands: `id`, `whoami`

---

## Confidence and Limitations

The mappings describe behaviors observed in the synthetic lab evidence.

They do not independently prove malicious intent or confirm that an account was compromised.

In a real investigation, additional evidence would be required, such as authentication source context, process information, command history, endpoint telemetry, network telemetry, and confirmation from the system owner.

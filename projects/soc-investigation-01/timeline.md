# SOC Investigation #1 — Event Timeline

| Time | Event | Source IP | Account | Assessment |
|---|---|---|---|---|
| 09:02:11 | Failed password authentication | 10.10.10.45 | admin | Suspicious |
| 09:02:14 | Failed password authentication | 10.10.10.45 | admin | Suspicious |
| 09:02:17 | Failed password authentication | 10.10.10.45 | admin | Suspicious |
| 09:02:20 | Failed password authentication | 10.10.10.45 | admin | Suspicious |
| 09:02:24 | Failed password authentication | 10.10.10.45 | admin | Suspicious |
| 09:03:02 | Successful password authentication | 10.10.10.45 | admin | High priority |
| 09:03:18 | `id` executed through sudo as root | Not recorded | admin | Privileged activity |
| 09:03:31 | `whoami` executed through sudo as root | Not recorded | admin | User/privilege discovery |

## Summary

The timeline shows five failed password authentication attempts against the `admin` account from `10.10.10.45`, followed by a successful authentication from the same source IP.

Sixteen seconds after the successful authentication, the `admin` account executed `id` and `whoami` through `sudo` as `root`.

The activity is suspicious and warrants further investigation. Account compromise is not confirmed based on the available evidence alone.

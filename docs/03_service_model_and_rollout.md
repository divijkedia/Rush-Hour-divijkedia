# Service model and rollout

> Core theme 1 (service model) and core theme 4 (rollout and success measures). Replace every `[[FILL IN]]`.

## 1. The service model

### From call to dispatched vehicle

Describe the flow step by step, from the citizen's phone call to the vehicle arriving. A numbered list or a simple diagram works well.

1. [[FILL IN]]
2. [[FILL IN]]
3. [[FILL IN]]

### Where humans stay in the loop

Who receives the recommended route? Can a dispatcher or driver override it? What happens when the system is down or not trusted (the manual fallback)?

[[FILL IN]]

### Channels

How does the citizen reach the service (phone call today)? Could SMS or an app be added later, and when?

[[FILL IN]]

### Who runs what

| Function | Run by | Notes |
| --- | --- | --- |
| Call handling | [[FILL IN]] | |
| The AI routing service | [[FILL IN]] | |
| The emergency vehicles | Third-party operators, paid by the government | |
| Data feeds (traffic, GPS, incidents) | [[FILL IN]] | |

## 2. Rollout

### Pilot

Where would you start (for example one high-traffic zone), for how long, and why there?

[[FILL IN]]

### Phases and go/no-go criteria

| Phase | Scope | Duration | Go/no-go criteria to move on |
| --- | --- | --- | --- |
| 1. Pilot | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |
| 2. Expansion | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |
| 3. City-wide | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |

### KPIs

| KPI | How it is measured | Baseline (assumed) | Target |
| --- | --- | --- | --- |
| Average response time in high-traffic zones | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |
| Share of calls meeting the response-time target | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |
| Dispatcher override rate | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |
| Cost per call | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |

Record every baseline and target as an assumption in `07_assumptions_log.md`.

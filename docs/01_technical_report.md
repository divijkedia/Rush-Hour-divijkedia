# Technical report

> Replace every `[[FILL IN]]`. Keep it factual: say what you did, what you measured, and what the numbers do not show. Every improvement claim needs a named baseline and a metric.

## 1. Data exploration

What did you learn about the data before modelling? Class balance, which features separate the classes, differences between maps, anything surprising.

[[FILL IN]]

## 2. Machine-learning model

* **Model(s) tried and why:** [[FILL IN]]
* **Validation approach** (if you tuned on the training data, say how you split it; remember to split by `map_id`): [[FILL IN]]
* **Held-out results** (from `results/metrics/ml_metrics.json`):

| Metric | Value |
| --- | --- |
| Accuracy | [[FILL IN]] |
| Macro F1 | [[FILL IN]] |
| Recall for `blocked` | [[FILL IN]] |
| Blocked cells predicted as not blocked | [[FILL IN]] |

* **Confusion matrix:** [[FILL IN: paste or reference a figure]]

### Error analysis (required)

Where is the model wrong, and why? Focus on blocked cells predicted as not blocked. Which features or map regions are involved? What does this imply for your blocking policy?

[[FILL IN]]

## 3. Blocking policy

Which cells can a route never enter, and why? If you use a probability threshold, how did you choose it? What does the policy do about the missed blocked cells above?

[[FILL IN]]

## 4. Cost function

How do predictions become a cost per cell? Give the formula, the parameters, and the reasoning. Does it use class probabilities? Does it add cost for incident probability?

```text
[[FILL IN: your cell cost formula]]
```

[[FILL IN: why this design]]

## 5. Route planner

Algorithm (Dijkstra, A*, or other), how it uses the cost function and the blocking policy, and any change to the provided `shortest_path()`. The objective is:

```text
J(P) = sum over every step u -> v of:  d(u, v) × ( c(u) + c(v) ) / 2
```

[[FILL IN]]

## 6. Results by scenario

Both routes use **the same blocking policy**. Cost is under your own objective. Judges also score against hidden ground truth.

| Scenario | Route | Length | Cost (your objective) | Extra distance vs distance-only | Cost change vs distance-only |
| --- | --- | --- | --- | --- | --- |
| RUSH-1 | Distance-only | [[FILL IN]] | [[FILL IN]] | | |
| RUSH-1 | Traffic-aware | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |
| RUSH-2 | Distance-only | [[FILL IN]] | [[FILL IN]] | | |
| RUSH-2 | Traffic-aware | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] | [[FILL IN]] |

Optional: RUSH-3 (stress test), with a more conservative policy. [[FILL IN or write "not attempted"]]

Figures: reference the images in `results/figures/`.

## 7. Trade-offs and robustness

How much extra distance did you accept, and why? What happens when you change the blocking threshold or the cost weights? Which experiments did you run, and what did they show?

[[FILL IN]]

## 8. Limitations

What does this work not show? Consider the synthetic data, the model's missed hazards, and the simplifications in the cost function.

[[FILL IN]]

## 9. Reproducibility

Commands, versions, seeds, and the order to run things. A judge should be able to reproduce `results/` from a fresh clone.

[[FILL IN]]

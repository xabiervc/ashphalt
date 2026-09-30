# Race flow diagrams

## Standard event

```text
[Workshop / Free Roam]
          |
[Event Preview: objective, route, risk, reward]
          |
       [Start]
          |
[Explore / Race / Attack / Shortcut / Rescue]
      /       \
 [Success]   [Failure]
    |           |
[Score, time,   [Fail-forward: damage, lost reward,
 reward, rep]    changed route or rival advantage]
      \       /
       [Aftermath]
          |
[Repair / Tune / Explore / Next Event]
```

## The Crown slice flow

```text
[Workshop Row]
   → choose Crown Circuit
   → drive Financial Ruins
   → official route or Old Transit shortcut
   → rival encounter
   → Authority response
   → weather route change at Floodgate Nine
   → finish / disable rival / fallback objective
   → faction decision
   → city-state update
   → return to changed Workshop Row
```

## Race design rule

Every official route has at least one safe line, one risky shortcut, one destruction opportunity, one recovery route, and one optional objective.

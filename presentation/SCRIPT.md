# Three-minute pitch — official teammate model

Aim to finish at 2:55. Approximately 330 spoken words; allow short pauses for navigation and demo actions. A: business speaker. B: modelling teammate.

## Slide 1 — A — 0:00–0:25

Our user is a SAF producer’s investment planner: where should we build, how large, and how should material move?

Kalimantan has 6.8 million tonnes of biomass, but 71% is in the west. Demand is split evenly across four airports. At 20% conversion yield, supplying them needs six million tonnes every year.

## Slide 2 — B — 0:25–1:05

The model chooses facility counts, sizes and flows over land-checked candidate sites. It balances construction spread over twenty years, operating costs and transport, while enforcing supply, capacity and fuel demand.

The proposed network has six large refineries and 23 depot units sharing those sites. It costs 890.1 million US dollars annually, versus 981.7 million for a feasible nearest-greedy baseline under the same official assumptions. That saves 91.6 million a year, or 9.3%, and brings cost per tonne from 818 to 742 dollars.

## Slide 3 — A — 1:05–1:30

The saving comes almost entirely from transport, rather than fewer refineries. Both networks have six large units.

Co-locating depots with refineries removes the intermediate biomass haul. Total transport falls from 158.4 to 67.1 million dollars annually. Upfront investment barely changes: about 4.69 billion dollars in either design.

## Slide 4 — A speaks; B drives — 1:30–2:25

[Set yield to 18%.]

Keep the original flow pattern and lower yield: 120 thousand tonnes go undelivered.

[Choose Compare solved designs.]

A stored seven-unit alternative meets demand at this yield. This compares solved designs and reprices them; it is not a fresh optimisation on every slider movement.

[Reset. Click Ketapang.]

Lose this refinery and 217 thousand tonnes are unserved before rerouting. Even perfect use of the remaining refinery capacity leaves at least 113 thousand tonnes short. Cheaper operation during an outage is not a saving: we are serving less fuel.

## Slide 5 — A — 2:25–2:55

Our recommendation is to shortlist these six shared hubs, with 21 large and two small depots.

Before committing capital, validate collectable feedstock, conversion yield, land and actual transport access. Then use the model to price reserve capacity and test rerouting against a service target.

The value is a transparent investment decision: a quantified cost improvement, a feasible comparison, and clear conditions under which the recommendation changes.

## Demo keys

Arrow keys move slides; F enters fullscreen. On slide4, Home on the yield slider selects18%; click Compare solved designs. Reset before the outage. Click the refinery again or Reset to restore it.

## Q&A boundaries

- The reported0.01% gap applies to the final co-located candidate model, not all possible geographic locations. Coordinate refinement is heuristic.
- The sensitivity library has63 supplied scenario plans plus the final polished network. Repricing fixed costs and tonne-kilometres is exact for each stored plan. It does not establish the continuous optimum at arbitrary slider values. The supplied package did not run its random fresh-solve library validation.
- Keep mode holds routes and the size-specific processing mix, scaling flows down when feasible. It does not reroute. Fully used sources/refineries cap proportional expansion.
- Outages remove the failed hub’s flows, retain all built-asset annual fixed costs, and keep other routes unchanged. Airport losses follow actual exported deliveries. The113kt number is a capacity lower bound, not a solved rerouting result.
- The construction slider changes refinery CapEx and its linked fixed OpEx. Depot construction costs stay at baseline. Distance multiplier applies to all three legs, including the supplied barge-distance convention. Depot-to-refinery rate is a separate input.
- No SAF sales price is supplied. Cost reductions are not profit-margin forecasts.

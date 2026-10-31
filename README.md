# Kalimantan SAF network presentation

Open [index.html](index.html) in a browser. The five-slide deck works offline with no install or external assets. Use the left/right arrow keys to navigate and **F** for fullscreen. The interactive analysis is on slide4. A stacked view is available at `index.html#sheet`.

The presentation keeps the original deck’s typography, cobalt/neutral palette, maps and five-screen story while using the teammate’s uploaded model package. [Speaking script](presentation/SCRIPT.md) fits the three-minute presentation, including a short technical explanation and demo.

## Model evidence

Source: `saf_project.zip` uploaded in commit `4ef8167800a5ced730617a152646013964840e6a`. That original archive is preserved unchanged. The figures below use its full-precision `outputs/results.json`, not the retired interim model.

| Annual metric | Proposed network | Feasible nearest-greedy baseline |
|---|---:|---:|
| Total cost, USDm/year |890.148|981.701|
| Cost per tonne SAF, USD |741.79|818.08|
| Transport, USDm/year |67.116|158.351|
| Upfront CapEx, USDbn |4.689|4.6935|
| SAF delivered, kt/year |1,200|1,200|

Saving: USD91.553m/year,9.326%. Final design:6 large refineries,21 large+2 small depot units co-located at6 hubs. It uses6,000kt of6,800kt available biomass at20% yield. Annual cost is CapEx/20+fixed OpEx5% of CapEx+size-specific processing+transport. The final reported gap is0.00981% for the co-located candidate model; it is not a global continuous-location certificate.

## Sensitivity and disruption

- **Keep sites & flow pattern:** exact evaluation of the exported flow pattern. Biomass flows and the original processing mix scale down to meet demand where possible. Proportional expansion is capped by fully used sources/refineries. The cost of reduced service is shown per tonne actually delivered; it must not be mistaken for savings.
- **Compare solved designs:**63 supplied scenario plans plus the final polished design. For a supported demand/yield pair, every matching plan is repriced at the selected refinery-construction multiplier, distance multiplier and depot–refinery rate; the cheapest is shown. This is a stored-design comparison, not a live MILP. General low-rate cases fix refinery counts from their corresponding hub design. Random fresh-solve validation was not included in the source package.
- **Outage:** a clicked refinery and its co-located depot flows stop; all other flows stay fixed. Built-asset annual fixed costs remain. Delivery losses are calculated from the model’s actual airport links. No rerouting is claimed. The113kt/year gap is the minimum residual refinery-capacity shortfall after one large refinery fails, assuming remaining capacity could be fully used; routing/supply can make service worse.
- A supply-insufficient demand/yield pair displays its aggregate shortfall without inventing a cost or a feasible network.

## Sources and files

`presentation/data/` preserves the supplied full-precision model results, sensitivity library, facilities, flows and biomass-use exports. `presentation/VALIDATION.json` records independent recomputation of both networks’ costs, source limits, mass balances, capacities, all airport demands, great-circle distances and facility membership in the supplied land polygon. These checks do not validate real roads, permits or feedstock collectability.

The original model archive contains the optimiser and source assumptions. No replacement optimiser was implemented for the presentation. The current deck replaces the old airport-adjacent comparison and interim scenario figures throughout.

# Toronto Bike Share maps

Static pages built from the public
[GBFS feeds](https://toronto.publicbikesystem.net/customer/gbfs/v2/gbfs.json)
and from a continuous local poll of them. No build step, no server.

## [Where the ASTROs are](https://freems88.github.io/astro-map/)

Live map of the **ASTRO** pilot e-bikes — the newest type in the fleet, a few
dozen bikes against ~1,300 EFIT and ~6,300 ICONIC, and the only one rated to
70 km. Reads the GBFS feeds straight from the browser and refreshes every 60
seconds.

- `?type=EFIT` (or any `vehicle_type_id`) maps a different part of the fleet
- "Nearest me" sorts by distance from your location
- Charging docks are shown saturated, plain docks muted — battery level is not
  published in the public feed, so a charging dock is the only charge signal
  there is

## [Dock Roulette](https://freems88.github.io/astro-map/reliability/)

How often each station **fails you**: empty when you want a bike (weekday
07:00–09:59) or full when you want to park (weekday 16:00–18:59). Built from
90 days of local polling at ~11-minute resolution across all 1,138 stations,
so unlike the ASTRO map this one is a periodic snapshot rather than live.

Search by name, filter by failure rate, click any station for both numbers.

Data is regenerated from the poller's SQLite archive into `reliability/data.json`.

Extracted from [BikeGone](https://github.com/Freems88/BikeGone).

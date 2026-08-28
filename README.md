# astro-map

Live map of the **ASTRO** pilot e-bikes in the Toronto Bike Share system.

ASTRO is the newest e-bike type in the fleet — a few dozen bikes against
~1,300 EFIT and ~6,300 ICONIC, and the only type rated to 70 km of range.
This page shows every one currently sitting in a dock.

**→ https://freems88.github.io/astro-map/**

Static page, no build step and no server. It reads the public
[GBFS v2 feeds](https://toronto.publicbikesystem.net/customer/gbfs/v2/gbfs.json)
straight from the browser and refreshes every 60 seconds.

- `?type=EFIT` (or any `vehicle_type_id`) maps a different part of the fleet
- "Nearest me" sorts by distance from your location
- Each station links out to Google Maps directions

Bikes move constantly — treat it as a shortlist, not a guarantee.

Extracted from [BikeGone](https://github.com/Freems88/BikeGone).

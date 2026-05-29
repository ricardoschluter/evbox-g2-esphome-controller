The Solar Surplus mode uses a grid power sensor.

Expected sign convention:

- Positive = importing from grid
- Negative = exporting to grid

The controller works as feedback control:

- grid power below `-deadband`: increase current
- grid power within `±deadband`: hold current
- grid power above `+deadband`: decrease current
- if at minimum current and grid import remains above threshold for the configured delay: stop charging
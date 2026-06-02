## RFID/card behavior

RFID/card IDs are currently tracked and exposed as Home Assistant text sensors:

- `EVBox Current RFID`
- `EVBox Last RFID`
- `EVBox Session RFID`

At this stage, there is no allowlist enforcement.  
Any RFID/card is accepted as long as `EVBox Charging Mode` is not set to `Off`.

Future versions may add an optional RFID allowlist using a Home Assistant helper.
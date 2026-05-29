# Wiring

EVBox internal 4-pin connector:

| Pin | Function |
|---|---|
| 1 | GND |
| 2 | RS485 B / inverting |
| 3 | RS485 A / non-inverting |
| 4 | +12V |

M5Stack ATOMIC RS485 Base:

| ESP32-S3 | Function |
|---|---|
| GPIO6 | UART TX |
| GPIO5 | UART RX |

Verify polarity and voltage before connecting.  
If RS485 communication does not work, try swapping A/B.
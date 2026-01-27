# Test Procedure

## Power Input
- Supply voltage: +5.0 V
- Connect GND to board ground
- Connect +5V to R1 input

## Expected Behavior
- LED D1 turns ON
- Current flows through R1 → D1
- Test point TP1 shows LED forward voltage

## Measurement
| Point | Expected |
|-----|----------|
| Supply | 5.0 V |
| TP1 | ~1.8–2.2 V (LED Vf) |
| Current | ~3–5 mA (with 1kΩ) |

## Failure Cases
- LED OFF → polarity check
- 0V at TP1 → open trace / solder issue
- Full 5V at TP1 → LED reversed or missing

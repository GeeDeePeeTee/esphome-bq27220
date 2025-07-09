# GDPT BQ27220 TODO

This is the active development checklist for the ESPHome-compatible `bq27220` fuel gauge component.

## Phase 1: Cleanup
- Remove `Arduino.h` include from headers
- Remove unused `DEFAULT_SCL` and `DEFAULT_SDA` macros
- Test build & functionality after cleanup

## Phase 2: Code Hygiene
-  Move method bodies from `bq27220.h` to `bq27220.cpp` for cleaner interface/implementation separation

## 🛠️ Phase 3: Schema Improvements
- Reformat `sensor.py` to use `cv.Required` and `cv.Optional` properly
- Group sensors logically in schema for easier YAML setup

## Phase 4: Bitmask + Status
- Implement status/flag sensors (OperationStatus, BatteryStatus, etc.)
- Expose them as binary sensors or masked numeric sensors in HA

## Phase 5: Advanced Control Support
- Add ESPHome `number`, `select`, `button` for:
  - Full Access
  - Design Capacity
  - Profile Switching
  - Sealing/Unsealing
  - etc.
- Map to Control/MAC commands via register logic
- Test Home Assistant control panel integration

---


# esphome-bq27220 BQ27220 ESPHome Component

A clean drop-in ESPHome component for the Texas Instruments BQ27220 fuel gauge, for hackers, tinkerers, and of course — for Dale. 🏁

## Features
- Reads State of Charge, State of Health, Voltage, Current, Capacity (Full, Design & Remaining), Temperature & Device ID
- Supports MAC and Control command access
- Designed to expand into status flags, calibration, sealing, profile config

## Quickstart with ESPHome

```yaml
external_components:
  - source:
      type: git
      url: https://github.com/GeeDeePeeTee/esphome-bq27220
    components: [bq27220]

i2c:
  sda: GPIOXX
  scl: GPIOXX

sensor:
  - platform: bq27220
    voltage:
      name: "Battery Voltage"
      id: batt_voltage
    current:
      name: "Battery Current"
      id: batt_current
    soc:
      name: "Battery SOC"
      id: batt_soc
    remaining_capacity:
      name: "Battery Remaining Capacity"
      id: batt_remaining_capacity
    temperature:
      name: "Battery Temperature"
      id: batt_temperature
    full_charge_capacity:
      name: "Battery Full Charge Capacity"
      id: batt_full_charge_capacity
    design_capacity:
      name: "Battery Design Capacity"
      id: batt_design_capacity
    state_of_health:
      name: "Battery State of Health"
      id: batt_soh
    device_number:
      name: "Battery Device ID"
      id: bq27220_battery_device_id
```

## 📖 Docs
- [BQ27220 Datasheet (TI)](https://www.ti.com/product/BQ27220)
- [ESPHome External Components Guide](https://esphome.io/components/external_components.html)

---

GDPT: Fueled by curiosity and doin' it for Dale!

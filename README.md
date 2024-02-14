# picopico EVT (Engineering Validation Test)

Validation and production test of `zeriyoshi/picoletta` and `zeriyoshi/xtrapico`.

## Specs

- Two `RP2040` implementations
    - BIG: Based on [`RetroScaler/RP2040-PICO-BOOT`](https://github.com/RetroScaler/RP2040-PICO-BOOT)
        - For main keyboard controller
        - Better and Rich implementation, not optimized usecase.
    - little: Based on [`zeriyoshi/xtrapico`](https://github.com/zeriyoshi/xtrapico)
        - For Raspberry Pi Pico compatible module
        - Simple and Flexible implementation, but unsure if it works.
        - xtrapico based on [`Breadstick-Innovations/22008-RP2040-Dev-Board`](https://github.com/Breadstick-Innovations/22008-RP2040-Dev-Board)
- `WS2812B-V5` and `SK6182MINI` testing environments
    - `RP2040` -> `WS2812B-V5` -> `SK6182MINI` Voltage conversion
    - `RP2040` -> MOSFET -> `SK6182MINI` Voltage conversion
    - Direct drive `SK6182MINI` on 3.3V
- Focus on manufactualing by [JLCPCB](https://jlcpcb.com/)

## Requirements

- KiCad 7
    - [`Bouni/kicad-jlcpcb-tools`](https://github.com/Bouni/kicad-jlcpcb-tools)
- Python 3
- Java Runtime Environment (for [`freerouting/freerouting`](https://github.com/freerouting/freerouting))

```bash
$ git clone --recursive "https://github.com/zeriyoshi/picopico" "picopico"
$ cd "picopico"
$ pip install -r "requirements.txt"
```

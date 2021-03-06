# NCP81xxx-3St-LFPAK33-breakout
Breakout board for gate drivers like NCP81253 or NCP81161 with 3-state PWM input and FETs in LFPAK33 like the PSMN1R8-30MLH

![3D view](https://github.com/crteensy/NCP81xxx-3St-LFPAK33-breakout/blob/main/drv_lfpak33.png)

## Purpose
The purpose of this breakout board is to simplify BLDC ESC development by separating MCU and power stage on different boards. That way a proven gate driver/FET power stage can be used with different MCUs, or working code can be used with different power stages.

## Features
Inputs:
- active low enable for all gate drivers
- high side and low side inputs for each gate driver, wired to a pair of pull-up resistors to generate 3-state PWM with either) two plain open-drain outputs or) one plain open drain output for the low side and one resistive open drain output for the high side.

You can choose to connect the phase feedback voltage dividers to ground on J2 using a jumper or to bias them with an external voltage supply (1V2 has worked here). This feature was necessary to implement BLDC control with an ADC whose input range doesn't extend below ground (this was the case with PSoC6).

Outputs:
- Motor connections of course
- phase feedback voltage divider output.

## PCB design rules (if you want to get them made):
- Layers: 2
- smallest drill: 0.3 mm
- track width/spacing: 0.2 mm
so nothing special at all.


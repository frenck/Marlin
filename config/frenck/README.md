# Frenck's Marling Configuration

This is my personal config of the Community firmware for the Creality CR-6 SE
3D printer.

My Creality CR-6 SE has modifications, so you cannot use this firmware on
a factory state printer. I've swapped the following parts:

- Mainboard: [BigTreeTech BTT SKR-CR6 v1.0](https://www.bigtree-tech.com/products/btt-skr-cr6-v1-0.html)
- Display: [BigTreeTech BTT TFT70 V3.0](https://www.biqu.equipment/products/btt-tft43-v3-0-tft50-v3-0-tft70-v3-0-display-touch-screen-two-working-modes)
- Bowden tube: Capricorn XS Ultra-Low Friction PTFE

This repository contains my personal settings and preferences, but is also used
to contribute back upstream if needed.

Current changes in here for my personal taste:

- Custom version/names
- Set serial baudrate to 250000
- Tweak PID tuning hotend
- Enable PID edit menu
- Tweak PID tuning bed
- Tweak E steps
- Tweak acceleration for printing moves
- Reduce retract acceleration, unneeded fast, makes noise
- Enable S-Curve Acceleration
- Tweak PLA preheat settings
- Enable advanced OK + increase buffers

Use at your own risk.

../Frenck

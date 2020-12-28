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

Current changes in here for my personal taste (found in the `./config/frenck`
folder)

- Custom version/names
- Set serial baudrate to 250000
- Enable PID edit menu
- Reduce retract acceleration, unneeded fast, makes noise
- Enable S-Curve Acceleration
- Enable advanced OK + increase buffers
- Tweak PID tuning hotend & bed
- Tweak E steps
- Tweak acceleration for printing moves
- Tweak PLA preheat settings

Use at your own risk.

../Frenck

# CR-6 community configuration examples

You can find various example configurations in the sub-directories.

The following examples are available: 

**For the CR-6 SE:**

- [BTT SKR CR6 with BTT TFT](./btt-skr-cr6-with-btt-tft)
- [BTT SKR CR6 with Creality stock TFT](./btt-skr-cr6-with-stock-creality-tft)

- [With v4.5.2 motherboard](./cr6-se-v4.5.2-mb)
- [With v4.5.3 motherboard](./cr6-se-v4.5.3-mb)

**For the CR-6 MAX:**

- [With stock v4.5.3 motherboard](./cr6-max-stock-mb)
- [BTT SKR CR6 with BTT TFT](./cr6-max-btt-skr-cr6-with-btt-tft)
- [BTT SKR CR6 with Creality stock TFT](./cr6-max-btt-skr-cr6-with-stock-creality-tft)

## Helper scripts

There are some helper scripts. You need Powershell Core (`pwsh`) to run them.

### Generating configuration examples
To generate or update a configuration example, do the modifications and then run:

    scripts/Generate-ConfigExample.ps1 -Name MyExampleName

### Applying configuration examples
To apply a configuration example, just copy the `Configuration*` files from the example directory to the "Marlin" directory.

### Maintenance

To refresh configuration examples (repository maintainers):

    scripts/Update-ConfigExamples.ps1

This script essentially runs an update on all configuration examples based on the changes of the current configuration (diff).

### Run builds

To run builds for all examples (repository maintainers):

    scripts/Run-ExampleConfigBuilds.ps1 -TouchscreenRepositoryPath [path to cr6 touch screen repository]

This script is meant to be executed in the VSCode console and in preperation for firmware release.

#### How it works

The base configuration for this repository is based on the most common hardware configuration: The Creality CR-6 SE with v4.5.2 motherboard. All other configurations are derived from that configuration. Using diff files the original configuration can be amended, then built.
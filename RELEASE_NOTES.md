# Frequenz Python SDK Release Notes

## Summary

<!-- Here goes a general summary of what this release is about -->

## Upgrading

<!-- Here goes notes on how to upgrade from previous versions, including deprecations and what they should be replaced with -->

## New Features

<!-- Here goes the main new features and examples or instructions on how to use them -->

## Bug Fixes

- Fixes a bug in the ring buffer updating the end timestamp of gaps when they are outdated.
- Properly handles PV configurations with no or only some meters before the PV
  component.
  So far we only had configurations like this: Meter -> Inverter -> PV. However
  the scenario with Inverter -> PV is also possible and now handled correctly.
- Fix `consumer_power()` not working certain configurations.
  In microgrids without consumers and no main meter, the formula
  would never return any values.

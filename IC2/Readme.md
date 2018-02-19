# Industrial Craft 2

## General

This section is available to the following device:

> component.ic2_te_semifluid_generator
>
> component.ic2_te_rt_generator
>
> component.ic2_te_stirling_generator
>
> component.ic2_te_geo_generator
>
> component.ic2_te_wind_generator
>
> component.ic2_te_electric_kinetic_generator
>
> component.ic2_te_solar_generator
>
> component.ic2_te_electric_heat_generator
>
> component.ic2_te_kinetic_generator
>
> component.ic2_te_generator
>
> component.ic2_te_water_generator
>
> component.ic2_te_condenser
>
> component.ic2_te_fluid_regulator
>
> component.ic2_te_pump
>
> component.ic2_te_fluid_bottler
>
> component.ic2_te_canner
>
> component.ic2_te_magnetizer
>
> component.ic2_te_terraformer
>
> component.ic2_te_extractor
>
> component.ic2_te_compressor
>
> component.ic2_te_sorting_machine
>
> component.ic2_te_electric_furnace
>
> component.ic2_te_solid_canner
>
> component.ic2_te_macerator
>
> component.ic2_te_block_cutter
>
> component.ic2_te_centrifuge
>
> component.ic2_te_induction_furnace
>
> component.ic2_te_recycler

If device is invalid or not supported, use `component.ic2_te_invalid` instead.

> Lamp,Tesla Coil

```Lua
address -- Address of device
type    -- component name
slot    -1

getSinkTier function

getCapacity function

getSourceTier   function

getEnergy   function
```

## Reactor

This section is available to the following device:

> component.reactor
>
> component.reactor_redstone_port

```Lua
address -- Address of device
type    reactor_redstone_port
slot    -1

producesEnergy  function():boolean -- Get whether the reactor is active and supposed to produce energy.

getReactorEnergyOutput  function():number -- Get the reactor's energy output. Not multiplied with the base EU/t value.

getReactorEUOutput  function():number -- Get the reactor's base EU/t value.

getMaxHeat  function():number -- Get the reactor's maximum heat before exploding.

getHeat function():number -- Get the reactor's heat.
```

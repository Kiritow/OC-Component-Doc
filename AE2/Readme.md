# Applied Energistics 2

## component.me_controller

Block: ME Controller

Adapter: Yes

```Lua
address -- Address of device
slot    -1
type    me_controller

getAvgPowerInjection    function():number -- Get the average power injection into the network.

getEnergyStored function():number -- Returns the amount of stored energy on the connected side.

store   function(filter:table, dbAddress:string[, startSlot:number[, count:number]]): Boolean -- Store items in the network matching the specified filter in the database with the specified address.

getAvgPowerUsage    function():number -- Get the average power usage of the network.

getIdlePowerUsage   function():number -- Get the idle power usage of the network.

canExtract  function():number -- Returns whether this component can have energy extracted from the connected side.

getCraftables   function([filter:table]):table -- Get a list of known item recipes. These can be used to issue crafting requests.

getCpus	function():table -- Get a list of tables representing the available CPUs in the network.

getItemsInNetwork   function([filter:table]):table -- Get a list of the stored items in the network.

canReceive  function():number -- Returns whether this component can receive energy on the connected side.

getMaxStoredPower   function():number -- Get the maximum stored power in the network.

getStoredPower  function():number -- Get the stored power in the network. 

getFluidsInNetwork  function():table -- Get a list of the stored fluids in the network.

getMaxEnergyStored  function():number -- Returns the maximum amount of stored energy on the connected side.
```

## component.energy_device

Block: Energy Acceptor

Adapter: Yes

```Lua
address -- Address of device
type    energy_device
slot    -1

canExtract  function():number -- Returns whether this component can have energy extracted from the connected side.

getMaxEnergyStored  function():number -- Returns the maximum amount of stored energy on the connected side.

getEnergyStored function():number -- Returns the amount of stored energy on the connected side.

canReceive  function():number -- Returns whether this component can receive energy on the connected side.
```

## component.me_interface

Block: ME Interface

Adapter: Yes

```Lua
address -- Address of device
type    me_interface
slot    -1

getCraftables   function([filter:table]):table -- Get a list of known item recipes. These can be used to issue crafting requests.

getStoredPower  function():number -- Get the stored power in the network.

store   function(filter:table, dbAddress:string[, startSlot:number[, count:number]]): Boolean -- Store items in the network matching the specified filter in the database with the specified address.

getCpus function():table -- Get a list of tables representing the available CPUs in the network.

getAvgPowerUsage    function():number -- Get the average power usage of the network.

getFluidsInNetwork  function():table -- Get a list of the stored fluids in the network.

getMaxStoredPower   function():number -- Get the maximum stored power in the network.

setInterfaceConfiguration   function([slot:number][, database:address, entry:number[, size:number]]):boolean -- Configure the interface.

getIdlePowerUsage   function():number -- Get the idle power usage of the network.

getAvgPowerInjection    function():number -- Get the average power injection into the network.

getInterfaceConfiguration   function([slot:number]):table -- Get the configuration of the interface.

getItemsInNetwork   function([filter:table]):table -- Get a list of the stored items in the network.
```

## component.me_importbus

Block: ME ImportBus

Adapter: Yes

```Lua
address -- Address of device
type    me_importbus
slot    -1

getImportConfiguration  function(side:number[, slot:number]):boolean -- Get the configuration of the import bus pointing in the specified direction.

setImportConfiguration  function(side:number[, slot:number][, database:address, entry:number]):boolean -- Configure the import bus pointing in the specified direction to import item stacks matching the specified descriptor.
```

## component.me_exportbus

Block: ME ExportBus

Adapter: Yes

```Lua
address 10353f18-5c5d-4549-ae97-475334762b48
type    me_exportbus
slot    -1

setExportConfiguration  function(side:number[, slot:number][, database:address, entry:number):boolean -- Configure the export bus pointing in the specified direction to export item stacks matching the specified descriptor.

getExportConfiguration  function(side:number, [ slot:number]):boolean -- Get the configuration of the export bus pointing in the specified direction.

exportIntoSlot  function(side:number, slot:number):boolean -- Make the export bus facing the specified direction perform a single export operation into the specified slot.
```

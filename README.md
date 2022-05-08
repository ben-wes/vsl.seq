# vsl.seq
Pure Data (Pd) sequencer and control module with step velocities and multiple input/output/manipulation options

See help patch for explanation and examples.

Left outlet outputs step values. Right outlet outputs additional and contextual data.

## Creation parameters
* `length` from 1 to 32
* `height` to change visible range for better readability and usability
* `color` to add unreasonable beauty via decimal RGB syntax (e.g. `999` for white) or preset color names
* `grid` to rasterize vertical resolution to an integer range instead of float from 0..1
* `receiver` to set object's receiver address
* `sender` to set object's sender address
* `partition` to set partition groups' size for better readability

## Messages
* `set <index> <value> [<duration> <ease mode>]` for setting value with optional duration and ease-mode
* list of values with optional `<duration> <ease mode>` for setting all values
* `random` to output random value/index by value probability
* `seed` to reseed random (with optional seed number)
* `permute` with list of indices to reorder sliders/values
* `shuffle` to randomly reorder sliders/values
* `sort [-1]` to sort values in descending (default) or ascending (via additional `-1`) order
* `run <duration> [<callback receiver>]` to run through values with given cycle duration
* `stumble <duration> [<callback receiver>]` to stumble through values with given cycle duration - but with duration of each step according to its value
* `output` to output all values on right outlet (mainly intended to copy sequences to another sequencer)
* `sum` to output value sum on right outlet
* `reset` to reset all values

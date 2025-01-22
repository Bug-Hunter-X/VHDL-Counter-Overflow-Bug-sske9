# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL: an integer counter that overflows without proper handling. The provided `counter_bug.vhdl` code implements a simple counter, but it lacks a mechanism to prevent the `internal_count` signal from exceeding its defined range (0 to 15). This can lead to unexpected behavior or simulation errors.

The solution, `counter_solution.vhdl`, shows how to address this by adding a modulo operator to wrap the count around when it reaches the maximum value.  This prevents the overflow and ensures correct functionality.

## How to reproduce

1. Synthesize and simulate `counter_bug.vhdl`.  Observe the counter's behavior after it reaches 15.
2. Compare its behavior to the corrected version, `counter_solution.vhdl`.

## Lessons Learned

- Always carefully consider potential integer overflow in your VHDL code.
- Employ appropriate techniques, such as modulo operations or saturated arithmetic, to handle such situations gracefully.
- Thoroughly test your designs in simulation to uncover and correct these types of errors early in the development process.
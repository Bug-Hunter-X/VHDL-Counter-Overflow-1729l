# VHDL Counter with Overflow Handling

This repository demonstrates a potential overflow issue in a simple VHDL counter and provides a corrected version.

## Bug Description
The original `counter.vhdl` code implements a 4-bit counter.  It lacks overflow detection, meaning when the counter reaches its maximum value ("1111"), the next increment will result in an overflow and wrap around to "0000".  This behavior might be unintended, causing unexpected behavior in a larger design.

## Solution
The `counter_fixed.vhdl` code addresses the overflow by adding a check. When the counter reaches its maximum value, it remains there instead of wrapping around.

## How to Use
1.  Synthesize and simulate both `counter.vhdl` and `counter_fixed.vhdl` using your preferred VHDL simulator (e.g., ModelSim, GHDL).
2.  Observe the difference in behavior when the counter reaches its maximum value.

## Lessons Learned
Always consider potential overflow conditions in your designs, especially when dealing with counters or arithmetic operations. Add appropriate overflow checks or use saturating arithmetic to handle these situations gracefully.
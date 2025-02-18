# Intermittent Array Index Out of Bounds in Objective-C

This repository demonstrates a subtle Objective-C bug involving an array index that occasionally goes out of bounds. The bug is intermittent, making it challenging to debug.  The core issue is in the calculation of the array index, which can exceed the bounds under specific conditions.

## Bug Description
The `processArray` function attempts to access an array element using an index calculated within the loop.  However, due to a flaw in this calculation, the index can exceed the valid index range of the array, leading to unexpected behavior or a crash. The error is intermittent due to the unpredictable nature of the data being processed.

## Solution
The solution involves carefully reviewing and correcting the index calculation.  Boundary checks should always be implemented to ensure that the array index is never greater than or equal to the array's count and never less than zero.
# Package Sorting Function

This project implements a function called `sort(width, height, length, mass)` that determines how a package should be classified based on its dimensions and weight.

## Classification Rules

A package is evaluated based on the following criteria:

### Bulky
A package is considered **bulky** if:

- Its volume (`width * height * length`) is greater than or equal to **1,000,000 cm³**, **or**
- Any one of its dimensions (`width`, `height`, or `length`) is greater than or equal to **150 cm**

### Heavy
A package is considered **heavy** if:

- Its mass is **greater than or equal to 20 kg**

### Sorting Output

Based on the above conditions, the function must return one of the following:

| Condition | Output |
|----------|--------|
| Heavy AND bulky | `REJECTED` |
| Heavy OR bulky | `SPECIAL` |
| Neither heavy nor bulky | `STANDARD` |

## Error Handling

The function raises a `ValueError` if:

- Any dimension is less than or equal to 0
- Mass is less than or equal to 0

This ensures invalid or physically impossible package data is not processed.

## Big-O Complexity Analysis

This function runs in **constant time** and uses **constant space**.

- **Time Complexity: O(1)**  
  The function performs a fixed number of comparisons and arithmetic operations, regardless of input values. There are no loops or recursive calls.

- **Space Complexity: O(1)**  
  The function uses a constant amount of memory for a few variables and does not allocate additional space based on input size.

## Test Coverage

The included tests validate:

- Standard packages
- Special cases (heavy only, bulky only by volume, bulky only by dimension)
- Rejected packages
- Boundary conditions
- Invalid input handling through exception testing

All logic paths are tested to ensure the implementation behaves as expected.


# Off-by-one error in vector iteration
This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.
The bug is in the for loop's condition: `i <= vec.size()`.  Vectors are zero-indexed, so the last valid index is `vec.size() - 1`. Accessing `vec[vec.size()]` results in undefined behavior.
The solution demonstrates the correct way to iterate using `<` instead of `<=`.
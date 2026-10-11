# Sorting Fixed-Length Social Media IDs

## Problem Statement
A social media application needs to sort these fixed-length IDs in ascending order:

`324, 125, 456, 218, 102, 389, 275, 147`

This project implements Merge Sort and Quick Sort, shows their sorted output, records the execution trace, and compares their time complexity and additional space.

## Project Files
- `merge_sort.c` — Merge Sort implementation.
- `quick_sort.c` — Quick Sort implementation (last element as pivot).
- `analysis.txt` — Execution traces and algorithm comparison.

## Expected Output
Both programs produce:

`102 125 147 218 275 324 389 456`

## Compile and Run
Using GCC:

```bash
gcc merge_sort.c -o merge_sort
./merge_sort
```

```bash
gcc quick_sort.c -o quick_sort
./quick_sort
```

On Windows, run `merge_sort.exe` or `quick_sort.exe` after compilation.

## Complexity Summary

| Algorithm | Best | Average | Worst | Extra space |
|---|---|---|---|---|
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) |
| Quick Sort | O(n log n) | O(n log n) | O(n^2) | O(log n) average recursion space; O(n) worst case |

## Conclusion
Merge Sort is a good choice when guaranteed O(n log n) performance and stability are important. Quick Sort often performs well in practice and usually needs less auxiliary memory, but its worst case is O(n^2). For fixed-length numeric IDs where digit-by-digit sorting is required, Radix Sort is also worth considering.

# Producer-Consumer-Instances
This repository contains the benchmark instances used in: Gupta, S.D., Simonis, H., Quesada, L. and O'Sullivan, B., 2025, November. Producer/Consumer Problems. In 2025 IEEE 37th International Conference on Tools with Artificial Intelligence (ICTAI) (pp. 363-370). IEEE.

### Main Benchmark Set: folders `val1/` through `val10/`

These folders contain instances of varying problem sizes used for scalability analysis.

- **Instance sizes**: 10 different sizes with producers/consumers ranging from 5 to 50 (increments of 5)
- **Organization**: 
  - `val1/`: 10 instances with 5 producers and 5 consumers
  - `val2/`: 10 instances with 10 producers and 10 consumers
  - `val3/`: 10 instances with 15 producers and 15 consumers
  - ...
  - `val10/`: 10 instances with 50 producers and 50 consumers
- **Total**: 100 instances (10 sizes × 10 instances per size)

### Constraint Ordering Variation Set: `size50folder/` and `varcon1/` through `varcon10/`

These folders contain instances used to compare Algorithm 1 and Algorithm 3 performance with respect to soft constraint ordering.

- **`size50folder/`**: 10 base instances with 50 producers and 50 consumers, each with a fixed constraint ordering
- **`varcon1/` through `varcon10/`**: Each folder corresponds to one base instance from `size50folder/` and contains 10 variants where the soft constraints are reordered
- **Total**: 10 base instances + 100 variants (10 base × 10 orderings each)

## Instance Format

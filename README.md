# Producer-Consumer-Instances
This repository contains the benchmark instances used in: Gupta, S.D., Simonis, H., Quesada, L. and O'Sullivan, B., 2025, November. Producer/Consumer Problems. In 2025 IEEE 37th International Conference on Tools with Artificial Intelligence (ICTAI) (pp. 363-370). IEEE.

### Main Benchmark Set: folders `val1/` through `val10/`

These folders contain instances of varying problem sizes used for scalability analysis.

- **Instance sizes**: 10 different sizes with producers/consumers ranging from 5 to 50 (increments of 5). 
- **Organization**: 
  - `val1/`: 10 instances with producers and consumers varying from 5 to 50
  - `val2/`: 10 instances with producers and consumers varying from 5 to 50
  - `val3/`: 10 instances with producers and consumers varying from 5 to 50
  - ...
  - `val10/`: 10 instances with producers and consumers varying from 5 to 50
- **Total**: 100 instances (10 sizes × 10 instances per size)

### Constraint Ordering Variation Set: `size50folder/` and `varcon1/` through `varcon10/`

These folders contain instances used to compare Algorithm 1 and Algorithm 3 performance with respect to soft constraint ordering.

- **`size50folder/`**: 10 base instances with 50 producers and 50 consumers, each with a fixed constraint ordering
- **`varcon1/` through `varcon10/`**: Each folder corresponds to one base instance from `size50folder/` and contains 10 variants where the soft constraints are reordered
- **Total**: 10 base instances + 100 variants (10 base × 10 orderings each)

## Instance Format
Instances contain the following decision variables:
### Variable: `start` correspond to start time
### Variable: `end` correspond to end time
### Variable: `maxQ` correspond to maximum quantity
### Variable: `num_producers` correspond to number of producers
### Variable: `num_consumers` correspond to number of consumers
### Variable: `n_sconsts` correspond to number of soft constraints
### Variable: `n_hconsts` correspond to number of hard constraints
### Variable: `qC` correspond to consumer quantities
### Variable: `sconsts/hconsts` correspond to the soft and hard constraints
```
sconsts=[|1,1,9|1,2,18|1,3,19|3,1,7|3,2,10|3,3,28|4,1,0|];
hconsts=[|2,1,7|2,2,7|2,3,29|];
```

Each tuple `[x,y,z]` is separated by `|` and represents:
- **First index (x)**: Entity type
  - `1` = producer arrival time
  - `2` = consumer quantity
  - `3` = consumer start time
  - `4` = safety margin
- **Second index (y)**: Entity ID (which producer/consumer)
  - For producers (i=1): y-th producer (e.g., y=2 means Producer 2)
  - For consumers (i=2): y-th consumer (e.g., y=5 means Consumer 5)
- **Third index (z)**: Quantity value for that entity

**Example:** `[1,2,3]` → Producer 2 has arrival time 3 

# Independent-Research-MPI-Performance-Evaluation-in-WSL2

## Overview

This project investigates the performance of parallel and distributed computing workloads in a single-machine WSL2 environment. Using Python, the project evaluates task execution time, throughput, and correctness under different workload sizes.

The aim is to explore how workload size affects performance and to establish a foundation for further experiments involving different process counts and MPI-based parallel execution.

## Objectives

Evaluate performance across different workload sizes.

Measure execution time and task throughput.

Verify the correctness of task processing.

Explore the effects of parallel execution on performance.

Document the experimental environment and results for reproducibility.

Experimental Environment

Operating System: Ubuntu on Windows Subsystem for Linux 2 (WSL2)

Programming Language: Python

Parallel Computing Technology: MPI / Open MPI (for MPI-specific experiments)

Compiler: GCC

Platform: Single-machine environment

## Methodology

The experiments use Python programs to process workloads of different sizes. Performance is evaluated using execution time, throughput (tasks per second), and the number of correctly processed tasks.

The initial workload tests include 100, 1,000, 10,000, and 50,000 tasks. Further experiments can compare different process counts to investigate parallel performance and overhead.

## Results

The initial Python client-server benchmark produced the following results:

| Number of Tasks | Correct Tasks | Execution Time (seconds) | Throughput (tasks/second) |
| ---: | ---: | ---: | ---: |
| 100 | 100 | 0.0089 | 11240.01 |
| 1000 | 1000 | 0.0502 | 19926.59 |
| 10000 | 10000 | 0.4637 | 21563.47 |
| 50000 | 50000 | 2.3628 | 21161.63 |

All tasks were processed correctly in these tests. Throughput increased with workload size initially and then remained relatively stable.

**Note:** These results are from the initial Python client-server benchmark, not MPI-specific performance measurements. MPI performance results will be reported separately after dedicated MPI experiments are completed.


## Project Structure



## Limitations

The current experiments run on a single machine under WSL2. Their results may be affected by system resources, virtualization overhead, and communication costs. They should not be treated as representative of a multi-node HPC cluster.

The initial Python client-server benchmark is separate from MPI-specific performance testing. Conclusions about MPI scalability require dedicated MPI experiments with documented process counts and repeated measurements.

Future Work

Conduct MPI-specific benchmarks using different process counts.

Repeat experiments to improve measurement reliability.

Compare execution time, throughput, and parallel overhead.

Visualize the results and investigate scalability.

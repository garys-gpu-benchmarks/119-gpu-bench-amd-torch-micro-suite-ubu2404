# Results: 119 PyTorch Microkernel Suite

**Main goal:** Measure PyTorch GEMM and Conv2d microkernel time, TFLOPS, and bandwidth  
**Tools:** Run the PyTorch microkernel suite through scripts/gemm.py and scripts/conv2d.py

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-12T23:15:11Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:55 · benchmark 00:09 · whole run 01:20
- **Source:** run 119_20261112_231511
- **Command:** `bash run_benchmark.sh --smoke --device-id 0 --dtype fp16 --input-shape 1,3,32,32 --M 64 --N 64 --K 64 --warmup-iters 2 --num-iterations 5 --seed 42`

| # | Metric | Result |
|---|---|---|
| 1 | GEMM execution time, us (gemm_time_usec) | 28.2334 |
| 2 | GEMM throughput, TFLOPS (gemm_tflops) | 0.01857 |
| 3 | GEMM minimum traffic, GB/s (gemm_bandwidth_gb_s) | 0.870458 |
| 4 | Conv2d execution time, us (conv_time_usec) | 50.5838 |
| 5 | Conv2d throughput, TFLOPS (conv_tflops) | 0.008745 |
| 6 | Conv2d minimum traffic, GB/s (conv_bandwidth_gb_s) | 0.4539 |
<!-- /profile:smoke -->

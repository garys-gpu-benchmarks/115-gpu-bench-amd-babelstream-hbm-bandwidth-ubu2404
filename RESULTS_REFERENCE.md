# Results: 115 BabelStream HBM Bandwidth

**Main goal:** Measure sustained BabelStream HBM bandwidth  
**Tools:** Build via scripts/build.sh if needed; run bin/hip-stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_142 · recorded 2026-11-16). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-16T11:13:25Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:12 · benchmark 00:02 · whole run 00:24
- **Source:** run 115_20261116_111325
- **Command:** `bash run_benchmark.sh --smoke --device-id 0 --block-size 256 --array-size 67108864 --warmup-iters 1 --num-iterations 20`

| # | Metric | Result |
|---|---|---|
| 1 | Copy bandwidth (bandwidth_gb_s_copy) | 3750.561 |
| 2 | Mul bandwidth (bandwidth_gb_s_mul) | 3810.155 |
| 3 | Add bandwidth (bandwidth_gb_s_add) | 3846.626 |
| 4 | Triad bandwidth (bandwidth_gb_s_triad) | 3869.54 |
| 5 | Dot bandwidth (bandwidth_gb_s_dot) | 1857.376 |
<!-- /profile:smoke -->

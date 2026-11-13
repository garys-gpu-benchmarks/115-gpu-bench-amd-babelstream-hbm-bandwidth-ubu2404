# Results: 115 BabelStream HBM Bandwidth

**Main goal:** Measure sustained BabelStream HBM bandwidth  
**Tools:** Build via scripts/build.sh if needed; run bin/hip-stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-12T23:03:28Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:12 · benchmark 00:02 · whole run 00:26
- **Source:** run 115_20261112_230328
- **Command:** `bash run_benchmark.sh --smoke --device-id 0 --block-size 256 --array-size 67108864 --warmup-iters 1 --num-iterations 20`

| # | Metric | Result |
|---|---|---|
| 1 | Copy bandwidth (bandwidth_gb_s_copy) | 3776.699 |
| 2 | Mul bandwidth (bandwidth_gb_s_mul) | 3754.909 |
| 3 | Add bandwidth (bandwidth_gb_s_add) | 3855.254 |
| 4 | Triad bandwidth (bandwidth_gb_s_triad) | 3858.239 |
| 5 | Dot bandwidth (bandwidth_gb_s_dot) | 2248.666 |
<!-- /profile:smoke -->

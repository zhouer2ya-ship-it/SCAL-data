# SCAL source data

[Figures](Figures/) contains the figure PDFs. [Source data](Source_Data/) contains the workbooks, CSV tables and NPZ arrays. The [file list](Files.csv) gives the files for each figure and table. ED denotes Extended Data and FigS denotes a Supplementary Figure.

## Data provenance

- **SRAM sense amplifier (Fig. 5).** SpreadT (北京宽温微电子科技有限公司, Beijing, China) provided the circuit simulation data for an SRAM sense amplifier designed in an advanced FinFET process. The response is the signed offset voltage, ΔV (mV).
- **Cerebral aneurysm (Fig. 6).** The Advanced Computing and Multi-media Mechanics (ACMM) Laboratory at Peking University, led by Prof. Moubin Liu, provided the smoothed particle hydrodynamics (SPH) simulation data for the cerebral aneurysm.

The plotted values for Supplementary Figures 2 and 6 are in `FigS2_Plot_Data.csv` and `FigS6_Paired_Differences.csv`. In the latter file, `control` gives the experiment key and `control_label` gives the figure label. `FigS2.xlsx` gives the underlying learning paths and basis diagnostics. `FigS6.xlsx` gives the four crossed trajectories and whole-path effects.

`FigS3.xlsx` gives the projection dictionary, persistent terms by seed and history decisions by sample size.

The `Sobol indices by input` sheet in [Fig5.xlsx](Source_Data/Fig5.xlsx) gives first-order and total Sobol indices and simulator input names for all 159 SRAM inputs.

In [Fig6.xlsx](Source_Data/Fig6.xlsx), `Field moment trajectories` gives the values for panel h. `Case errors and quantiles` gives the heatmap values for panel i and the paired spatial 99th percentiles for panel j at the final budget of 20 simulations. `Map geometry` gives the camera, crop bounds and fixed location. [Fig6_Maps.npz](Source_Data/Fig6_Maps.npz) gives coordinates, spatial IDs and field values, including the case 8 arrays used in panel k.

For panel l, `Fixed point test cases` gives the paired stress values for the 30 tests. `Exceedance curve` gives the probabilities and their interval bounds across thresholds. The grey band in the figure shows the pointwise 95% binomial intervals for the SPH reference fractions. The Monte Carlo intervals in the workbook quantify integration precision for 1,000,000 draws from the input law evaluated with the fixed surrogate.

In `Supplementary_Tables.xlsx`, the sheets `Table 2A component effects` and `Table 2B crossed effects` support Supplementary Table 2. The `Fixed-design recovery` sheet gives the endpoint results for Supplementary Table 3. `Timing_Summary.csv` and `Timing_By_Seed.csv` give the timings described in Supplementary Note 2.

## SCAL software

The SCAL Python implementation, documentation and usage examples are publicly available on GitHub under the BSD 3-Clause License. The repository includes a self-contained Ishigami example and instructions for using SCAL with Python functions and external simulators. [SCAL repository](https://github.com/zhouer2ya-ship-it/SCAL-code) · [Installation and examples](https://github.com/zhouer2ya-ship-it/SCAL-code/blob/main/docs/QUICKSTART.md) · [Software license](https://github.com/zhouer2ya-ship-it/SCAL-code/blob/main/LICENSE)

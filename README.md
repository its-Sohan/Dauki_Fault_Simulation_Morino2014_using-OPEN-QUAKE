# Dauki Fault Simulation — Morino et al. (2014) using OpenQuake

Probabilistic seismic hazard and risk assessment for the Dauki Fault region (Bangladesh), based on the fault parameters from **Morino et al. (2014)** and computed with the [OpenQuake](https://github.com/gem/oq-engine) engine.

*A paleo-seismological study of the Dauki fault at Jaflong, Sylhet, Bangladesh: Historical seismic events and an attempted rupture segmentation model* — [ResearchGate](https://www.researchgate.net/figure/a-An-active-fault-map-of-Bangladesh-The-Dauki-fault-passes-along-the-southern-margin_fig1_263391442)

## Contents

| File | Description |
|------|-------------|
| `Dauki_Fault_Simulation_Morino2014.ipynb` | Jupyter notebook with the full analysis workflow |
| `source_model.xml` | Seismic source model (point source) |
| `source_model_logic_tree.xml` | Source model logic tree |
| `gmpe_logic_tree.xml` | Ground-motion prediction equation logic tree |
| `exposure.xml` | Exposure model (buildings/inventory) |
| `vulnerability.xml` | Vulnerability functions |
| `site_model.csv` | Site amplification parameters (Vs30, etc.) |
| `job_hazard.ini` | OpenQuake job configuration — hazard calculation |
| `job_risk.ini` | OpenQuake job configuration — risk calculation |
| `exports/` | Computed hazard curves, hazard maps, uniform hazard spectra, and loss curves |

## Usage

1. Install [OpenQuake engine](https://github.com/gem/oq-engine).
2. Run hazard:  
   `oq engine --run job_hazard.ini`
3. Run risk:  
   `oq engine --run job_risk.ini`
4. Export results:  
   `oq engine --export-outputs`

## Reference

Morino, M., Kamal, A. S. M. M., Akhter, S. H., Rahman, M. Z., Ali, R. M. E., Talukder, A., & Kaneko, Y. (2014). *A paleo-seismological study of the Dauki Fault at Jaflong, Sylhet, Bangladesh: Implications for hazard assessment.* Journal of Asian Earth Sciences, 91, 263–271.

## <img src="./../../logo/lbnl_logo.png" alt="logo" width="150"/> Teststand overview 
This is an overview of the LBNL teststand `ppc01` measurements. For more details on the individuals runs, see the readme files in this directory. 

The follow the following naming scheme: `readme_<period>_<runs>.md`.  

<style>
@media (prefers-color-scheme: dark) {
  .logo-inline {
    content: url("./../../logo/lbnl_logo_dark.png");
  }
}
</style>

## Overview table: period 1 `p01`: ASIC + Oscilloscope
All runs in this period are taken this the **ASIC L1k65n**. 
|                   |                 |            |            |                                                                                                              |
| :---------------- | :-------------- | :--------- | :--------- | :----------------------------------------------------------------------------------------------------------- |
| **runs**          | **# waveforms** | **buffer** | **cables** | **short description**                                                                                        |
| `r001`            | 9,677           | no         | short      |                                                                                                              |
| `r002`            | 3,000           | yes        | short      | super-capacitors + LDO  were continuously charged throughout the measurement                                 |
| `r003`            | 45,328          | yes        | short      | same as  run 2, but more waveforms                                                                           |
| `r004`, `r005`    | -               | yes        | short      | recorded in `.wfm` (instead of `.csv`), not used.                                                            |
| `r006` -   `r013` | 3,000  each     | yes        | short      | Detector voltage `1.3 kV` - `3.0 kV`  , super-capacitors + LDO pre-charged; disconncected during measurement |
| `r014`            | 10,659          | yes        | short      | Detector voltage `2.5 kV`, high stats.   data taking took much longer than expected. Stable ASIC voltage ?   |
|                   |                 |            |            |                                                                                                              |



## Overview table: period 2 `p02`: GFET + Oscilloscope
All runs in this period are taken this the **GFET  xxx**. 
|          |                 |              |                       |
| :------- | :-------------- | :----------- | :-------------------- |
| **runs** | **# waveforms** | **duration** | **short description** |
| `r001`   | 4,279           | `131.072 µs` |        `t0 ≈ 23 µs`               |
| `r002`   | 16,383          | `131.072 µs` |                       |
| `r003`   | 8,000           | `131.056 µs` |                       |
| `r004`   | 4,000           | `199.984 µs` | `t0 ≈ 40 µs`          |
|          |                 |              |                       |


## Overview table: period 3 `p03`: ASIC + Vireo
All runs in this period are taken this the **ASIC L1k65n** (same as `p01`). In constrast to `p01` this dataset was recorded using a digitizer **SkuTek FemtoDAQ Vireo** instead of the oscilloscope. 
|                |                    |            |              |                                                                        |
| :------------- | :----------------- | :--------- | :----------- | :--------------------------------------------------------------------- |
| **runs**       | **# waveforms**    | **buffer** | **cables**   | **short description**                                                  |
| `r001`         | 5,000              | yes        | short        | first test                                                             |
| `r002`         | 100,000            | yes        | short        | first higher stat. data                                                |
| `r003`-`r014`  | 3,000              | yes        | short        | Optimization of DAQ Parameters                                         |
| `r015`-`r016`  | 3,000              | yes        | short        | Check for decay time with longer charge-time for Capasitor             |
| `r017`-`r026`  | 5,000              | yes        | short        | Optimization of DAQ prameters                                          |
| `r027`-`r030`  | 5,000 or 50,000    | yes        | ~4m          | With longer cables                                                     |
| `r031`-`r036`  | 50,000             | yes        | ~4m and 2m   | Comparison of different cable-lengths under same setting               |
| `r037`-`r038`  | 3,000              | yes        | 2m           | reference data for decay time constant under 90.5K                     |
| `r039`-`r041`  | 50,000             | yes        | 2m, 4m, 6.4m | Examine influence of cable length on the energy resolution under 90.5K |
| `r042`-`r044`  | 100,000            | yes        | 2m, 4m, 6.4m | 100,000 samples to reduce statistical errors                           |
| `r045`         | 50,000             | yes        | 185 cm       | th228 source. trigger 200 ADC                                          |
| `r046`         | 5,000              | yes        | 185 cm       | th228 source. trigger 860 ADC                                          |
| `r047`         | 5,000              | yes        | 185 cm       | welding rods as th228 source. trigger  400 ADC                         |
| `r048`         | 5,000              | yes        | 185 cm       | th228 source. trigger 400 ADC                                          |
| `r049`, `r050` | 5,000  and 100,000 | yes        | 185 cm       | th228 source. trigger 350 ADC                                          |
| `r051`         | 100,000            | yes        | 405 cm cable | th228 source. trigger 350 ADC                                          |
| `r052`         | 100,000            | yes        | 645 cm cable | th228 source. trigger 350 ADC                                          |
|                |                    |            |              |                                                                        |


## <img src="./../../logo/lbnl_logo.png" alt="logo" width="150"/> Teststand overview  - `bch` (benchtest)
This is an overview of the LBNL teststand `ppc01` measurements. For more details on the individuals runs, see the readme files in this directory. 
The follow the following naming scheme: `readme_<category>_<period>_<runs>.md`.  

<style>
@media (prefers-color-scheme: dark) {
  .logo-inline {
    content: url("./../../logo/lbnl_logo_dark.png");
  }
}
</style>

## Overview table: period 1 `p01`   
All runs in this period are taken this the **ASIC L1k65n + buffer**. The Germanium detector is not connected. For more detail, see `readme_bch_p01.md`
|               |                 |                 |            |                                                  |
| :------------ | :-------------- | :-------------- | :--------- | :----------------------------------------------- |
| **runs**      | **# waveforms** | **temperature** | **cables** | **short description**                            |
| `r001 - r010` |                 | 295 K (room)    | 185 cm     | linearity data                                   |
| `r011`        |                 | 295 K (room)    | 185 cm     | noise run                                        |
| `r012`        |                 | 90 K            | 185 cm     | noise run                                        |
| `r013 - r022` |                 | 90 K            | 185 cm     | linearity data                                   |
| `r023 - r032` |                 | 90 K            | 185cm      | linearity data with improved termination         |
| `r33`         |                 | 90.3 K          | 185cm      | noise run with terminated pulser and diff output |
|               |                 |                 |            |                                                  |



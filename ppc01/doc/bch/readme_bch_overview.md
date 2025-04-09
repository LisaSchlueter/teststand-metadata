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
|               |                  |                 |            |                                                                           |
| :------------ | :--------------- | :-------------- | :--------- | :------------------------------------------------------------------------ |
| **runs**      | **# waveforms**  | **temperature** | **cables** | **short description**                                                     |
| `r001 - r010` | 5,000 (each)     | 295 K (room)    | 185 cm     | linearity data                                                            |
| `r011`        | 100,000          | 295 K (room)    | 185 cm     | noise run                                                                 |
| `r012`        | 100,000          | 90 K            | 185 cm     | noise run                                                                 |
| `r013 - r022` | 5,000 (each)     | 90 K            | 185 cm     | linearity data                                                            |
| `r023 - r032` | 5,000 (each)     | 90 K            | 185cm      | linearity data with improved termination                                  |
| `r033 - r038` | 5,000 to 100,000 | 90.3 K          | 185cm      | noise runs      **pulser cap was not connected - CSA input was grounded!** |
|               |                  |                 |            |                                                                           |

##  period 2 `p02`   
This data was taken **before** period 1, in summer 2024 by Damien Bowen during his summer internship. Back then, the data strucutre didn't follow the period/run strucutre. It was integrated into the current structure at a later time. All runs in this period are taken this the **ASIC L1k65n without buffer**. For more detail, see `readme_bch_p02.md`
|          |                 |                 |               |                 |             |                |                                    |
| :------- | :-------------- | :-------------- | :------------ | :-------------- | :---------- | :------------- | :--------------------------------- |
| **runs** | **# waveforms** | **temperature** | **amp. gain** | **C inj. (fF)** | **Cf (fF)** | **comment**    | **old name**                       |
| `r001`   | 100             | 300 K (room)    | 48.0          | 3,000           | 500         | LDO + supercap | `noise-3pF_300K_2MHz_LDO_SUPERCAP` |
| `r002`   | 100             | 300 K (room)    | 48.0          | 3,000           | 500         | LDO            | `noise-3pF_300K_2MHz_LDO`          |
| `r003`   | 10              | 300 K  (room)   | 100.0         | 3,000           | 500         |                | `NOISE_10162024_3pF_300K`          |
| `r004`   | 10              | 77 K            | 100.0         | 3,000           | 500         |                | `NOISE_10162024_3pF_77K`           |
|          |                 |                 |               |                 |             |                |                                    |


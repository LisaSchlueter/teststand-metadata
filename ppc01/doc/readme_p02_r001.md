## <img src="./../../logo/lbnl_logo.png" alt="logo" width="150"/> Teststand data 
LBNL measurement protocol 

<style>
@media (prefers-color-scheme: dark) {
  .logo-inline {
    content: url("./../../logo/lbnl_logo_dark.png");
  }
}
</style>

## General measurement information
| | |
|:----------------| :----------------|
| Setup name | `ppc01`|
| period | 2 | 
| run | 1 - 4 | 
| Location | LBNL, building 70,  room 70-141 |
| Date of measurement (yyyy-mm-dd) | 2025-01-15 | 
| Operator | Marcos Turqueti, Lisa Schlueter, Ryutaro Matsumoto | 
| Goal of measurement | Characterization of GFET |
| | |

## Experimental setup description
Germanium detector in vaccum cryostat at pressure: `8e-8 hPa (8e-11 bar)`.
Cooled via cold finger in liquid nitrogen dewar to `~90.2 K`. 

## Germanium detector
| | |
|:----------------| :----------------|
| Type | PPC | 
| Name | `DetectorId(:LBNL_PP01)` / `ChannelId(1)` | 
| Operation voltage |  2.44 kV (fully depleted) | 
| | |

## Electronics
LBNL graphene GFET amplifier. 

## DAQ

| | |
|:----------------| :----------------|
|  |  | 
| Sample rate | `62.5 MHz` | 
| Number of samples | `8192` | 
| Waveform length | `131.072 µs` |
| Trigger threshold | `0.1 V` |
| Resolution | `16` bit |
| Coupling mode | `AC coupled` | 
| | |
## Remarks and comments
Period 3 and 4 are longer and have different `t0`. 
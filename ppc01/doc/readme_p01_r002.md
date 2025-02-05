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
| period | 1 | 
| run | 2 | 
| Location | LBNL, building 70,  room 70-141 |
| Date of measurement (yyyy-mm-dd) | 2025-02-05 | 
| Operators | Marcos Turqueti, Lisa Schlueter, Ryutaro Matsumoto | 
| Goal of measurement | Characterization of ASIC with **buffer** (but without long cables) |
| | |

## Experimental setup description
Germanium detector in vaccum cryostat. Cooled via cold finger in liquid nitrogen dewar to ~90K. 


## Germanium detector
| | |
|:----------------| :----------------|
| Type | PPC | 
| Name | `DetectorId(:LBNL_PP01)` / `ChannelId(1)` | 
| Operation voltage | 2.5 kV (fully depleted) | 
| | |

## Radioactive source
Co-60. Placed on top of vacuum cryostat with some styrofoam plates as distance keepers. 

## Electronics
LBNL ASIC `l1k65n`. Board `A`. The **buffer** is activated and we make use of the differential output. The positive and negative output waveforms are subtracted frmo each other.

## DAQ
Oscilloscope Tektronix MSO44B. We record analog waveform signals.

| | |
|:----------------| :----------------|
|  |  | 
| Sample rate | `62.5 MHz` | 
| Number of samples | `8192` | 
| Waveform length | `131.072 µs` |
| Trigger threshold | `0.XX V` |
| Resolution | `16` bit |
| Coupling mode | `DC coupled` | 
| Trigger position approx. | `19.6 µs` (`15%` of waveform lengths ) | 
| | |

## Remarks and comments



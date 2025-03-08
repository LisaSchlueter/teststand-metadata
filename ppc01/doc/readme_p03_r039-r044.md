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
| period | 3 | 
| runs | 39 - 44 | 
| Location | LBNL, building 70,  room 70-141 |
| Date of measurement (yyyy-mm-dd) | 2025-03-07  | 
| Operators | Ryutaro Matsumoto | 
| Goal of measurement | Characterization of ASIC with **buffer** with 2m, 4m, 6.4 cables  |
| | |

## Experimental setup description
Germanium detector in vaccum cryostat. The pressure was kept to `~ 1e-7 hPa` with a turbomolecular pump. The vacuum chamber is cooled via cold finger in liquid nitrogen dewar to `90.5~ 90.6 K`. 

## Germanium detector
|        |                                          |
| ------ | ---------------------------------------- |
| Type   | PPC                                      |
| Name   | `DetectorId(:LBNL_PP01)`  `ChannelId(1)` |
| Weight | `~ 900 g`                                |
| Bias voltage | `2.71 kV (± 0.02 kV) `. |
|        |                                          |

## Radioactive source
Co-60 10µCi. Placed on top of vacuum cryostat with 2 styrofoam plates as distance keepers. 

## Electronics
LBNL ASIC `l1k65n`. Board `A`. The **buffer** is activated and we make use of the differential output. The positive and negative output waveforms are subtracted frmo each other. We use a board with charged capacitors + LDO for the ASIC power supply. 
| | |
|:----------------| :----------------|
|||
| Name | `l1k65n` |
| Buffer | yes |
| Cables | `~2m(r039, r044) ~4m(r040, r043) / ~6.4m(r041, r042)` |
 `V_ref` | `+ 2.6 V` |

The reference voltage of the ASIC `V_ref` was provided by a stationary power supply (Keysight `E36313A`). To reduce noise 
we added a board with super-capacitors and LDOs between the ASIC and the power supply. The super-capacitors were pre-charged(with 3.8V) and then disconnected before the measurement to provide low-noise power to the ASIC.

## DAQ
Skutek Digitizer "FemtoDAQ Vireo". 
Used one of the optimal configuration of parameters.
| | |
|:----------------| :----------------|
|  |  | 
| Sample rate | `100 MHz` | 
| Number of samples | `4096` | 
| Waveform length | `40.96 µs` |
| Trigger threshold (ADC) | 200 (channel 0) |
| Resolution | `16` bit | 
| Pulse Height Window | `5.00`µs |
| Pulse Height Avaraging Window | `0.32`µs|
| Trigger Averaging Window | `0.32` µs |
| Coupling mode | `DC coupled` | 
| Trigger position approx. | `8 µs` | 
| Analog Offsets | `-5`, `-100`|
| Digital Offsets | `0`, `0`|
| | |

## Remarks and comments

|          |                 |                       |
| :------- | :-------------- | :-------------------- |
| **runs** | **# waveforms** | **comment** |
| `r039-041`   | 50,000/each      |  with 2, 4, 6.4m cables(this order) |
| `r042-044`   | 100,000/each         | with 6.4, 4, 2m cables(this order)   |



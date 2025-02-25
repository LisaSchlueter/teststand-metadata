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
| runs | 15 - 16 | 
| Location | LBNL, building 70,  room 70-141 |
| Date of measurement (yyyy-mm-dd) | 2025-02-24  | 
| Operators | Alexey Drobizhev, Ryutaro Matsumoto | 
| Goal of measurement | Finding out the reason why the decay-times of r003-r014 were around 395µs, which is slower than that of the last results: 282µs  |
| | |

## Experimental setup description
Germanium detector in vaccum cryostat. The pressure was kept to `~ 1e-7 hPa` with a turbomolecular pump. The vacuum chamber is cooled via cold finger in liquid nitrogen dewar to `91.7~ 91.9 K`. 

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
| Cables | `~ 2 m` |
 `V_ref` | `+ 2.6 V` |

The reference voltage of the ASIC `V_ref` was provided by a stationary power supply (Keysight `E36313A`). To reduce noise 
we added a board with super-capacitors and LDOs between the ASIC and the power supply. The super-capacitors were pre-charged and then disconnected before the measurement to provide low-noise power to the ASIC.

## DAQ
Skutek Digitizer "FemtoDAQ Vireo". 
| | |
|:----------------| :----------------|
|  |  | 
| Sample rate | `100 MHz` | 
| Number of samples | `4096` | 
| Waveform length | `40.96 µs` |
| Trigger threshold (ADC) | 200 (channel 0) |
| Resolution | `16` bit | 
| Pulse Height Window | `30.00`µs |
| Pulse Height Avaraging Window | `0.32`µs|
| Trigger Averaging Window | `0.16` µs|
| Coupling mode | `DC coupled` | 
| Trigger position approx. | `8 µs` | 
| | |

## Remarks and comments

|          |                 |                       |
| :------- | :-------------- | :-------------------- |
| **runs** | **# waveforms** | **comment** |
| `r015`   | 3000/ea         | Charged capasitor longer than before(Ic became 6mA), no change of decay time  |
| `r016`   | 3000/ea         | Removed thermal pins, which left connected through r003 - r015, no change of decay time(smaller diviation of 0.24µs) |


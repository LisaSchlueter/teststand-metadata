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
| runs | 6 - 10 | 
| Location | LBNL, building 70,  room 70-141 |
| Date of measurement (yyyy-mm-dd) | 2025-02-06 to 2025-02-10 | 
| Operators | Marcos Turqueti, Lisa Schlueter | 
| Goal of measurement | Characterization of ASIC with **buffer** (but without long cables). Find optimzal operating voltage of detector.  |
| | |

## Experimental setup description
Germanium detector in vaccum cryostat. The pressure was kept to `~ 1e-7 hPa` with a turbomolecular pump. The vacuum chamber is cooled via cold finger in liquid nitrogen dewar to `~ 90.0 K - 91.5 K`. 

## Germanium detector
|        |                                          |
| ------ | ---------------------------------------- |
| Type   | PPC                                      |
| Name   | `DetectorId(:LBNL_PP01)`  `ChannelId(1)` |
| Weight | `~ 900 g`                          |
|        |                                          |

We changed the detector (operation) voltage from run to run to find the voltage with full depletion. The voltage varied within a run by `± 0.02 V`.   
|         |                      |
| ------- | -------------------- |
| **Run** | **Detector voltage** |
| `r006`  | `1.3 kV`             |
| `r007`  | `1.6 kV`             |
| `r008`  | `1.9 kV`             |
| `r009`  | `2.2 kV`             |
| `r010`  | `2.5 kV`             |
| `r011`  | `2.7 kV`             |
| `r012`  | `2.9 kV`             |
| `r013`  | `3.0 kV`             |
|         |                      |

## Radioactive source
Co-60. Placed on top of vacuum cryostat with some styrofoam plates as distance keepers. 

## Electronics
LBNL ASIC `l1k65n`. Board `A`. The **buffer** is activated and we make use of the differential output. The positive and negative output waveforms are subtracted frmo each other. We use a board with charged capacitors + LDO for the ASIC power supply. 
| | |
|:----------------| :----------------|
|||
| Name | `l1k65n` |
| Buffer | yes |
| Long cables | no |
 `V_ref` | `+ 2.6 V` |

The reference voltage of the ASIC `V_ref` was provided by a stationary power supply (Keysight `E36313A`). To reduce noise 
we added a board with super-capacitors and LDOs between the ASIC and the power supply. The super-capacitors were pre-charged and then disconnected before the measurement to provide low-noise power to the ASIC.

## DAQ
Oscilloscope Tektronix MSO44B. We record analog waveform signals.

| | |
|:----------------| :----------------|
|  |  | 
| Sample rate | `62.5 MHz` | 
| Number of samples | `8192` | 
| Waveform length | `131.072 µs` |
| Trigger threshold | `70.4 mV` |
| Resolution | `16` bit |
| Coupling mode | `? coupled` | 
| Trigger position approx. | `19.6 µs` (`15%` of waveform lengths ) | 
| | |

## Remarks and comments



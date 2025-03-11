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
| runs | 45 - 52 | 
| Location | LBNL, building 70,  room 70-141 |
| Date of measurement (yyyy-mm-dd) | 2025-03-10 and 2025-03-11  | 
| Operators | Ryutaro Matsumoto, Lisa Schlueter | 
| Goal of measurement | Characterization of ASIC with **buffer** and **Th-228** source and different cable length |
| | |

## Experimental setup description
Germanium detector in vaccum cryostat. The pressure was kept to `~ 1e-7 hPa` with a turbomolecular pump. The vacuum chamber is cooled via cold finger in liquid nitrogen dewar to `90.5K - 90.8 K`. 

## Germanium detector
|        |                                          |
| ------ | ---------------------------------------- |
| Type   | PPC                                      |
| Name   | `DetectorId(:LBNL_PP01)`  `ChannelId(1)` |
| Weight | `~ 900 g`                                |
| Bias voltage | `2.71 kV (± 0.02 kV) `. |
|        |                                          |

## Radioactive source
Th-228 9.32 µCi (2/8/2023). LBNL Source Id `#HC6852` (from Alexey). Placed on top of vacuum cryostat with 2 styrofoam plates as distance keepers. 
In `r047`, we used a welding rod that contains Th-288 as an alternative source. However, we observed many additional gamma lines. That's why we went back to `#HC6852`.

## Electronics
LBNL ASIC `l1k65n`. Board `A`. The **buffer** is activated and we make use of the differential output. The positive and negative output waveforms are subtracted frmo each other. We use a board with charged capacitors + LDO for the ASIC power supply. 
|        |            |                  |
|        |  **runs**     | **Description**                       |
| :-----| :-----  | :--------------------------- |
| CSA   | all |`l1k65n`                     |
| Buffer | all |yes                          |
| Cables | `r045` - `r050` |  `185 cm `  |
|        |  `r051` |`405 cm`            |
 `V_ref` | all | `+ 2.6 V` |   

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
| Resolution | `14` bit | 
| Trigger Averaging Window | `0.32` µs |
| Coupling mode | `DC coupled` | 
| Trigger position approx. | `8 µs` | 
| Analog Offsets | `-10`, `-100`|
| Digital Offsets | `0`, `0`|
| Termination | `1 kΩ` 
| | | 


| runs | Trigger threshold (channel 0) in ADC |
| :---------------- | :----------------   |
| `r045`            | 200 |
| `r046`            | 860 |
| `r047`            | 400 |
| `r048`            | 400 |
| `r049` - `r052`   | 350 |
## Remarks and comments

|          |                 |                       |
| :------- | :-------------- | :-------------------- |
| **runs** | **# waveforms** | **comment** |
| `r045`   | 50,000      |  trigger threshold of 200 includes a lot of low-energy gammas, which are not useful for calibration |
| `r046`   | 5,000     |  set trigger threshold to 860 ADC (approx. 1000 keV) --> too high!  |
| `r047`   | 5,000     |  source: welding rods, trigger threshold = 400 ADC (~ 500 keV) --> a lot of additional gamma lines with this source.  |
| `r048`   | 5,000      |  back to proper Th228 source. trigger threshold to 4000 ADC. still a bit too high  |
| `r049`   | 5,000      |  trigger threshold to 350 ADC   |
| `r050`   | 100,000      |  same as `r049` with higher stat.   |
| `r051`   | 100,000      |  405 cm cable   |
| `r052`   | 100,000      |  645 cm cable   |


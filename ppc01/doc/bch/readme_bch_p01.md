## <img src="./../../logo/lbnl_logo.png" alt="logo" width="150"/> Teststand data 
LBNL measurement protocol for benchtest "`bch`"

<style>
@media (prefers-color-scheme: dark) {
  .logo-inline {
    content: url("./../../logo/lbnl_logo_dark.png");
  }
}
</style>

## General measurement information
|                                  |                                                    |
| :------------------------------- | :------------------------------------------------- |
| Setup name                       | `ppc01`                                            |
| period                           | 1                                                  |
| Location                         | LBNL, building 70,  room 70-141                    |
| Date of measurement (yyyy-mm-dd) | 2025-03-17                                         |
| Operators                        | Marcos Turqueti, Lisa Schlueter, Ryutaro Matsumoto |
| Goal of measurement              | Benchtest ASIC: Linearity and noise performance    |
|                                  |                                                    |

## Experimental setup description
- ASIC in vacuum chamber, but kept at atmospheric pressure (no vacuum). In this setup, the chamber is used for em-shielding. 
- Germanium detector is not connected to ASIC. 
- Pulser is direclty connected to the CSA. 
- For `90 K` measurements, the chamber is cooled via cold finger in liquid nitrogen dewar.

## Electronics
LBNL ASIC `l1k65n`. Board `A`. The **buffer** is activated and we make use of the differential output. The positive and negative output waveforms are subtracted frmo each other. We use a board with charged capacitors + LDO for the ASIC power supply. 

|        |  **runs**       | **Description** |
| :----- | :-----          | :---------------|
| CSA    | all             |`l1k65n`         |
| Buffer | all             | yes, but use only single output             |
| `V_ref`| all            | `+ 2.6 V` (super cap board)      |    

## Pulser
- capacitance `C = 500 fF` (outside of chamber. shielded with copper tape)
- pulse generator: TELEDYNE `T3AFG500`
  - frequency = `20 Hz` 
  - pulse width = `30 ms`
  - fall edge = `20 ms`
  - amplitude (peak-to-peak): varied

## DAQ
Skutek Digitizer "FemtoDAQ Vireo". 
Used one of the optimal configuration of parameters.
|                            |                                     |
| :------------------------- | :---------------------------------- |
|                            |                                     |
| Sample rate                | `100 MHz`                           |
| Number of samples          | `4096`                              |
| Waveform length            | `40.96 µs`                          |
| Resolution                 | `14` bit                            |
| Coupling mode              | `DC coupled`                        |
| channel 0                  | CSA output positive                 |
| channel 1                  | pulser                              |
| Analog Offsets (ch0, ch1)  | `-100`, `0`                         |
| Digital Offsets (ch0, ch1) | `0`, `0`                            |
| Termination                | `1 kΩ`                              |
| Trigger on                 | pulser                              |
| Trigger Averaging Window   | `0.32` µs                           |
| Trigger position approx.   | `8 µs`, exception: `r011 -> 40.9 µs` |
| Trigger threshold          | 500 `r001`-`r004`                   |
|                            | 300 `r005`                          |
|                            | 100 `r006-r010`                     |
|                            | 1 on ch0. `r11`                          |


## Remarks and comments

|          |                 |                         |             |
| :------- | :-------------- | :---------------------- | :---------- |
| **runs** | **# waveforms** | **pulser voltage (pp)** | **comment** |
| `r001`   | 5,000           | `300 mV`                |             |
| `r002`   | 5,000           | `400 mV`                |             |
| `r003`   | 5,000           | `500 mV`                |             |
| `r004`   | 5,000           | `100 mV`                |             |
| `r005`   | 5,000           | `50 mV`                 |             |
| `r006`   | 5,000           | `25 mV`                 |             |
| `r007`   | 5,000           | `150 mV`                |             |
| `r008`   | 5,000           | `200 mV`                |             |
| `r009`   | 5,000           | `250 mV`                |             |
| `r010`   | 5,000           | `350 mV`                |             |
| `r011`   | 50,000          | not connected to ASIC   | noise run   |
|          |                 |                         |             |







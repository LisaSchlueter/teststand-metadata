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
|                                  |                                                              |
| :------------------------------- | :----------------------------------------------------------- |
| Setup name                       | `ppc01`                                                      |
| period                           | 1                                                            |
| Location                         | LBNL, building 70,  room 70-141                              |
| Date of measurement (yyyy-mm-dd) | 2025-03-17 (`r001 - r011`),     2025-03-18   (`r012 - r022`), 2025-03-20 (`r023 - r032`), 2025-03-25 (`r33`) |
| Operators                        | Lisa Schlueter, Marcos Turqueti, Ryutaro Matsumoto     |
| Goal of measurement              | Benchtest ASIC: Linearity and noise performance              |
|                                  |                                                              |

## Experimental setup description
- ASIC in vacuum chamber, but kept at atmospheric pressure (no vacuum). In this setup, the chamber is used for em-shielding. 
- Germanium detector is not connected to ASIC. 
- Pulser is direclty connected to the CSA. 
- For room termperature measurements, the chamber is in a "warm" dewar (not cooled).
- For `90 K` measurements, the chamber is cooled via cold finger in liquid nitrogen dewar.

## Electronics
LBNL ASIC `l1k65n` + buffer. Board `A`. We use a board with charged capacitors + LDO for the ASIC power supply. 

|         | **runs** | **Description**                 |
| :------ | :------- | :------------------------------ |
| CSA     | all      | `l1k65n`                        |
| Buffer  | all      | yes, but use only single output |
| `V_ref` | all      | `+ 2.6 V` (super cap board)     |

## Pulser
- capacitance `C = 500 fF` (outside of chamber. shielded with copper foil)
- pulse generator: TELEDYNE `T3AFG500`
  - frequency = `20 Hz` 
  - pulse width = `30 ms`
  - fall edge = `20 ms`
  - rise edge = `25 ns`
  - amplitude (peak-to-peak): varied `25 mV` - `500 mV`

## DAQ
Skutek Digitizer "FemtoDAQ Vireo". 
Used one of the optimal configuration of parameters.
|                            |                                            |
| :------------------------- | :----------------------------------------- |
|                            |                                            |
| Sample rate                | `100 MHz`                                  |
| Number of samples          | `4096`                                     |
| Waveform length            | `40.96 µs`                                 |
| Resolution                 | `14` bit                                   |
| Coupling mode              | `DC coupled`                               |
| channel 0                  | CSA output positive                        |
| channel 1                  | pulser                                     |
| Analog Offsets (ch0, ch1)  | `-100`, `0`                                |
| Digital Offsets (ch0, ch1) | `0`, `0`                                   |
| Termination                | `1 kΩ`                                     |
| Trigger on                 | pulser  (Rise)                             |
| Trigger Averaging Window   | `0.32` µs                                  |
| Trigger position approx.   | `8 µs`, exception: `noise runs -> 40.9 µs` |
| Trigger threshold          | 500 `r001`-`r004`                          |
|                            | 300 `r005`                                 |
|                            | 100 `r006-r010` ,  `r023-r032`             |
|                            | 1 on ch0. `r11`, `r012`, `r33`             |
|                            |                                            |


## Run overview:

|          |                 |                                    |                                                             |
| :------- | :-------------- | :--------------------------------- | :---------------------------------------------------------- |
| **runs** | **# waveforms** | **pulser voltage (pp)**            | **comment**                                                 |
| `r001`   | 5,000           | `300 mV`                           | room temperature, not-used CSA output not terminated.       |
| `r002`   | 5,000           | `400 mV`                           | "                                                           |
| `r003`   | 5,000           | `500 mV`                           | "                                                           |
| `r004`   | 5,000           | `100 mV`                           | "                                                           |
| `r005`   | 5,000           | `50 mV`                            | "                                                           |
| `r006`   | 5,000           | `25 mV`                            | "                                                           |
| `r007`   | 5,000           | `150 mV`                           | "                                                           |
| `r008`   | 5,000           | `200 mV`                           | "                                                           |
| `r009`   | 5,000           | `250 mV`                           | "                                                           |
| `r010`   | 5,000           | `350 mV`                           | "                                                           |
| `r011`   | 100,000         | not connected to ASIC              | ", noise run                                                |
|          |                 |                                    |                                                             |
| `r012`   | 100,000         | not connected to ASIC              | noise run. **89.9 K**, not-used CSA output terminated       |
| `r013`   | 5,000           | `25 mV`                            | **89.9 K**, not-used CSA output terminated                  |
| `r014`   | 5,000           | `50 mV`                            | "                                                           |
| `r015`   | 5,000           | `100 mV`                           | "                                                           |
| `r016`   | 5,000           | `150 mV`                           | "                                                           |
| `r017`   | 5,000           | `200 mV`                           | "                                                           |
| `r018`   | 5,000           | `250 mV`                           | "                                                           |
| `r019`   | 5,000           | `300 mV`                           | "                                                           |
| `r020`   | 5,000           | `350 mV`                           | "                                                           |
| `r021`   | 5,000           | `400 mV`                           | "                                                           |
| `r022`   | 5,000           | `500 mV`                           | "                                                           |
| `r023`   | 5,000           | `25 mV`                            | "                                                           |
| `r024`   | 5,000           | `50 mV`                            | "                                                           |
| `r025`   | 5,000           | `100 mV`                           | "                                                           |
| `r026`   | 5,000           | `150 mV`                           | "                                                           |
| `r027`   | 5,000           | `200 mV`                           | "                                                           |
| `r028`   | 5,000           | `250 mV`                           | "                                                           |
| `r029`   | 5,000           | `300 mV`                           | "                                                           |
| `r030`   | 5,000           | `350 mV`                           | "                                                           |
| `r031`   | 5,000           | `400 mV`                           | "                                                           |
| `r032`   | 5,000           | `500 mV`                           | "                                                           |
| `r33`    | 100,000         | not connected to ASIC + terminated | noise run `90.3K`, both CSA outputs recorded with DAQ       |
| `r33`    | 100,000         | not connected to ASIC + terminated | noise run `90.3K`, both CSA outputs recorded with DAQ       |
| `r34`    | 10,000          | not connected to ASIC + terminated | "" + improved shielding                                     |
| `r35`    | 10,000          | not connected to ASIC + terminated | "" + improved shielding                                     |
| `r36`    | 5,000           | not connected to ASIC + terminated | noise run `90.0K`, use additional amplitfier with gain 11.9 |
|          |                 |                                    |                                                             |


## Remarks and comments
We see a "wiggle" in the waveform (CSA output), which likely comes from reflections in the cables. For `r012` - `r022`, we added a termination on the CSA output channel that is *not* used. The resistance has tuned so that the wiggle became minimal. For `r023` - `r032`, new termination introduced to reduce relerection.





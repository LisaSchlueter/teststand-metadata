# teststand-metadata
Collection of metadata for different hpge teststands. 

# PPC01
This set of metadata belongs to the LBNL testand (lab 70-141). This testatand consists of a single Germanium detector called `LBNL_PPC01`.  

The detector is operated in a vacuum cryostat, which is cooled via a cold finger in a liquid Nitrogen dewar to `~ 90K`. This teststand is mainly used for electronics testing (status February 2025). 

## docs
Documentation. 

-  `/docs/bch/` benchtest measurements
- `/docs/cal/` calibration measurements

These folder contain a collected of markdown files containing information on the benchtest `bch` and calibration `cal` measurements. Both folders contain an overview file for all period/runs within the respective category:
-  `readme_bch_overview.md` 
- `readme_cal_overview.md` 

Moreover, the folder contains file with detailed information on individual runs within a period.  These files are named according to the category, period and run:  `"readme_{category}_{period}_{run}.md"`

## hardware
Metadata for the germanium detector and the electronics
- `/detectors/germanium/` metadata, such as geometry, of germanium detectors
- `/asic/` metadata of the asic, such as feedback capacitance or injectection capacitance of pulser (if present)

## jldataprod
### **`.json`** files
This folder contains configuration files in `.json` format for different steps of the data processing. 
- `dsp`: digital signal processing
- `energy`: energy calibration
- `qc`: quality cuts
### **`validity.jsonl`** files
Each folder contains a `validity.jsonl` file, which defines the configuration mapping for specific filekeys.

Each entry in validity.jsonl associates a filekey with a configuration .json file. The configuration assigned to a filekey remains valid starting from that filekey up until (but not including) the next filekey that specifies a different configuration.

This allows for time-based configuration management, where each config remains in effect until explicitly overridden by a newer entry.
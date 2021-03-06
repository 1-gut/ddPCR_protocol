# ddPCR Protocol using Stilla Sapphire (GAPDH/ND2 Duplex)

## Overview

There are a few stages and mixes to be created before running the dPCR chip:

1. DNA sample with EcoRI mix and digest
2. Primer and probe mix
3. Main mix

## Step-by-step

### Before starting this protocol

Defrost the following:

- Samples
- EcoRI and EcoRI buffer
- Stilla MasterMix 5X and Buffer B
- ND2/GAPDH primers and probes

You will need approximately 50 collection tubes for 24 samples.

### Phase 1 - Digest step

| Reagent (per sample) | Volume |
| -------------------- | ------ |
| Nuclease free water  | 3ul    |
| 10X buffer           | 1ul    |
| EcoRI                | 1ul    |
| DNA Sample           | 5ul    |

1. Add 3ul of nuclease free water to each sample tube
2. Add 1ul of 10X EcoRI buffer
3. Add 1ul of EcoRI
4. Add 5ul of DNA sample
5. Incubate at 37&deg;C for 30 mins
6. While incubating, proceed make phase 2 and 3 mixes.

### Phase 2 - Prepare primers and probes

7. Make primer-probe mixes according to table below:

#### Sapphire primer and probe

| Reagents | COX3/ND2 Duplex for 24 samples (Deprecated) | **GAPDH/ND2 Duplex for 24 samples** | GAPDH Mono for 12 samples (For reference only) |
|---|---|---|---|
| GAPDH Ready mixed primers and probe |  | 12.5ul | 6.25ul |
| ND2 Forward Primer | 5ul | 5ul |  |
| ND2 Reverse Primer | 5ul | 5ul |  |
| ND2 Probe | 2.5ul | 2.5ul |  |
| COX3 Forward Primer | 5ul | - |  |
| COX3 Reverse Primer | 5ul | - |  |
| COX3 Probe | 2.5ul | - |  |
| Nuclease free water | 15ul | 15ul | 13.75ul |
| **Total Volume** | 40ul | 40ul | 20ul |

### Phase 3 - Prepare the mastermixes

The reference table below shows the composition required for a single sample and the calculations for running multiple samples with an appropriate volume buffer.

#### Sapphire mastermix

|                                             | Final Conc. | Volume (ul) | Volume (ul)      | Volume (ul)       | Volume (ul)       |
|---------------------------------------------|-------------|-------------|------------------|-------------------|-------------------|
| Desired Number of Samples                   |             |             | 8 actual samples | 12 actual samples | 24 actual samples |
| Sample multiplier to include reserve buffer |             | 1X          | 10X              | 15X               | 30X               |
| H2O                                         |             | 16          | 160              | 240               | 480               |
| Naica Multiplex PCR MasterMix 5X            | 1X          | 5           | 50               | 75                | 150               |
| Buffer B                                    | 4%          | 1           | 10               | 15                | 30                |
| Probe and Primer Mix 25X                    | 1X          | 1           | 10               | 15                | 30                |
| Subtotal Volume                             |             | 23          | 230              | 345               | 690               |
| DNA Sample                                  |             | 2           |                  |                   |                   |
| Final Volume                                |             | 25          |                  |                   |                   |

8. For 24 samples prepare mix as indicated in table (we use 30X calculation to provide sufficient buffer).
9. Add 23ul of above mastermix into individual tubes **Top tip:** Use p20 and pipette 2x 11.5ul for better accuracy.
10. Add 2ul of DNA sample from phase 1 into individual tubes (For Opal add 1ul of DNA sample)
11. **Top tip:** Spin these samples in a tabletop centrifuge for a few seconds to mix evenly and reduce risk of air bubble formation.
12. Prepare sapphire chip - take white port off.
13. Load Sapphire chip with 25ul of above by dropping liquid onto top of oil and cover with white adapter

### Phase 4 - Run ddPCR

13. Turn on pump and ensure pressure between 1.2-1.3 bar.
14. Turn on main ddPCR machine and set program as follows:
    - Partition at 40&deg;C with Sapphire chip
    - Temperature 95&deg;C, 3 minutes wait
    - Cycle 47x
    - 95&deg;C with 15 seconds wait
    - 52&deg;C with 20 seconds wait
    - Close cycle
15. Wipe bottom of chip with antistatic wipe then load chip into ddPCR machine and start

### Phase 5 - ddPCR Chip Reading

16. Open Stilla CrystalReader
    - Scanning Parameters for COX3/ND2:
        - Blue 65ms - COX3
        - Green 100ms - ND2
        - Red 40ms (no target but must be set for reading to happen.)
    - Scanning parameters for GAPDH/ND2;
        - Blue 100ms - GAPDH
        - Green 100ms - ND2
        - Red 40ms - blank
17. Enter corresponding sample ID on screen to chip location
18. Scan chip ID on main screen
19. Open tray, load chip and scan
20. Once scanning is finished open in crystal miner

## Important Notes

### COX3

- MT-COX3 Forward 5' - CGA GTC TCC CTT CAC CAT TTC - 3'
- MT-COX3 Reverse 5' - TTG GCG GAT GAA GCA GAT AG - 3'
- Probe MT-COX3 FAM

### ND2

- MT-ND2 Forward 5' - ACC TGA GTA GGC CTA GAA ATA ACC - 3'
- MT-ND2 Reverse 5' - GTT GCT TGC GTG AGG AAA TAC - 3'
- Probe MT-ND2 HEX

### 16S

- 16S Forward 5' - CGA AAG CGT GGG GAG CAA A - 3'
- 16S Reverse 5' - GTT CGT ACT CCC CAG GCG G - 3'
- Probe 16S FAM

### GAPDH

- GAPDH copy number assay from ThermoFisher (Cat no. 4400291) [Link here](https://www.thermofisher.com/order/catalog/product/4400291)

## Protocol Updates

### 17 Jun 2022

- Moving forwards, decision confirmed to run ND2/GAPDH duplex to obtain both genomic and mitochondrial readouts

### 6 Jun 2022

- Further attempt with GAPDH
- GAPDH primer and probes confirmed to be working on mono assay
- GAPDH/ND2 duplex confirmed to be working
- Results of ND2 is in line with previous COX3/ND2 assay
- Results of GAPDH is in line between mono and duplex assays
- GAPDH/ND2 reinstated for future work (COX3 and ND2 confirmed to be almost perfectly correlated, R=0.997)

### 22 Apr 2022

- Opal chips added for scalability
- **Final decision:** Continue using Sapphire for now, Opal is technically finicky with the loading of samples and it has reduced margins of error as only 8ul is loaded vs 25ul

### 24 Jan 2022

- Protocol cleaned up with key steps clarified for running 24 samples as default (6 chips - current maximum in a single session).
- MasterMix volume adjusted to provide more reserve.

### 10 Sep 2021

- GAPDH gene did not amplify well. (6 June 2022 update - likely because sample did not have much genomic cfDNA in first place, retested on new array of samples and primer-probe confirmed to be working)
- GAPDH amplification is now deprecated. (6 June 2022 update - because COX3 and ND2 are correlated at 0.997, plan to transition to GAPDH/ND2 duplex)

## Deprecated Opal Tables

### Opal primer and probe mix

| Reagents | Mitochondrial DNA primers (COX3/ND2 Duplex) |  |  |
|---|---|---|---|
|  | 16 samples | 32 samples | 48 samples |
| ND2 Forward Primer | 2.5ul | 5ul | 5ul |
| ND2 Reverse Primer | 2.5ul | 5ul | 5ul |
| ND2 Probe | 1.25ul | 2.5ul | 2.5ul |
| COX3 Forward Primer | 2.5ul | 5ul | 5ul |
| COX3 Reverse Primer | 2.5ul | 5ul | 5ul |
| COX3 Probe | 1.25ul | 2.5ul | 2.5ul |
| Nuclease free water | 7.5ul | 15ul | 15ul |
| Total Volume | 20ul | 40ul | 40ul |

### Opal Mastermix

| Reagents | Mitochondrial DNA primers (COX3/ND2 Duplex) |  |  |  |  |
|---|---|---|---|---|---|
| Final Conc. | Volume (ul) | Volume (ul) | Volume (ul) | Volume (ul) |  |
| Desired Number of Samples |  |  | 16 actual samples | 32 actual samples | 48 actual samples |
| Sample multiplier to include reserve buffer |  | 1X | 20X | 40X | 60X |
| H2O |  | 4.44 | 88.8 | 177.6 | 266.4 |
| Naica Multiplex PCR MasterMix 5X | 1X | 1.6 | 32 | 64 | 96 |
| Buffer B | 4% | 0.32 | 6.4 | 12.8 | 19.2 |
| Probe and Primer Mix 25X | 1X | 0.64 | 12.8 | 25.6 | 38.4 |
| Subtotal Volume |  | 7 | 140 | 280 | 420 |
| DNA Sample |  | 1 |  |  |  |
| Final Volume |  | 25 |  |  |  |

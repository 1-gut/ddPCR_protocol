# ddPCR Protocol using Stilla Sapphire

## Overview

There are a few stages and mixes to be created before running the dPCR chip:

1. DNA sample with EcoRI mix and digest
2. Primer and probe mix
3. Main mix

## Step-by-step:

### Before starting this protocol

Defrost the following:
- Samples
- EcoRI and EcoRI buffer
- Stilla MasterMix 5X and Buffer B
- COX3/ND2 primers and probes

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

7. Make 20ul of primer-probe mix according to table below:

| Reagents                            | Mitochondrial DNA primers (COX3/ND2 Duplex) for 24 samples | Genomic DNA primers (GAPDH) (Deprecated) for 12 samples |
|-------------------------------------|------------------------------------------------------------|---------------------------------------------------------|
| GAPDH Ready mixed primers and probe |                                                            | 6.25ul                                                  |
| ND2 Forward Primer                  | 5ul                                                        |                                                         |
| ND2 Reverse Primer                  | 5ul                                                        |                                                         |
| ND2 Probe                           | 2.5ul                                                      |                                                         |
| COX3 Forward Primer                 | 5ul                                                        |                                                         |
| COX3 Reverse Primer                 | 5ul                                                        |                                                         |
| COX3 Probe                          | 2.5ul                                                      |                                                         |
| Nuclease free water                 | 15ul                                                       | 13.75ul                                                 |
| **Total Volume**                    | 40ul                                                       | 20ul                                                    |


### Phase 3 - Prepare the two mastermixes A and B

The reference table below shows the composition required for a single sample and the calculations for running multiple samples with an appropriate volume buffer.

_Reference table for calculation (use 9 for 8 samples/2 chips and 13 for 12 samples/3 chips - 1 sample buffer volume)_
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

8. For 24 samples prepare mix as indicated in table (we use 30 to provide sufficient buffer).
9. Add 23ul of above mastermix into individual tubes
10. Add 2ul of DNA sample from phase 1 into individual tubes
11. Prepare sapphire chip - take white port off.
12. Load Sapphire chip with 25ul of above by dropping liquid onto top of oil and cover with white adapter

### Phase 4 - Run ddPCR

13. Turn on pump and ensure pressure between 1.2-1.3 bar.
14. Turn on main ddPCR machine and set program as follows:
    - Partition at 40&deg;C with Sapphire chip
    - Temperature 95&deg;C, 3 minutes wait
    - Cycle 47x
    - 95&deg;C with 15 seconds wait
    - 52&deg;C with 20 seconds wait
    - Close cycle
15. Wipe bottom of Sapphire chip with antistatic wipe then load chip into ddPCR machine and start

### Phase 5 - ddPCR Chip Reading

16. Open Stilla CrystalReader
    - Scanning Parameters:
      - Blue 65ms - COX3
      - Green 200ms - ND2
      - Red 40ms (no target but must be set for reading to happen.)
17. Enter corresponding sample ID on screen to chip location
18. Scan chip ID on main screen
19. Open tray, load chip and scan
20. Once scanning is finished open in crystal miner

## Important Notes:

### COX3:

- MT-COX3 Forward 5' - CGA GTC TCC CTT CAC CAT TTC - 3'
- MT-COX3 Reverse 5' - TTG GCG GAT GAA GCA GAT AG - 3'
- Probe MT-COX3 FAM

### ND2:

- MT-ND2 Forward 5' - ACC TGA GTA GGC CTA GAA ATA ACC - 3'
- MT-ND2 Reverse 5' - GTT GCT TGC GTG AGG AAA TAC - 3'
- Probe MT-ND2 HEX

### 16S:
- 16S Forward 5' - CGA AAG CGT GGG GAG CAA A - 3'
- 16S Reverse 5' - GTT CGT ACT CCC CAG GCG G - 3'
- Probe 16S FAM

## Protocol Updates

### 24 Jan 2022
- Protocol cleaned up with key steps clarified for running 24 samples as default (6 chips - current maximum in a single session).
- MasterMix volume adjusted to provide more reserve.
### 10 Sep 2021

- GAPDH gene did not amplify well.
- GAPDH amplification is now deprecated.

# ddPCR Protocol using Stilla Sapphire

## Overview

There are a few mixes to be made before running the chip:

- DNA sample with EcoRI mix and digest
- Primer and probe mix
- Main mix

## Step-by-step:

### Phase 1 - Digest step

| Reagent             | Volume |
| ------------------- | ------ |
| Nuclease free water | 3ul    |
| 10X buffer          | 1ul    |
| EcoRI               | 1ul    |
| DNA Sample          | 5ul    |

1. Add 3ul of nuclease free water to each sample tube
2. Add 1ul of 10X EcoRI buffer
3. Add 1ul of EcoRI
4. Add 5ul of DNA sample
5. Incubate at 37&deg;C for 30 mins

### Phase 2 - Prepare primers and probes

6. Make 20ul of primer-probe mix according to table below:

| Reagents                                       | Genomic DNA primers (GAPDH) A | Mitochondrial DNA primers (COX3/ND2 Duplex) B |
| ---------------------------------------------- | ----------------------------- | --------------------------------------------- |
| GAPDH Ready mixed primers and probe            | 6.25ul                        |                                               |
| ND2 Primers (Mix 3ul forward and 3ul reverse)  |                               | 5ul                                           |
| ND2 Probe                                      |                               | 1.25ul                                        |
| COX3 Primers (Mix 3ul forward and 3ul reverse) |                               | 5ul                                           |
| COX3 Probe                                     |                               | 1.25ul                                        |
| Nuclease free water                            | 13.75ul                       | 7.5ul                                         |
| **Total Volume**                               | 20ul                          | 20ul                                          |

7. Mix 3ul of COX3 forward and 3ul of COX3 reverse primers
8. Mix 3ul of ND2 forward and 3ul of ND2 reverse Primers
9. Add the regaents above to make primer-probe mix A (genomic) and primer-probe mix B (mitochondrial)

### Phase 3 - Prepare the two mastermixes A and B

_Reference table for calculation (use 9 for 8 samples/2 chips and 13 for 12 samples/3 chips - 1 sample buffer volume)_
| | Final Conc. | Volume (ul) | Volume (ul) | Volume (ul) |
|----------------------------------|-------------|-------------|-------------|-------------|
| Number of Samples | | 1 | 9 | 13 |
| H2O | | 16 | 144 | 208 |
| Naica Multiplex PCR MasterMix 5X | 1X | 5 | 45 | 65 |
| Buffer B | 4% | 1 | 9 | 13 |
| Probe and Primer Mix 25X | 1X | 1 | 9 | 13 |
| DNA Mix | | 2 | | |
| Final Volume | | 25 | | |

10. For 12 samples prepare 208ul of water, 65ul of PCR MasterMix 5X, 13ul of Buffer B, 13ul of primer-probe mix from phase 2.
11. Add 23ul of above mastermix into individual tubes
12. Add 2ul of DNA sample from phase 1 into individual tubes
13. Prepare sapphire chip - take white port off.
14. Load Sapphire chip with 25ul of above by dropping liquid onto top of oil and cover with white adapter

### Phase 4 - Run ddPCR

15. Turn on pump and ensure pressure between 1.2-1.3 bar.
16. Turn on main ddPCR machine and set program as follows:
    - Partition at 40&deg;C with Sapphire chip
    - Temperature 95&deg;C, 3 minutes wait
    - Cycle 47x
    - 95&deg;C with 15 seconds wait
    - 52&deg;C with 20 seconds wait
    - Close cycle
17. Wipe bottom of Sapphire chip with antistatic wipe then load chip into ddPCR machine and start

### Phase 5 - ddPCR Chip Reading

18. Open Stilla CrystalReader
    - Load image analysis configuration: `C:/Program Files/Stilla/CrystalReader/config/AnalysisConfigurationFile_Prism3_SapphireChip_naica_multiplex-PCR-MIX_Taqman_v1.0.yaml`
    - Note image analysis config can be left blank actually
    - Scanning Parameters:
      - Blue 65ms
      - Green 200ms
      - Red 40ms
19. Enter corresponding sample ID on screen to chip location
20. Scan chip ID on main screen
21. Open tray, load chip and scan
22. Once scanning is finished open in crystal miner

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

### Experimental Results 10 Sep 2021

GAPDH gene did not amplify well.

# ddPCR Protocol using Stilla Sapphire

## Overview

There are a few mixes to be made before running the chip:

- DNA sample with EcoRI mix and digest
- Primer and probe mix
- Main mix

### EcoRI Digest Step

Initial sample mix:

- 3ul nuclease free water
- 1ul 10x buffer
- 1ul EcoRI
- 5ul DNA sample

## Step-by-step:

Phase one (Digest step)

1. Add 3ul of nuclease free water to each sample tube
2. Add 1ul of 10X EcoRI buffer
3. Add 1ul of EcoRI
4. Add 5ul of DNA sample
5. Incubate at 37&deg;C for 30 mins

Phase two (Prepare primers and probes)

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

Phase 3 - Prepare the two mastermixes A and B

10. For 12 samples prepare 208ul of water, 65ul of PCR MasterMix 5X, 13ul of Buffer B, 13ul of primer-probe mix from phase 2.
11. Add 23ul of above mastermix into individual tubes
12. Add 2ul of DNA sample from phase 1 into individual tubes
13. Prepare sapphire chip - take white port off.
14. Load Sapphire chip with 25ul of above by dropping liquid onto top of oil and cover with white adapter

Phase 4 - Run ddPCR

15. Turn on pump and ensure pressure between 1.2-1.3 bar.
16. Turn on main ddPCR machine and set program as follows:
    - Partition at 40&deg;C with Sapphire chip
    - Temperature 95&deg;C, 3 minutes wait
    - Cycle 47x
    - 95&deg;C with 15 seconds wait
    - 52&deg;C with 20 seconds wait
    - Close cycle
17. Wipe bottom of Sapphire chip with antistatic wipe then load chip into ddPCR machine and start

Phase 5 - Reading chip

### Important Notes:

-

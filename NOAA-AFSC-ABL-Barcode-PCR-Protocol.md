---
# MIOP terms
methodology_category: Omics Analysis
project: NOAA AFSC ABL Environmental DNA Lab Protocols
purpose: PCR [OBI:0000415]
analyses: PCR [OBI:0000415]
broad_scale_environmental_context: marine biome [ENVO:00000447], freshwater biome [ENVO:00000873]
local_environmental_context: marine biome [ENVO:00000447], freshwater biome [ENVO:00000873]
environmental_medium: sea water [ENVO:00002149], fresh water [ENVO:00002011]
target: 12S mitochondrial ribosomal RNA  [NCIT:C128263], MT-RNR1 Gene [NCIT:C128260]
creator: Kimberly Ledger, Diana Baetscher
skills_required: sterile technique, pipetting skills, standard molecular technique
time_required: 80 minutes
personnel_required: 1
language: en
issued: 2025-06-04
audience: scientists
publisher: NOAA Alaska Fisheries Science Center Auke Bay Laboratories Genetics Program
hasVersion: 1
license: CC0 1.0 Universal
maturity level: mature

# FAIRe terms
pcr_0_1: 1
pcr2_thermocycler: Applied Biosystems GeneAmp PCR System 9700
pcr2_amplificationReactionVolume: 10
pcr2_commercial_mm: Qiagen Multiplex PCR Plus
pcr2_custom_mm: PCR reactions were run in 10 uL reaction volumes, with 2 µl of diluted (1:5) PCR product per reaction, 5 µl of Qiagen Multiplex PCR Plus, 1 µl of i07 index (1 µM), and 2 µl of i05 index (0.5 µM).
pcr2_dna_vol: 2.0
pcr2_cond: initial denaturation:95_5;denaturation:95_0.167;annealing:65_0.5;elongation:72_0.5;final elongation:72_5;10
pcr2_annealingTemp: 65
pcr2_cycles: 10
pcr2_analysis_software: not applicable
pcr2_method_additional: not applicable

---

# Protocol Template - PCR

## PROTOCOL INFORMATION

### Minimum Information about an Omics Protocol (MIOP)

- MIOP terms are listed in the YAML frontmatter of this page.
- See [MIOP_definition.md](https://github.com/BeBOP-OBON/0_protocol_collection_template/blob/main/MIOP_definition.md) for list and definitions.

### Making eDNA FAIR (FAIRe)

- FAIRe terms are listed in the YAML frontmatter of this page.
- See <https://fair-edna.github.io/download.html> for the FAIRe checklist and more information.
- See <https://fair-edna.github.io/guidelines.html#missing-values> for guidelines on missing values that can be used for missing FAIRe or MIOP terms.

### Authors

| PREPARED BY | AFFILIATION | ORCID | DATE |
| ------------- | ------------- | ------------- | ------------- |
| Kimberly Ledger | Genetics Program, Auke Bay Laboratories, Alaska Fisheries Science Center, NOAA | https://orcid.org/0000-0002-5552-5598 | 2025-06-04 |
| Diana Baetscher | Genetics Program, Auke Bay Laboratories, Alaska Fisheries Science Center, NOAA | Content Cell | 2025-06-04 |

### Related Protocols

| PROTOCOL NAME | LINK         | VERSION      | RELEASE DATE | INTERNAL/EXTERNAL |
| ------------- | ------------ | ------------ | ------------ | ----------------- |
| NOAA-AFSC-ABL-MiFish-mod-U-PCR-Protocol  | TBD | 1.0.0 | 2025-06-04   | Internal  |

### Protocol Revision Record

| VERSION | RELEASE DATE | DESCRIPTION OF REVISIONS |
| ------------- | ------------- | ------------- |
| 1.0.0 | 2025-06-04 | Initial release |

- Version numbers start at 1.0.0 when the protocol is first completed and will increase when changes that impact the outcome of the procedure are made (patches: 1.0.1; minor changes: 1.1.0; major changes: 2.0.0).
- Release date is the date when a given protocol version was finalised.
- Description of revisions includes a brief description of what was changed relative to the previous version.

### Acronyms and Abbreviations

| ACRONYM / ABBREVIATION | DEFINITION |
| ------------- | ------------- |
| AFSC | Alaska Fisheries Science Center  |
| NOAA | National Oceanic and Atmospheric Administration|
| ABL | Auke Bay Laboratories |
| eDNA | environmental DNA  |
| PCR | polymerase chain reaction |
| NTC | no template control | 
| DI water | deionized water | 
| IDT| Integrated DNA Technologies

### Glossary

| SPECIALISED TERM | DEFINITION |
| ------------- | ------------- |
| amplicon PCR | aka PCR 1 or the first PCR of a two-step PCR library preparation | 
| barcode PCR | aka PCR 2 or the second PCR of a two-step PCR library preparation | 

## BACKGROUND

### Summary

This protocol describes the steps to perform the second PCR of a two-step PCR next generation sequencing library preparation using custom indices.

This protocol must follow an amplicon PCR protocol where the locus-specific primers included Illumina sequencing primers (specifically the Illumina small RNA primer with the forward primer (cRead1: 5'-CGACAGGTTCAGAGTTCTACAGTCCGACGATC-3') and the Illumina Multiplexing read 2 primer with the reverse primer (cRead2: 5'-GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT-3')). 

This protocol enables multiplexing many, many plates of samples as the i7 barcodes are unique for each plate and the i5 barcodes are unique for each well. The combination of the i7 and i5 barcodes results in unique library-specific barcodes attaching to each amplicon PCR product.

### Method Description and Rationale

This protocol was chosen because it has been tested and deployed at scale by the NOAA AFSC Genetics Program.

### Spatial Coverage and Environment(s) of Relevance

This protocol can be used to attach unique library-specific barcodes to any amplicon PCR product, given Illumina sequencing primers were included with the locus-specific primers during PCR.

## PERSONNEL REQUIRED

One person with molecular biology experience.

### Safety

This protocol does not involve any hazardous chemicals, although standard precautions including wearing PPE should be taken to avoid skin and eye exposure to chemical reagents.

### Training Requirements

Molecular biology training (including, at a minimum, sterile technique, pipetting small volumes, and programming and running PCR thermocyclers) is required to conduct this protocol.

### Time Needed to Execute the Procedure

** PCR preparation and running the PCR protocol for a single 96-well plate takes approximately 90 minutes, of which 40 mins is the thermocycler run time. Additional plates can be run simultaneously without greatly increasing the time required.

## EQUIPMENT

| DESCRIPTION | PRODUCT NAME AND MODEL | MANUFACTURER | QUANTITY | REMARK |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| **Durable equipment** |
| PCR workstation | Content Cell | Content Cell | Content Cell | Content Cell |
| Pipetter: 1-10 μl|Pipet-Lite LTS Pipette L-10XLS+ |Rainin|1|Can be substituted with any accurate pipettor|
| Pipetter: 20 - 200 μl	|Pipet-Lite LTS Pipette L-200XLS+ |Rainin|	1|Can be substituted with any accurate pipettor|
| Pipetter: 100-1000 μl	|Pipet-Lite LTS Pipette L-1000XLS+ |Rainin|1|Can be substituted with any accurate pipettor|
| 8-channel Pipetter: 1-10 μL| Pipet-Lite Multi Pipette L8-10XLS+ |Rainin| 1|Can be substituted with any accurate pipettor. Not required but reduces protocol time.|
| Vortex | Vortex Genie 2 | Scientific Industries | 1 | Can be substituted with generic|
| Plate centrifuge | Centrifuge 5430 | Eppendorf | 1| Can be substituted with generic|
| Mini-centrifuge | myFuge  | Benchmark | 1 | Can be substituted with generic, but needs to fit 1.5-2.0 mL tubes | 
| 2 mL tube rack | Microcentrifuge tube rack | unknown | 1 | Can be substituted with generic | 
| 96-well PCR plate rack | PCR tube rack for 96-well plates | unknown | 1 | Can be substituted with generic |
| Thermocycler | GeneAmp PCR System 9700 | Applied Biosystems | 1 | Can be substituted with generic |
| E-Gel Device| E-Gel Power Snap Electrophoresis Device | Invitrogen | 1 | Can be substituted with agarose gel electrophoresis system|
| **Consumable equipment** |
| 1000 μL filter pipette tips | Pipette Tips TR LTS 1000uL F | Rainin | 1 | Can be subsituted with generic - must be sterile, filtered, and match pipetter |
| 200 μL filter pipette tips  | Pipette Tips TR LTS 200uL F | Rainin| 10 | Can be subsituted with generic - must be sterile, filtered, and match pipetter|
| 10 μL filter pipette tips  | Pipette Tips TR LTS 20uL F | Rainin | 96x3 | Can be subsituted with generic - must be sterile, filtered, and match pipetter |
| 96-well PCR plate | Template semi-skirted 96-well PCR plate, 0.2 ML | USA Scientific | 1 | Can be substituted with generic |
| 8-well strip tube w/ caps | 0.2 mL 8-tube strips with caps | Bio-Rad | 1 | optional, Can be substituted with generic |
| foil plate seals | VWR Adhesive PCR Foil Seals | VWR | 1 | Can be substituted with generic |
| microcentrifuge tubes | GeneMate 1.7 uL microcentrifuge tube | VWR | 1 | Can be substituted with generic |
| disposable gloves | Comfort Nitril Gloves | Fisherbrand | 2 | Can be substituted with generic |
| E-Gel | E-Gel EX Agarose Gel | Invitrogen | 1 | Can be substituted with agarose gel |
| **Chemicals** |
| 2X PCR Master Mix | Qiagen Multiplex PCR Plus | Qiagen | 624 uL per plate | Store at -20C long-term, or in refrigerator for up to one week. |
| i07 Index Primers | Custom oligos | IDT | 108 uL per plate | Store at -20C long-term, or in refrigerator for up to one week.  |
| i05 Index Primers | Custom oligos | IDT | 2 uL per sample | Store at -20C long-term, or in refrigerator for up to one week. |
| Nuclease-Free Water  | Ultrapure DNase/RNase-free distilled water | ThermoFisher Scientific | 1 mL | Can be substituted with generic |
| 70% EtOH | Molecular grade ethanol| Generic | 40 mL | |
| 10% bleach| Hypochlorite bleach |Clorox| 40 mL | Remake every ~5 days as bleach decomposes quickly at 10% concentration |

## STANDARD OPERATING PROCEDURE

### Protocol

#### Preparation

1. While wearing clean, disposable gloves, sterilize workspaces and durable equipment, including pipettes within the POST-PCR eDNA workstation with 10% bleach. Then wipe down all surfaces and equipment with 70% EtOH.
2. Run the UV light in the POST-PCR eDNA workstation for at least 10 minutes before starting work.
3. Label all PCR plates both on the side of the plate and on the top of the foil (in the plate margins). Recommended labeling scheme includes plate name, i07 primer ID, date of PCR and personnel initials.

#### PCR

**i7 Primer Sequences for Plate Barcoding**
Oligo sequence structure: 5'-**[P7 Capture Sequence]**[6bp i7 Barcode]_[Multiplexing Read2 Primer]_-3'

| i7 Index Name | Barcode_Sequence | Reverse_Complement | Oligo Sequence (5’ -> 3’)|
| ----- | ----- | ----- | ----- |
|GTseq_i7_i01| CGTGAT | ATCACG | **CAAGCAGAAGACGGCATACGAGAT**CGTGAT_GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT_|
|GTseq_i7_i02| ACATCG | CGATGT | **CAAGCAGAAGACGGCATACGAGAT**ACATCG_GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT_|

**i5 Primer Sequences for Well Barcoding**: 
Oligo structure: 5'-**[P5 Capture Sequence]**[6bp i5 Barcode] _[Small RNA Primer]_ -3'

| Well Position| Barcode_Sequence | Reverse_Complement | Sequence (5’ -> 3’)|
| ----- | ----- | ----- | ----- |
|A01 | AAACGG  | CCGTTT | **AATGATACGGCGACCACCGAGATCTACAC**AAACGG_CGACAGGTTCAGAGTTCTACAGTCCGACGATC_ |
|B01 | ACTCTT | AAGAGT | **AATGATACGGCGACCACCGAGATCTACAC**ACTCTT_CGACAGGTTCAGAGTTCTACAGTCCGACGATC_ |

See Google Sheet for entire list of available barcode sequences: https://docs.google.com/spreadsheets/d/1YHxEQUjd1nAA7z5jbdtoXQAFNmeGuaf9/edit?usp=sharing&ouid=102569603400220961523&rtpof=true&sd=true

**Reaction Mixture**: PCR reagents, volumes, initial and final concentrations

| Reagent |Volume (μL) per plate| Volume (μL) per reaction | Intial concentration| Final concentration|
| ----- | ----- | ----- |----- |----- |
| Qiagen Multiplex PCR Plus | 520 | 5.0 |100% |50% |
| i7 Index Primer | 104 | 1 |1 μM |0.1 μM |
| i5 Index Primer | N/A | 2 |0.5 μM | 0.1 μM |
| PCR Product |N/A| 2 | N/A | N/A |
| **Total**|**624**| **10.0** | **N/A** |**N/A**|

This table breaks down the mixture per plate and per reaction. When running full plates (96-wells), each reagent volume was multipled by 104 (96+8 extra sample volumes to account for pipetting error) when preparing the final master mix.

**PCR Cycling Program**: 

| PCR step | Temperature | Duration | Repetition |
| ----- | ----- | ----- | ----- |
|Initial denaturation|	95°C	|5min|	1X
|**Normal Cycling**||||
|Denaturation|	95°C|	10s|	10X|
|Annealing|	65°C|	30s	|10X|
|Extension 	|72°C	|30s	|10X|
|Final extension	|72°C	| 5min	|1X|
|Hold	|4°C	|∞	|1X|

**Step-by-Step Instructions:**

*Note: For eDNA library prep, PCR set-up should be carried out in a dedicated post-PCR eDNA space that is distinct from where non-eDNA post-PCR activities are located. No equipment, consumables, or reagents should be shared between pre- and post-PCR spaces with a unidirectional flow of sample processing. Post-PCR for eDNA samples should be kept separate from non-eDNA samples.*

1. While wearing clean, disposable gloves, set out PCR master mix, index primers, and PCR product to thaw if frozen.
2. Briefly vortex (just a few pulses is sufficient) and spin down thawed PCR master mix, index primers, and PCR product.
3. Dilute PCR product 1:5 by transferring 5uL of PCR product and 20uL of nuclease-free water to a new 96-well plate, or by adding 44 uL of of nuclease-free water directly to the PCR product plate (assuming ~11uL of PCR product is remaining). 
4. Pool reagents to make barcode PCR master mix that includes PCR master mix and i7 index primer (@ 1uM), as denoted in the above reaction mixture table. If primers are not at designated working concentration, make a dilution from the stock concentration first. 
5. Aliquot 6 μL of barcode PCR master mix into each well of the PCR plate. If setting up a full 96-well plate, it is more efficient aliquot 77 μL of barcode PCR master mix per well into a 8-well strip tube. Then use a multichannel pipet to transfer 6 μL of final master mix into 96-well plate.
6. Using a multichannel pipet, add 2 uL of i5 index primer (@ 0.5uM) to each well. 
7. Using a multichannel pipet, add 2 μL of 1:5 diluted PCR product to each well.
8. Seal the PCR plate with foil and double check plate is labeled with plate name, i7 primer ID, date of PCR and personnel initials. 
9. Briefly vortex (just a few pulses is sufficient) and spin down the plate, and then place in thermocycler.
10. Run PCR cycling program.

### Quality Control

1. Plates should be removed from the thermocycler after the run completes and stored at 4°C until run on a gel. Storing the PCR product at -20˚C is ideal for 1-6 month term storage.
2. Run gel visualization using E-Gel System confirm successful PCR and correct target size fragment. Performing the barcode PCR protocol should increase the PCR product size by ~65 bps. 

#### E-Gel Protocol
1. Insert pre-cast agarose gel into E-Gel device. 
2. Load 18 uL of DI water to every well (regardless of whether or not sample or ladder will be added). 
3. Add 2 uL of DNA ladder or PCR product into the wells (total volume per well is 20 uL). Note: You may reuse E-Gels and do not need to load a sample to every well in a single run. 
4. Select appropriate program and run gel for 10 minutes. Visualize using built-in light system. 

## REFERENCES

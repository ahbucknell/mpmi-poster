# Poster walkthrough
## Section 1: Introduction
- Some NLRs exist in sensor-helper pairs, such as the rice Pik pair.
- Pik1 contains an integrated domain (ID) that recognises the AVR-Pik effector.
- Pik2 acts as the helper NLR, and activates the downstream effector-triggered immune response.
- Previous research shows that IDs are modular, and can be engineered to alter the NLR's ability to recognise effectors.

- RFdiffusion can generate new-to-nature proteins, including proteins that bind to a given target protein.
- Over a set number of steps, RFdiffusion will generate a protein backbone using a pre-trained algorithm.
- The output from RFdiffusion is a PDB file containing the structure of the generated protein, but with no  corresponding amino acid sequence.
- Inverse protein folding tools such as ProteinMPNN are used to generate sequences that fold to the designed structures. We generated 8 sequences for each backbone generated.
- Structural predictions of the sequences are done via AlphaFold2 to ensure they match the generated backbones.
- ColabDesign makes this pipeline very user-friendly, and was used to generated the binders against AVR-Pii.

## Section 2: AVR-Pii
- Previous NLR engineering attempts have focused on expanding the recognition of MAX effectors.
- We wanted to demonstrate novel recognition of a non-MAX effector, such as AVR-Pii which is a Zinc-finger fold effector.
- Furthermore, the AVR-Pii crystal structure has been resolved (PDB: 7PP2), making it a good target effector to design against.

## Section 3: _In silico_ filtering
- In total we generated 256 different candidate binders against AVR-Pii.
- As recommended by Bennett _et al._ (2023), binders were filtered by having a interface predicted alignment error (iPAE) value of less than 10.
- Only 6 binders passed this filter, all of which were taken forward for testing *in planta*

## Section 4: Cell death assays
- The 6 binders were separately integrated into the Pikm1 chasis.
- Each binder-integrated Pikm1 NLR was transiently expressed within *Nicotiana benthamiana*, these are referred to only by their binder name (e.g. Pii1004)
- Each Pikm1 was co-infiltrated with Pikm2, P19 (for better expression), and either AVR-Pii or an empty vector (EV) control. Only elements which change per infiltration are shown (Pikm1 + effector/EV).
- Pikm1<sup>WT</sup> was infiltrated with AVR-PikD to act as a positive control. Pikm1<sup>WT</sup> + AVR-Pii served as the negative control. Both of these combinations were infiltrated with Pikm2 + P19.
- All binders were challenged with AVR-Pii to test for recognition, and also against the EV control to test for auto-activity.
- Pii0003- and Pii1004-integrated Pikm1s showed recognition of AVR-Pii without auto-activity.

## Section 5: Future work
- Via X-ray diffraction we hope to resolve the structure of Pii1004 to verify it matches the RFdiffusion-generated backbone.
- We aim to characterise the binding affinity of the Pii1004 binder to AVR-Pii by isothermal titration calorimetry.
- We hope to demonstrate that the recognition of AVR-Pii by the Pii0003 and Pii1004 binders are translatable to economically-significant crop species.

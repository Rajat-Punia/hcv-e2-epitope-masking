# Structure-guided epitope masking of Hepatitis C glycoprotein E2

Code and input data for the design of glycan- and PEG-masked HCV E2 immunogens: choosing which
residues of the immunodominant βSW antigenic region to occlude, and prioritizing where to make the
necessary amino-acid substitutions.

Both analyses are in one notebook, [`epitope_masking_design.ipynb`](epitope_masking_design.ipynb).

**Consensus epitope.** Four E2–antibody complexes are analyzed to identify the E2 residues contacted
by every antibody, the common primary epitope residues (CPER), and those close to every antibody but
contacted by none, the common secondary epitope residues (CSER).

**Site selection.** For every position, the frequency across circulating genotype 1 E1E2 sequences of
the feature each masking chemistry requires: an N-linked sequon (N-X-S/T, X ≠ P) for glycan masking,
or a lysine for amine-directed conjugation. Candidate sites are the CPER and CSER positions at which
the feature is already carried by at least one circulating strain, on the reasoning that such a
variant is compatible with E2 folding and secretion.

```
epitope_masking_design.ipynb
data/
  E1E2_genotype1_alignment.fasta  curated HCV genotype 1 E1E2 alignment (HCV-GLUE)
  structures/
    E2_E1.pdb                     E2 with antibody E1      (PDB 6UYG)
    E2_hcab17.pdb                 E2 with antibody hcab17  (PDB 8W0Y)
    E2_HEPC46.pdb                 E2 with antibody HEPC46  (PDB 6MEJ)
    E2_hcab44.pdb                 E2 with antibody hcab44  [PDB accession]
requirements.txt
```


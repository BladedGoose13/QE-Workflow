# Electronic Structure of Silicon-Doped Graphene - DFT with Quantum ESPRESSO

This repository documents my undergraduate research training in computational materials science at Instituto Tecnológico y de Estudios Superiores de Monterrey, under the supervision of Dr. José Ángel Reyes Retana.

The work progressed in two stages: first replicating known graphene band structure results to validate the computational setup, then extending to an original study of silicon doping effects via the Virtual Crystal Approximation (VCA). Results were presented as a poster at the Tec Science Summit 2026 (NextGen Scientists Program).

---

## Project Summary

Density Functional Theory calculations were used to analyze how silicon doping modifies the electronic structure of graphene at varying concentrations (0%, 10%, 20% Si). The key finding is a progressive distortion of the Dirac cone and the emergence of a bandgap with increasing silicon content, suggesting a transition toward semiconducting behavior tunable by doping concentration.

---
## Scientific Poster
[PDF](Silicon_Doped_Graphene.pdf)
---

## Workflow

```
1. Structural relaxation     →   vc-relax
2. SCF calculation           →   pw.x
3. NSCF for band structure   →   pw.x (nscf)
4. Band structure            →   bands.x
5. Density of States (DOS)   →   dos.x
6. Projected DOS (PDOS)      →   projwfc.x
7. Post-processing & plots   →   Python
```

---

## Computational Parameters

| Parameter | Value |
|---|---|
| Code | Quantum ESPRESSO |
| Exchange-correlation | PBE (GGA) |
| Pseudopotentials | Ultrasoft |
| Kinetic energy cutoff | 40 Ry |
| k-point grid | 60 × 60 × 1 |
| Smearing method | Tetrahedron |
| Silicon doping model | VCA via `virtual_v2.x` |

---

## Systems Studied

| System | Si concentration |
|---|---|
| Graphene | 0% Si (reference) |
| C₁₉Si₀₁ | 5% Si |
| C₁₈Si₀₂ | 10% Si |
| C₁₇Si₀₃ | 15% Si |
| C₁₆Si₀₄ | 20% Si |
| C₁₅Si₀₅ | 25% Si |
| C₁₄Si₀₆ | 30% Si |
| C₁₃Si₀₇ | 35% Si |
| C₁₂Si₀₈ | 40% Si |
| C₁₁Si₀₉ | 45% Si |
| C₁₀Si₁₀ | 50% Si |
---

## Software & Environment

- **Quantum ESPRESSO** — DFT engine
- **Linux** (VirtualBox) — simulation environment
- **Python** — data analysis and visualization (NumPy, Matplotlib)

---

## References

- P. Giannozzi et al., *J. Phys.: Condens. Matter* **21**, 395502 (2009)
- P. Giannozzi et al., *J. Phys.: Condens. Matter* **29**, 465901 (2017)
- Nguyen T. Hung, Ahmad R. T. Nugraha, Ritsuko Saito, *Quantum ESPRESSO Course for Solid-State Physics*

---

## Acknowledgments

Developed under the supervision of Dr. José Ángel Reyes Retana (Tecnológico de Monterrey, Campus Monterrey). AI tools were used to assist in formatting, text polishing, and scientific vocabulary. All content was manually reviewed, edited, and verified by the author to ensure accuracy and originality.

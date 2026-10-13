[README (3).md](https://github.com/user-attachments/files/33379985/README.3.md)
# Protein Explorer

**[Open the live site →](https://juvasshini.github.io/protein-explorer/)**

Load any structure from the Protein Data Bank or AlphaFold Database and explore its 3D shape, backbone geometry, residue contacts and flexibility, all computed in your browser.

![Protein Explorer](screenshot.png)
<img width="1920" height="822" alt="screenshot (1)" src="https://github.com/user-attachments/assets/9e236362-d2c7-42a2-865c-0d86e0526e07" />


## What it does

- **3D viewer** : cartoon, sticks, spheres and surface styles, with colouring by secondary structure or, for predicted models, by prediction confidence. Drag to rotate, scroll to zoom, right-drag to pan.
- **Ramachandran plot** : every residue by its backbone φ and ψ angles, coloured by fold state. Click a point to jump to that residue in the viewer.
- **Contact map** : the Cα–Cα distance matrix. Hover for any residue pair and its separation; click to highlight both.
- **Mobility against depth** : B-factor against distance from the centre of mass, with a least-squares fit and correlation coefficient. For AlphaFold models this becomes confidence against depth, since the B-factor column carries pLDDT.
- **Sequence strip** : the resolved chain one letter per residue, coloured by fold, with gaps shown where the density ran out.
- **Lab numbers** : molecular weight, theoretical pI, extinction coefficient and A280 conversion, GRAVY, plus crystallisation conditions, space group, Matthews coefficient and solvent content read from the deposition.
- **Export** : every field as a tab-separated row, ready to paste into a comparison spreadsheet, with a matching header row.
- **Guided starters** : six annotated structures to begin with, including a predicted model to compare against its experimental counterpart.
- **AlphaFold support** : load by UniProt accession, the current model file is found through the AlphaFold API rather than hard-coded.

Deep links work: `#1JNK` opens that structure, and `#1JNK/lab` opens it on a particular screen.

## Built with

HTML, CSS and JavaScript — no framework and no build step, so it runs as a single static file.

- [3Dmol.js](https://3dmol.csb.pitt.edu) for the molecular viewer
- [RCSB Protein Data Bank](https://www.rcsb.org) for experimental structures and entry metadata
- [AlphaFold Protein Structure Database](https://alphafold.ebi.ac.uk) for predicted models (CC BY 4.0)

Every parameter on the page is calculated in the browser from the coordinate file. Nothing is precomputed and there is no server.

## Why I built it
<img width="1000" height="283" alt="banner" src="https://github.com/user-attachments/assets/9b9be73a-35eb-473c-89ff-da4cdbdad3ca" />

![DUDE I LOVE PROTEINS!](banner.gif)

## Running it locally

Clone the repository and open `index.html` in a browser. There is nothing to install and nothing to build.

```bash
git clone https://github.com/juvasshini/protein-explorer.git
cd protein-explorer
open index.html
```

## Licence

MIT — see [LICENSE](LICENSE). Structure data belongs to the RCSB PDB and the AlphaFold DB under their own terms.

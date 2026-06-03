# Radiology Diagnostic Portal — jamesxxx1997

A personal radiology imaging-diagnosis meta-site (pure static HTML/JS, hosted on GitHub Pages).
Open `index.html`, pick an organ system, and explore the interactive diagnostic tree
(Mermaid mind-map + hover tooltips, plus small decision-support calculators).

## Credits & sources

This site is built on top of the structure and content created by **Dr. Irene Lee (學姊)**:
<https://drireneleemd.github.io/diagnostic-tools/>

| Marker | Meaning |
|--------|---------|
| 📘 Blue | Diagnostic tree by **Dr. Irene Lee** — adapted from her original meta-site |
| 📗 Green | Section built by **jamesxxx1997** from my own imaging notes |

### How each organ is composed

- **Senior-only organs** (brain, spinal_cord, bones, lungs, heart, kidneys, spleen, stomach,
  bowel, urinary_bladder): Dr. Lee's tree, re-hosted with a 📘 attribution banner.
- **Shared organs** (adrenal_glands, liver, pancreas): a combined page that stacks
  **Section 1 (📘 Dr. Lee)** above **Section 2 (📗 jamesxxx1997)**, each in its own frame.
- **My-only organs**: none yet — will be added as new notes are written.

My sections are distilled (imaging content only) from personal notes:
- Adrenal — MRI chemical-shift / T2-first tree (complements Dr. Lee's HU-branch tree)
- Liver — dynamic-enhancement-first tree + ancillary chemical-shift / T2 / DWI / haemorrhage tables
- Pancreas — imaging-only PDAC workup (epidemiology / risk / clinical sections removed)

## File layout

```
index.html                       master dashboard (organ grid + source legend)
Organ/
  <organ>.html                   senior-only pages (📘 banner + Dr. Lee's tree)
  adrenal_glands.html            combiner: senior frame + mine frame
  liver.html                     combiner
  pancreas.html                  combiner
  senior/<organ>.html            Dr. Lee's original pages (unmodified)
  mine/<organ>.html              my distilled trees
```

## Deploy (GitHub Pages)

```bash
cd ~/radiology-tools
git init && git add -A && git commit -m "Initial radiology meta-site"
git branch -M main
git remote add origin https://github.com/Jamesxxx1997/radiology-tools.git
git push -u origin main
# then: GitHub → repo Settings → Pages → Branch: main / root → Save
# live at: https://jamesxxx1997.github.io/radiology-tools/
```

> Educational reference only — not a substitute for formal radiology reporting or clinical judgement.

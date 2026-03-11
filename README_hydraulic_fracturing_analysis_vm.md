# 🛢️ Hydraulic Fracturing Operations Analysis
### Vaca Muerta — Completion Data Analytics Portfolio

**Author:** Stefania Dottori  
**Role:** Energy Systems & Completion Data Analyst  
**Field Experience:** Halliburton (Argentina · Mexico · USA) — 2013–2018  
**Operators:** TotalEnergies · Repsol · Chevron · YPF · Petrobras  

---

## 📌 Project Overview

This project demonstrates end-to-end data analysis of hydraulic fracturing operations in **Vaca Muerta**, one of the world's largest unconventional hydrocarbon plays.

The dataset combines simulated operational data with geological properties sourced from **peer-reviewed scientific literature**, validated against the author's direct field experience as sole field engineer on multi-stage horizontal completions.

> *"I was in the field interpreting this data in real time. Now I'm letting the data tell the story."*

---

## 🎯 Business Questions Answered

| Question | Finding |
|---|---|
| Which formation has the highest screen-out risk? | La Cocina (ductile, anoxic environment) |
| Does a better fracture always mean more production? | No — TOC and porosity outweigh fracturability |
| Which PDAT parameter best predicts IP? | Fracture Half-Length (SRV proxy) |
| How do decline rates differ by formation? | La Cocina 2x faster than Organico |
| What is the optimal landing zone? | Organico — best balance of fracturability + reservoir quality |

---

## 📂 Repository Structure

```
📁 Portfolio Stefania Dottori/
│
├── 📓 analisis_fractura_vm.ipynb     ← Main analysis notebook
│
├── 📊 Data/
│   ├── 01_pozos.csv                  ← 40 horizontal wells
│   ├── 02_etapas_frac.csv            ← 1,255 frac stages
│   ├── 03_parametros_operacionales.csv ← Treating pressure, ISIP, slurry rate...
│   ├── 04_pdat_diagnostico.csv       ← DFIT / Minifrac / Step-Rate analyses
│   ├── 05_eventos_anomalias.csv      ← Screen-outs, pressure spikes, delays
│   ├── 06_produccion_post_frac_v2.csv ← 24-month decline curves
│   └── 07_propiedades_geologicas_v3.csv ← Geological properties by formation
│
├── 📈 Figures/
│   ├── fig01_screenout_analysis.png
│   ├── fig02_geological_properties.png
│   ├── fig03_fracture_geometry.png
│   ├── fig04_decline_curves.png
│   └── fig05_pdat_predictor.png
│
└── 📄 README.md
```

---

## 🗄️ Dataset Description

**5,000+ records across 6 tables:**

| Table | Records | Key Parameters |
|---|---|---|
| Wells | 40 | Operator, field, formation, lateral length, TVD |
| Frac Stages | 1,255 | Stage status, fluid type, proppant, cluster count |
| Operational Params | 1,255 | Treating pressure, ISIP, BHTP, slurry rate, fluid efficiency, net pressure |
| PDAT Diagnostics | 1,196 | Closure pressure, permeability (nD), skin factor, half-length, Cw |
| Anomaly Events | 446 | Screen-outs, pressure spikes, rate drops, tortuosity |
| Production | 960 | Oil (bopd), GOR, water cut, WHP — 24-month Arps decline |

**Geological Properties** (per formation, from published literature):

| Formation | TOC (%) | Young's Modulus (GPa) | Brittleness | Depositional Environment |
|---|---|---|---|---|
| Loma Amarilla | 4.5 | 35.0 | 0.76 | Shallow Marine Carbonate Ramp |
| La Cocina | 3.0 | 14.0 | 0.38 | Deep Marine Anoxic Basin |
| Organico | 6.5 | 24.0 | 0.58 | Transitional Marine Ramp |

---

## 🔍 Key Findings

### 1. Screen-out Risk — La Cocina is the most challenging formation
La Cocina's ductile behavior (Young's Modulus 14 GPa), combined with well-preserved lamination from its anoxic depositional environment, generates complex fracture geometry — limiting proppant transport and increasing screen-out risk.

### 2. Fracturability ≠ Producibility
Loma Amarilla (most brittle, BI=0.76) produces the longest fractures — but the lowest IP due to lower TOC (4.5%) and porosity (9.5%). **Organico achieves the highest IP** despite intermediate fracturability, driven by its superior reservoir quality (TOC 6.5%, porosity 11.5%).

### 3. Fracture Half-Length is the strongest IP predictor
Among all PDAT parameters, **fracture half-length** shows the highest correlation with Initial Production — confirming that Stimulated Reservoir Volume (SRV) is the primary production driver in Vaca Muerta shale.

> This justifies PDAT as an economic investment: low half-length in early stages should trigger real-time job redesign to maximize SRV in subsequent stages.

### 4. Decline rates differ significantly by formation
| Formation | Di (monthly) | Year-1 Decline |
|---|---|---|
| La Cocina | 12% | ~75% |
| Loma Amarilla | 8% | ~60% |
| Organico | 6% | ~50% |

---

## 🛠️ Tech Stack

```
Python 3.11       pandas · numpy · matplotlib · seaborn · scipy
SQL / PostgreSQL   (Phase 2 — Power BI integration)
Power BI          (Phase 2 — Interactive dashboard)
Claude API        (Phase 3 — Natural language data agent)
```

---

## 📚 Data Sources & References

**Operational data:** Simulated with technically realistic distributions,  
validated against author's field experience in hydraulic fracturing  
(Halliburton, Vaca Muerta / Eagle Ford / Burgos Basin, 2013–2018)

**Geological properties:**
- SPE URTeC-2154603 — *Pore system characterization, El Trapial field*
- SPE URTeC-2437257 — *Simplified petrophysical model, Vaca Muerta*
- Espinoza, D. (2020) — *Geomechanical properties of Vaca Muerta*, U.Texas
- AAPG Wiki — *Vaca Muerta Shale Play*
- AAPG Memoir 121, Ch.13 — *Geomechanics, pressure regimes & hydraulic fractures*
- SPE URTeC-2460081 — *Shell, lateral continuity study*

---

## 🗺️ Portfolio Roadmap

- [x] **Phase 1** — Python data analysis (this notebook)
- [ ] **Phase 2** — Power BI interactive dashboard
- [ ] **Phase 3** — Claude API data agent (natural language queries)
- [ ] **Phase 4** — One-page consulting business case

---

## 👩‍💼 About the Author

Geologist and former Field Engineer at Halliburton with 5 years of international experience operating hydraulic fracturing, acid stimulation, and PDAT jobs on horizontal multi-stage unconventional wells.

Sole engineer-in-charge on 18–45 stage completions across **Vaca Muerta, Neuquén Basin, Burgos Basin and Eagle Ford**, serving operators including TotalEnergies, Repsol, Chevron, YPF and Petrobras.

Now combining deep operational domain knowledge with a **Master's in Data Science & AI** to deliver completion analytics and digital strategy for the upstream sector.

📧 stefania.dottori@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/stefaniadottori)  
📍 Barcelona, Spain

---

*This project is part of an active portfolio in development. Phases 2–4 coming soon.*

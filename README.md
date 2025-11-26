# When Society Fails Women: GBV & Femicide Figures for South Africa

This repository contains the code used to generate a set of data visualisations on gender–based violence (GBV) and femicide in South Africa. The figures are designed as a **16-day “data walk”** to accompany an article for the 16 Days of Activism campaign:

> **“When Society Fails Women: A Data Walk Through GBV in South Africa”**

Each visual corresponds to one day and one key question about women’s safety, experience of violence, and the failures of systems meant to protect them.

---

## What this notebook does

The main notebook (e.g. `gbv_femicide_figures.ipynb`) generates a series of PNG images saved under `img/`. The figures are grouped roughly into four themes:

1. **Everyday danger & prevalence**
   - **DAY 1 – Feelings of safety:** dot plot comparing how safe women feel walking alone at night across countries (`dayX_feel_safe_global_dotplot.png`).
   - **DAY 2 – Experience of violence:** 100-women waffle chart showing how many have experienced physical/sexual violence, and how many are currently living with it (`dayX_exp_violence.png`).
   - **DAY 3 – Types of sexual offences:** proportional bar showing the composition of sexual offences reported to SAPS (`dayX_sexual_offences_composition.png`).
   - **DAY 4 – Disability & IPV:** lollipop chart comparing intimate partner violence for women with and without disabilities (`dayX_women_disability_ipv_lollipop.png`).

2. **When violence becomes deadly**
   - **DAY 5 – Murders per day & time of day:** stylised timeline of how many women are murdered in an average day and when across the 24-hour clock (`dayX_murders_time_of_day.png`).
   - **DAY 6 – Who kills women:** same timeline, coloured to show murders by intimate partners/family vs others (`dayX_murders_who_kills.png`).
   - **DAY 7 – Femicide trends:** stacked area chart of intimate partner, non-partner and unknown femicide rates over time (`dayX_femicide_trends_stack.png`).
   - **DAY 8 – Mechanisms of killing:** 100% stacked area chart of firearm, stabbing, blunt force and other methods (`dayX_how_are_women_killed_shares.png`).
   - **DAY 9 – Rape-related femicides:** 100% bars comparing the average share of femicides that involve rape for partner vs non-partner killers (`dayX_rape_femicides_avg.png`).

3. **Where violence happens & service load**
   - **DAY 10 – Sexual offences per 100k women:** provincial bar chart of sexual offences per 100,000 women (`dayX_sexual_offences_per_100k_women.png`).
   - **DAY 11 – Rape cases per TCC:** provincial bar chart of rape cases per Thuthuzela Care Centre (`dayX_rape_per_TCC_by_province.png`).
   - **DAY 12 – Prior IPV known to police:** 10-square chart showing how often intimate partner violence had already been reported before femicide (`dayX_prior_ipv_knowledge.png`).

4. **Justice system failures & survivor experiences**
   - **DAY 13 – The justice funnel:** horizontal funnel showing how 100 rapes drop off from occurrence to conviction (`dayX_rape_funnel.png`).
   - **DAY 14 – Convictions for femicide:** 10-square chart showing how many killers of women are convicted, for partner vs non-partner femicide (`dayX_convictions.png`).
   - **DAY 15 – Why survivors don’t report:** bar chart of reasons for not reporting rape (fear of reprisals, lack of trust in police, etc.) (`dayX_why_not_report_bars.png`).
   - **DAY 16 – Barriers in the system:** bar chart of barriers survivors face when reporting and seeking services (no info on rights/services, long waits, dismissive treatment, etc.) (`dayX_barriers_services.png`).

All plots are styled to use a consistent pink/red palette, minimal chart ink, and titles that are ready for direct use in an article or blog post.

---

## Data sources

The notebook relies on several data files stored in a `data/` directory. Key sources include:

- **SAPS Crime Statistics (2014–2024)**  
  `data/Sexual_Offence_Crimes_Reported_per_province_2014-2024.csv`  
  Used for:
  - Total rape and sexual offence counts per province
  - Composition of sexual offences (rape, sexual assault, attempted sexual offences, contact sexual offences)
  - Derived indicators:
    - Sexual offences per 100,000 women by province
    - Rape cases per Thuthuzela Care Centre

- **Perceptions of safety**  
  `data/safe_walk_2024.xlsx`  
  Cross-country data on the share of women who feel safe walking alone at night.

- **Convictions & rape-related femicides**  
  `data/convictions.csv`  
  Age-standardised femicide rates over time and information on rape-related femicides, by intimate partner vs non-partner.

- **IPV & disability**  
  Intimate partner violence prevalence for women with and without disabilities, from South African GBV survey data (manually re-entered as a small table in the notebook).

- **Barriers to reporting & services**
  - Reasons for not reporting rape (Stats SA / earlier national victimisation data).
  - Barriers in accessing justice and services from CFJ’s *Barriers to Justice: Gender-Based Violence in South Africa* (Western Cape sample).

---

## File structure

A typical layout for this project:

```text
.
├── data/
│   ├── safe_walk_2024.xlsx
│   ├── Sexual_Offence_Crimes_Reported_per_province_2014-2024.csv
│   ├── convictions.csv
│   ├── cause_of_death.csv
├── img/
│   ├── dayX_feel_safe_global_dotplot.png
│   ├── dayX_exp_violence.png
│   ├── dayX_sexual_offences_composition.png
│   ├── dayX_women_disability_ipv_lollipop.png
│   ├── dayX_murders_time_of_day.png
│   ├── dayX_murders_who_kills.png
│   ├── dayX_femicide_trends_stack.png
│   ├── dayX_how_are_women_killed_shares.png
│   ├── dayX_rape_femicides_avg.png
│   ├── dayX_sexual_offences_per_100k_women.png
│   ├── dayX_rape_per_TCC_by_province.png
│   ├── dayX_prior_ipv_knowledge.png
│   ├── dayX_rape_funnel.png
│   ├── dayX_convictions.png
│   ├── dayX_why_not_report_bars.png
│   └── dayX_barriers_services.png
├── visualisations_v2.ipynb
└── README.md

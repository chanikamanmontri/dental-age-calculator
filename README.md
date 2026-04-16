# Dental Age Calculator

A web-based tool for estimating dental age in children and adolescents using the Demirjian staging system. Designed for teaching and research in pediatric dentistry and forensic odontology.

## Methods

The calculator implements four dental age estimation methods based on the developmental stages (A–H) of seven mandibular left permanent teeth:

- **Demirjian 1973** — Classical 7-teeth method. Maturity scores from Table 2 are summed and converted to dental age via the Table 3 lookup (ages 3.0–16.0 yr).
- **Duangto 2016** — Thai population-specific 7-teeth method. Quadratic regression applied to the Demirjian 1973 maturity score (ages 6–15 yr).
- **Duangto 2018 Method I** — 4-teeth method using teeth 37, 36, 35, 34. Scores from Demirjian & Goldstein 1976 Table 3 with Thai-specific regression (ages 7–15 yr).
- **Duangto 2018 Method II** — 4-teeth method using teeth 37, 35, 34, 31. Scores from Demirjian & Goldstein 1976 Table 4 with Thai-specific regression (ages 7–15 yr). Suitable when the first permanent molar (tooth 36) is missing.

All results include 95% predictive intervals.

## Versions

| File | Description |
|------|-------------|
| `dental_age_calculator.html` | Desktop version with hover-to-highlight stage reference diagram |
| `dental_age_calculator_mobile_v2.html` | Mobile-friendly version with embedded stage reference image and touch-optimized tooth staging blocks |

Both are self-contained single HTML files — no server, no installation, no external dependencies.

## Live demo

- **Desktop:** [https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator.html](https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator.html)
- **Mobile:** [https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator_mobile_v2.html](https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator_mobile_v2.html)

## How to use

1. Select **sex** (male or female).
2. Enter **date of birth** and **date of X-ray** using the calendar picker. Chronological age is computed automatically.
3. **Stage each tooth** (37 to 31) by comparing the panoramic radiograph with the Demirjian reference chart and selecting the matching stage (A–H).
4. The calculator displays the maturity score and four dental age estimates with predictive intervals and difference from chronological age.
5. Use **Copy result** to paste the data (with column headers) into a spreadsheet.

## Important notes

- For **education and research purposes only**. Not intended for clinical or forensic decision-making without verification against original source materials.
- Scores are **sex-specific** — girls reach the same dental developmental stage at younger chronological ages than boys.
- The Duangto equations were developed and validated in **Thai children and adolescents**. Their accuracy may differ in other populations.
- The Demirjian 1973 classical method uses a **French-Canadian reference sample** and may overestimate dental age in some populations.

## Sources

- Demirjian A, Goldstein H, Tanner JM. A new system of dental age assessment. *Hum Biol* 1973;45:211–227.
- Demirjian A, Goldstein H. New systems for dental maturity based on seven and four teeth. *Ann Hum Biol* 1976;3:411–421.
- Duangto P, Janhom A, Prasitwattanaseree S, Mahakkanukrauh P, Iamaroon A. New prediction models for dental age estimation in Thai children and adolescents. *Forensic Sci Int* 2016;266:583.e1–e5.
- Duangto P, Janhom A, Prasitwattanaseree S, Iamaroon A. New equations for age estimation using four permanent mandibular teeth in Thai children and adolescents. *Int J Legal Med* 2018;132:1743–1747.
- Azarbakhsh G, Iranparvar P, Tehranchi A, Moshfeghi M. Relationship of vitamin D deficiency with cervical vertebral maturation and dental age in adolescents: a cross-sectional study. *Int J Dent* 2022;2022:7762873. (Stage reference chart, adapted under CC BY 4.0.)

## Author

Developed by **Chanika Manmontri**, Faculty of Dentistry, Chiang Mai University, with the assistance of Claude (Anthropic).

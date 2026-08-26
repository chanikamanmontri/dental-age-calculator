# Dental Age Calculator

A web-based tool for estimating dental age in children and adolescents using the Demirjian staging system. Designed for teaching and research in pediatric dentistry and forensic odontology.

## Methods

The calculator implements five dental age estimation methods based on the developmental stages (A–H) of seven mandibular left permanent teeth:

- **Demirjian 1973** — Classical 7-teeth method. Maturity scores from Table 2 are summed and converted to dental age via the Table 3 lookup (ages 3.0–16.0 yr).
- **Willems 2001** — Belgian adaptation of the Demirjian 7-teeth method. Per-tooth scores are expressed directly in years and summed, so no conversion table is needed (effective range ~3–17 yr).
- **Duangto 2016** — Thai population-specific 7-teeth method. Quadratic regression applied to the Demirjian 1973 maturity score (ages 6–15 yr).
- **Duangto 2018 Method I** — 4-teeth method using teeth 37, 36, 35, 34. Scores from Demirjian & Goldstein 1976 Table 3 with Thai-specific regression (ages 7–15 yr).
- **Duangto 2018 Method II** — 4-teeth method using teeth 37, 35, 34, 31. Scores from Demirjian & Goldstein 1976 Table 4 with Thai-specific regression (ages 7–15 yr). Suitable when the first permanent molar (tooth 36) is missing.

All results include 95% predictive intervals.

## Record sheet features

- **Panoramic radiograph.** The patient's panoramic film can be added to the record: click the upload area, drag and drop the file, or paste an image from the clipboard (Ctrl + V). An optional caption can be added. The image is held in the browser only — nothing is uploaded to any server — and it is cleared by the Reset button.
- **One-page printout.** Print (or save as PDF) fits a complete record on a single A4 page at 100% scale, with no custom scaling needed. The printed sheet shows the case details as plain text, the panoramic radiograph, the staging, all five dental age estimates, and the reference notes.

## Versions

| File | Description |
|------|-------------|
| `dental_age_calculator_desktop_version.html` | Desktop version with hover-to-highlight stage reference diagram and the full staging table on the printout |
| `dental_age_calculator_mobile_version.html` | Mobile-friendly version with embedded stage reference image, touch-optimized tooth staging blocks, and a compact staging table on the printout |

Both are self-contained single HTML files — no server, no installation, no external dependencies. The desktop version loads `demirjian_stages.png` from the same folder; the mobile version embeds the chart in the file.

## Live demo

- **Desktop:** [https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator_desktop_version.html](https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator_desktop_version.html)
- **Mobile:** [https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator_mobile_version.html](https://chanikamanmontri.github.io/dental-age-calculator/dental_age_calculator_mobile_version.html)

## How to use

1. Select **sex** (male or female).
2. Enter **date of birth** and **date of X-ray** using the calendar picker. Chronological age is computed automatically.
3. Optionally **add the panoramic radiograph** — click the upload area, drag the file in, or paste it from the clipboard.
4. **Stage each tooth** (37 to 31) by comparing the panoramic radiograph with the Demirjian reference chart and selecting the matching stage (A–H).
5. The calculator displays the maturity score and five dental age estimates with predictive intervals and difference from chronological age.
6. Use **Copy result** to paste the data (with column headers) into a spreadsheet, or **Print** to produce a one-page A4 record (keep the print scale at 100%).

## Important notes

- For **education and research purposes only** — not for clinical or forensic decision-making without verification against original source materials.
- Scores are **sex-specific**. Girls reach the same developmental stage at younger ages than boys. Selecting the wrong sex will shift all results.
- The **Demirjian 1973** classical method uses a French-Canadian reference sample and may overestimate dental age in some populations.
- The **Willems 2001** tables were developed in Belgian Caucasian children. The paper reports no formal SEP; the standard deviations of the validation-sample error (0.9 yr for boys, 1.3 yr for girls) are used here to build the predictive interval.
- The **Duangto equations** were developed in Thai children and adolescents. Accuracy may differ in other populations.
- **Children near the lower or upper age limits.** The Duangto formulas are quadratic curves fitted within a specific age range (6–15 yr for Duangto 2016; 7–15 yr for Duangto 2018). Near either boundary the curves can behave unpredictably:
  - **Young children (near the lower limit):** the curve can swing sharply upward and produce dental ages much higher than expected. For example, a 7-year-old male may get a Duangto 2016 estimate above 10 years, even though the Demirjian 1973 result is close to the true age.
  - **Older children (near the upper limit):** most teeth have reached stage G or H and the maturity score approaches its ceiling. Small scoring differences translate into large age differences, making all methods — including Demirjian 1973 — less precise. The Duangto curves also flatten in this region and may under- or overestimate.
  
  When the patient's chronological age is near or outside the validity range, interpret all results with caution. For young children, **the Demirjian 1973 result is generally more reliable** because it uses a direct lookup table rather than extrapolation. For older children nearing full dental maturity, **no method provides high precision** — report the result with its predictive interval and note the limitation.

## Sources

- Demirjian A, Goldstein H, Tanner JM. A new system of dental age assessment. *Hum Biol* 1973;45:211–227.
- Demirjian A, Goldstein H. New systems for dental maturity based on seven and four teeth. *Ann Hum Biol* 1976;3:411–421.
- Willems G, Van Olmen A, Spiessens B, Carels C. Dental age estimation in Belgian children: Demirjian's technique revisited. *J Forensic Sci* 2001;46(4):893–895.
- Duangto P, Janhom A, Prasitwattanaseree S, Mahakkanukrauh P, Iamaroon A. New prediction models for dental age estimation in Thai children and adolescents. *Forensic Sci Int* 2016;266:583.e1–e5.
- Duangto P, Janhom A, Prasitwattanaseree S, Iamaroon A. New equations for age estimation using four permanent mandibular teeth in Thai children and adolescents. *Int J Legal Med* 2018;132:1743–1747.
- Azarbakhsh G, Iranparvar P, Tehranchi A, Moshfeghi M. Relationship of vitamin D deficiency with cervical vertebral maturation and dental age in adolescents: a cross-sectional study. *Int J Dent* 2022;2022:7762873. (Stage reference chart, adapted under CC BY 4.0.)

## Author

Developed by **Chanika Manmontri**, Faculty of Dentistry, Chiang Mai University, with the assistance of Claude (Anthropic).

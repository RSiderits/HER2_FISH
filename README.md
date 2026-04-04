# HER2_FISH
HER2 FISH Signal counter

HER2 CAP Proficiency Survey / FISH Group Calculator
README

Overview
This HTML document is a browser-based calculator for entering paired centromere and HER2 signal counts by nucleus and generating a structured HER2 FISH summary. It was designed to support quick review of counted nuclei, automated result calculations, visual assessment of HER2 signal distribution, and standardized reporting output.

Core Functions
1. Sample Information
   - Stores Sample Name and Sample ID in the working session.
   - Includes these fields in the copied report.

2. Manual Pair Entry
   - Enter a Centromere count and a HER2 Signal count for each nucleus.
   - Press Enter from the Centromere field to move to HER2 Signal.
   - Press Enter in HER2 Signal to add the pair.
   - Add, Delete, and Clear functions are provided.

3. Running Calculations
   The calculator automatically updates:
   - Cells counted
   - Average HER2 signals per nucleus
   - Average centromere signals per nucleus
   - HER2 / centromere ratio
   - HER2 standard deviation
   - Coefficient of variation (CV)

4. CAP Group Assignment
   The calculator assigns the CAP-style HER2 group:
   - Group 1: Ratio >= 2.0 and Avg HER2 >= 4 -> Positive
   - Group 2: Ratio >= 2.0 and Avg HER2 < 4 -> Additional workup
   - Group 3: Ratio < 2.0 and Avg HER2 >= 6 -> Positive
   - Group 4: Ratio < 2.0 and Avg HER2 >= 4 and < 6 -> Additional workup
   - Group 5: Ratio < 2.0 and Avg HER2 < 4 -> Negative

5. Heterogeneity Scoring
   Heterogeneity is based on the coefficient of variation (CV) of HER2 signal counts:
   - Low heterogeneity: CV 0.25 to 0.40
   - Moderate heterogeneity: CV > 0.40 to 0.60
   - High heterogeneity: CV > 0.60
   - Values below 0.25 are reported as below the low heterogeneity range

6. Bimodality Detection
   The calculator evaluates the HER2 signal distribution for clear bimodality.
   It looks for:
   - At least two meaningful peaks
   - Adequate separation between the peaks
   - A valley between the peaks
   If these criteria are met, the result is reported as bimodal and the histogram marks the detected peaks with red dashed lines.

7. Histogram
   The histogram displays the number of nuclei at each HER2 signal count.
   This helps visualize clustering, spread, and possible bimodality.

New Chromosome Gain / Polysomy Function
A chromosome gain / polysomy assessment has been added to the HTML document.

Purpose
This feature provides a separate estimate of increased centromere copy number so that chromosome gain is not confused with focal HER2 amplification.

How It Works
The calculator uses the average centromere count per nucleus and assigns a category:
- No polysomy: Avg Centromere < 2.25
- Mild polysomy / low-level gain: Avg Centromere 2.25 to < 3.0
- Moderate polysomy: Avg Centromere 3.0 to < 4.0
- Marked polysomy: Avg Centromere >= 4.0

Display
Two new result fields are shown:
- Chromosome Gain
- Gain Note

Interpretive Explanation
This assessment is intentionally separate from the HER2 amplification result.
A high HER2 signal count with proportionally increased centromere counts may lower the ratio and may reflect chromosome gain rather than focal amplification.
In other words:
- Polysomy / chromosome gain is not the same as focal HER2 amplification
- The ratio remains important when deciding whether increased HER2 counts represent focal amplification or broader chromosome copy number gain

Copied Report Output
The Copy Report function now includes:
- Chromosome Gain / Polysomy category
- Gain Note

Typical Use
1. Open the HTML file in a browser.
2. Enter sample identifiers.
3. Enter paired centromere and HER2 values nucleus by nucleus.
4. Review the automatically updated results.
5. Review the histogram and bimodality output.
6. Review the chromosome gain / polysomy result as a separate interpretive aid.
7. Use Copy Report to export the summarized text.

Important Interpretation Note
This document is a calculation and visualization aid. Final interpretation should still be based on the laboratory's validated assay, interpretive framework, and medical director or pathologist review.


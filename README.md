# Anomalies_Detection
Geospatial analysis of 2023 Zamfara State election results to detect polling unit irregularities using geodesic distance and outlier scoring
# Zamfara Election Anomaly Detection

## Overview
This project investigates potential voting irregularities in Zamfara State 
during the 2023 Nigerian general elections. Using geospatial analysis and 
outlier detection techniques, polling units with abnormal vote counts relative 
to their geographic neighbours were identified.

## Dataset
- Source: Zamfara State crosschecked polling unit results (HNG Tech, 2023)
- Features: Polling unit names, party vote counts (APC, PDP, LP, NNPP), 
  Latitude, Longitude

## Tools & Libraries
- Python, Pandas, NumPy, Geopy, Matplotlib, Seaborn
- Google Sheets (Geocode by Awesome Table add-on)

## Methodology
- Geocoded polling units using Google Sheets
- Identified neighbouring units within a 1km geodesic radius using Geopy
- Calculated outlier scores by comparing each unit's votes to its 
  neighbours' average
- Visualised anomalies using party-coded scatterplots

## Key Findings
- **Keta I/Makaranta** recorded the highest PDP outlier score of 115.0 
  (120 votes vs neighbourhood average of 5.0)
- **Shamushale I/Shiyar Sabon Gari** recorded the highest APC outlier 
  score of 87.5
- LP and NNPP showed minimal irregularities with scores rarely exceeding 2.85
- Irregularities were concentrated in specific wards, suggesting localised 
  anomalies

## Top 3 Outlier Polling Units
| Polling Unit | Party | Votes | Neighbourhood Avg | Outlier Score |
|---|---|---|---|---|
| Keta I/Makaranta | PDP | 120 | 5.0 | 115.0 |
| Bakin Gulbi/Danfako | PDP | 95 | 6.0 | 89.0 |
| Shamushale I/Shiyar Sabon Gari | APC | 100 | 12.5 | 87.5 |

## Additional Resources
- [Full Analysis with Coordinates & Outlier Scores](https://drive.google.com/file/d/1HtzqOBVQJ7gg45M2LSqS5WHxkPCMwEo1/view?usp=drivesdk)
- [Sorted Outlier Scores by Party](https://docs.google.com/spreadsheets/d/1Ojy92eyk26hIP3UsfgMwegxIpra_QcDu/edit?usp=drivesdk&ouid=118001723712366640479&rtpof=true&sd=true)

## Conclusion
Geospatial outlier detection proves to be a valuable tool for enhancing 
electoral transparency. Flagged polling units should be prioritised for 
further investigation by relevant authorities.

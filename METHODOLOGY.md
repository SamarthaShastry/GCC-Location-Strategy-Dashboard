# Methodology

## Data Collection
All underlying data sourced from "Emerging Technology Hubs of India" 
— Deloitte & NASSCOM, August 2023. 20 Tier-2 cities evaluated across 
25 metrics.

## Normalization Approach
All metrics normalized to a 0–100 scale using min-max normalization.
Density-adjusted metrics used throughout to eliminate large-city bias 
— raw counts replaced with per-capita and per-km² equivalents where 
applicable.

## Direction of Metrics
| Type | Metrics |
|---|---|
| Higher is better | Talent density, literacy, connectivity, ecosystem indices |
| Lower is better | Salary, office rental, cost of living, crime, pollution, EoDB rank |

## Pillar Score Calculation
Each pillar score = average of normalized scores of constituent metrics.

## Composite Score Calculation
Composite Score = Σ (Pillar Score × Pillar Weight) / Σ (All Weights)
Weights auto-normalize to sum to 100% regardless of input.

## Multicollinearity Treatment
Science & Tech Graduates vs Total Graduates (r=0.98) — raw counts 
replaced with percentage equivalents.
Tech Businesses vs Population (r=0.91) — density per km² used instead.

## Risk Flag Criteria
| Flag | Threshold |
|---|---|
| No metro | Metro network = 0 km |
| No flights | Daily flights = 0 |
| No SEZ | SEZ area = 0 km² |
| High pollution | Pollution index > 70 |
| High crime | Crime index > 55 |
| Low internet | Download speed < 30 Mbps |
| Low EoDB rank | EoDB rank > 15 |

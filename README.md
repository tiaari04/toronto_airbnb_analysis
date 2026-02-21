# Toronto Airbnb Listings Analysis — Excel Dashboard Project
## Overview
Analysis of 21,469 Airbnb listings across Toronto to uncover pricing patterns, neighbourhood trends, and what drives review ratings, built entirely in Microsoft Excel.
<img width="973" height="584" alt="image" src="https://github.com/user-attachments/assets/05f2ff1a-a15c-4309-82fe-8dc6db04e9ed" />

## Key Insights
* Listings in **Old Toronto** are generally more expensive than other areas of the city
* Higher price category listings consistently accommodate more guests across all neighbourhoods
* Listings in the **mid-to-very-high price range** tend to have better review ratings
* **Private rooms** are consistently cheaper than entire home listings
* Even across expensive and budget listings, price per guest stays between **$33–$90**, making group stays relatively predictable

## Process
### Data Cleaning
* Started with 21,469 listings, ending with 15,800 after cleaning
* Removed irrelevant and redundant columns, and filtered out listings missing price or bathroom data
* Assigned a rating of 0 to listings with no reviews, rather than leaving blanks

### Analysis
* **Outlier Detection** - Calculated quartiles, IQR, and fences per neighbourhood to flag outliers neighborhood by neighborhood, enabling analysis both with and without them
* **Price Per Guest** - Added a price_per_guest column (price / accommodates) to normalize pricing across listing sizes
* **Price Categories** - Used percentiles within each neighbourhood to bucket listings into Very Low / Low / Mid / High / Very High, allowing fair cross-neighbourhood comparisons
* **Neighbourhood Consolidation** - Grouped granular areas into broader neighbourhoods using the help of Google Maps (e.g. North & South Riverdale → Riverdale)

### Useful Charts not Included in Dashboard
<img width="964" height="441" alt="image" src="https://github.com/user-attachments/assets/609c27db-396f-418f-806d-b04b6dd0d91c" />
<img width="968" height="436" alt="image" src="https://github.com/user-attachments/assets/0c2410f8-ed2a-46d2-b4cd-16d495a8adaa" />
<img width="2004" height="581" alt="image" src="https://github.com/user-attachments/assets/beef7ad3-e9e7-434b-b1e5-d85e67f305f2" />

## Tools & Techniques
* **Pivot Tables** for aggregation and cross-tabulation
* **Advanced Formulas**: IFS, XLOOKUP, FILTER, QUARTILE, PERCENTILE, SORT, UNIQUE, IFERROR
* **Charts**: Bar and line
* **Dashboard Slicers** to filter by room type, neighbourhood, and outlier inclusion

## Data Source
Raw data from Inside Airbnb - an open-source project providing publicly available Airbnb listing data.

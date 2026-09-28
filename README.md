# Logistics & Transportation — Power BI Report

## Overview
`Logistics___Transportation.pbix` is a Power BI report analyzing delivery and fleet
performance. It has a two-table data model and a five-page report covering on-time
delivery, fuel efficiency, cost per km, and route-level delivery performance.

## Data Model
| Table | Role |
|---|---|
| **Trips** | Fact table: one row per trip. Fields used in the report include Route, Origin, Destination, Delivery_Status, and Delivery_Date (with a date hierarchy) |
| **Vehicle_Master** | Vehicle dimension/reference table |

### Measures (defined on `Trips`)
- **On-Time Delivery %** — share of trips delivered on time
- **Fuel Efficiency** — fuel performance, trended by month
- **Cost per km** — transport cost normalized by distance

## Report Pages
| Page | Content |
|---|---|
| **On-Time Delivery % by Route** | Clustered bar chart of On-Time Delivery % by Route |
| **Fuel Efficiency Trend by Month** | Line chart of Fuel Efficiency by month |
| **Cost per km** | KPI cards: Cost per km and On-Time Delivery % |
| **Delivery performance by route** | Map by Origin, colored by Delivery_Status, sized by On-Time Delivery % |
| **Dash Board** (default page) | Combined view: line chart, map, bar chart, two KPI cards, banner image and text boxes, plus slicers for **Delivery_Status** and **Destination** |

## Technical Details
- Page size: 1920 x 1080
- Theme: Fluent 2 (base theme)
- Embedded images: a semi-truck banner photo and a PNG graphic
- Created from the Power BI service (cloud), release 2026.08

## Opening the Report
1. Open the file in **Power BI Desktop**.
2. If prompted, refresh the data. The data is stored in the compressed data model inside the file.
3. Start on the **Dash Board** page and use the Delivery_Status and Destination slicers to filter.

## Notes
- This README was built from the report's layout and metadata. The data model itself is compressed, so full column lists, DAX formulas, and the Trips–Vehicle_Master relationship are not documented here. Open the **Model view** in Power BI Desktop to confirm them.

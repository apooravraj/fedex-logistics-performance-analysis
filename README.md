# FedEx Logistics Performance Analysis

Exploratory analysis of the SCMS Delivery History dataset, focused on delivery timeliness, shipment patterns, and logistics cost signals.

## Project questions

- How does delivery timeliness vary by shipment mode and destination?
- Do fulfillment method or vendor INCO terms show different delivery patterns?
- Is PO-to-scheduled lead time associated with delivery delay?
- Is recorded shipment weight associated with line-item insurance cost?

## Notebook

Open `FedEx_Logistics_Performance_Analysis.ipynb` in Google Colab and run all cells. When prompted, upload `SCMS_Delivery_History_Dataset.csv`. The notebook preserves the raw fields and handles text placeholders as missing values in derived calculations rather than converting them to zero.

## Tools

Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, Google Colab.

## Initial findings

In the supplied file, 88.5% of records with usable scheduled and delivered dates were on time or early. The late rate varied by recorded shipment mode and destination. Numeric weight and insurance values showed a strong positive rank association; this is descriptive and may also reflect product value or type.

## Data handling

The dataset contains 10,324 rows and 33 columns. There were no exact duplicate rows. Some shipment modes, dosage, and insurance values are missing. Weight, freight, and date fields also include text markers. The repository intentionally excludes the source CSV; add it in Colab when prompted.

## Limitations

Records represent line items and may not correspond one-to-one with unique shipments. Group comparisons are descriptive and do not establish causation. Validate unusual dates and compare like-for-like routes and products before making operational changes.

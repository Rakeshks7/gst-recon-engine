# GST Purchase Reconciliation Engine

A high-performance, privacy-first web application designed to reconcile Books of Accounts against GSTR-2B portal data. Built to handle complex financial datasets entirely within the client's browser, ensuring sensitive financial records never touch an external server.

## Features
* **Zero-Server Processing:** Utilizes the HTML5 `FileReader` API and `SheetJS` to process massive `.xlsx` and `.csv` files locally.
* **Smart Key Normalization:** Advanced string parsing algorithms to match inconsistent invoice formats (e.g., "INV-2023/01" vs "INV202301").
* **Automated Column Mapping:** Regex-powered auto-detection of standard accounting column headers, with a manual UI fallback.
* **Granular Tolerance Thresholds:** Configurable numeric tolerance levels to filter out minor rounding differences automatically.
* **Dynamic ITC Summary:** Real-time calculation of Input Tax Credit (ITC) categorization across IGST, CGST, SGST, and Cess.

## Tech Stack
* **Frontend:** HTML5, Vanilla JavaScript (ES6+), CSS3
* **Libraries:** [SheetJS (xlsx)](https://sheetjs.com/)
* **Backend Framework (Serving):** Python, Flask
* **Deployment Environment:** Google Cloud Run (Dockerized)

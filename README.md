# ShareVolume

## Summary

ShareVolume is a front-end application that retrieves and processes financial data from the U.S. Securities and Exchange Commission (SEC) XBRL API, focusing on Entity Common Stock Shares Outstanding. It analyzes historical filings (post-FY 2020) to determine and display the maximum and minimum share counts for a specified company, defaulting to Centene Corporation.

## Features

*   **SEC Data Integration:** Fetches real-time financial data using the SEC EDGAR API (`companyconcept` endpoint).
*   **Data Analysis:** Calculates and persists the maximum and minimum values of Common Stock Shares Outstanding (post-FY 2020) in the `data.json` file for the default company.
*   **Dynamic Rendering:** Renders a visually appealing interface (`index.html`) displaying the calculated statistics, ensuring the entity name is present in the page title and H1 header.
*   **CIK Parameter Support:** Supports dynamic data loading via a URL query parameter (`?CIK=`) to switch between different publicly traded companies without a page reload.
*   **API Compliance:** Adheres to SEC guidelines by utilizing a descriptive User-Agent during data retrieval (required for the pre-processing step that generates `data.json`).

## Setup

This project consists primarily of static HTML, CSS, and JavaScript files, along with pre-processed data. No complex backend installation or dependencies are required.

1.  **Clone the Repository:** Obtain the project files from the source repository.
2.  **Execution:** Open `index.html` directly in a modern web browser.
3.  **Note on Data Fetching:** To fully test the dynamic CIK functionality, which involves fetching external data
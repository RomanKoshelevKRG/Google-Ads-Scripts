# Google Ads Product Classifier

This Google Ads script automatically analyzes and classifies products from your Merchant Center based on their performance metrics (ROAS, impressions, clicks, cost, age). The results are exported to a Google Spreadsheet with automated visual formatting and dashboard generation.

## 🚀 Key Features

* **Product Categorization:** Automatically segments products into categories such as `star`, `cash_cow`, `bad_roas`, `zombie_content_issue`, and more.
* **Grace Period (Immunity):** Protect specific products from being flagged or excluded for a defined period.
* **Automated Dashboards:** Generates and updates charts showing the current distribution of products and their historical dynamics over time.
* **Visual Formatting:** Automatically applies color-coded conditional formatting to the spreadsheet based on product categories for quick visual analysis.

## 🛠 Installation & Setup

1. **Create a copy of a new Google Spreadsheet.**
2. **Copy the code** from the `script.js` (or `Code.gs`) file.
3. Open your Google Ads account -> **Tools and Settings** -> **Scripts**.
4. Create a new script and paste the copied code.
5. Update the `SPREADSHEET_URL` variable in the configuration block of the script with the URL of your new Google Spreadsheet.
6. Authorize the script (grant the necessary permissions to access Google Ads and Google Sheets).
7. Set up a schedule for the script (e.g., run daily in the morning).

## ⚙️ Configuration Parameters

At the top of the script, you can adjust key parameters to fit your business logic:
* `TARGET_CUSTOM_LABEL`: Which custom label to use for exporting (0, 1, 2, 3, or 4).
* `LOOKBACK_DAYS`: The time window for performance analysis (default is 30 days).
* `ROAS_STAR_THRESHOLD` / `ROAS_CASH_COW`: ROAS targets for identifying your best-performing products.
* `BAD_COST_THRESHOLD`: The maximum acceptable spend (without hitting target ROAS) before a product is flagged as `bad_roas`.

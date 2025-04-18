
## 🔄 Power Query Transformations

### 📁 Source Files:
- `Email_campaign_analysis_dataset.xlsx` (Main dataset)
- `countries.xlsx` (Country metadata)

---

### 📌 Table: `email_data`

| Step | Transformation Description |
|------|----------------------------|
| 1️⃣ | **Imported Sheet**: Loaded the `email_data` sheet from Excel using `Excel.Workbook` and promoted headers. |
| 2️⃣ | **Changed Column Types**: Assigned appropriate data types to each column (e.g., `Date_sent` as date, `clicked`, `bounced`, etc. as integers). |
| 3️⃣ | **Extracted Domain Name**: Created a new column `Domain_Name` by extracting text between “@” and “.com” from `client_email`. |
| 4️⃣ | **Renamed Columns**: Renamed technical column names to friendly names (`Campaign_type` → `Campaign Type`, etc.). |
| 5️⃣ | **Standardized Country Names**: Replaced long or inconsistent country names (e.g., “Czech Republic” → “Czechia”, “Democratic Congo” → “Dem. Rep. Congo”, etc.) to ensure consistent mapping for visuals and filters. |
| 6️⃣ | **Removed Duplicate Country Modifications**: Final clean-up to ensure countries are uniquely named and not nested with repeated labels. |
| 7️⃣ | **Selected All Rows**: Applied a step to retain all rows (likely placeholder or ensured row count integrity). |

---

### 📌 Table: `countries_data`

| Step | Transformation Description |
|------|----------------------------|
| 1️⃣ | **Imported Sheet**: Loaded the `countries` sheet from Excel and promoted headers. |
| 2️⃣ | **Changed Column Types**: Ensured `country`, `Flag`, and `Continent` columns are in text format. |
| 3️⃣ | **Standardized Country Names**: Fixed name inconsistencies to align with `email_data` (e.g., “Macedonia [FYROM]” → “Macedonia”). |

---

### 📅 Date Table (Custom M Code):

A dynamic **Date Table** was generated based on `Date_sent` in `email_data`. Includes:

- **Basic Columns**: `Date`, `Year`, `Month`, `Day`, `Quarter`
- **Formatted Columns**: `MonthName`, `MonthName_short`, `WeekdayName`, `WeekdayName_short`
- **Weekend Flag**: `IsWeekend` indicates whether a date falls on a weekend.

```dax
DateTable = 
VAR MinDate = MIN(email_data[Date_sent])
VAR MaxDate = MAX(email_data[Date_sent])
RETURN
    ADDCOLUMNS(
        CALENDAR(MinDate, MaxDate),
        "Year", YEAR([Date]),
        "Month", MONTH([Date]),
        "MonthName", FORMAT([Date], "MMMM"),
        "MonthName_short", FORMAT([Date], "MMM"),
        "Day", DAY([Date]),
        "Quarter", QUARTER([Date]),
        "Weekday", WEEKDAY([Date], 2),
        "WeekdayName", FORMAT([Date], "dddd"),
        "WeekdayName_short", FORMAT([Date], "ddd"),
        "IsWeekend", IF(WEEKDAY([Date], 2) >= 6, TRUE, FALSE)
    )
```


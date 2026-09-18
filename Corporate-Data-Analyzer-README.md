# Corporate Data Analyzer — Python

A Python-based desktop application for analyzing CSV and Excel datasets, generating dynamic grouped reports, creating charts, and exporting analytical results.

## Project Overview

**Corporate Data Analyzer** is a reusable desktop data-analysis and reporting tool built with Python. Users can select a CSV or Excel file, inspect its structure, choose a text column for grouping, select a numeric value column and aggregation method, generate a summarized report, visualize the results, and export the output.

The application is designed to reduce repetitive manual reporting work and demonstrate a practical data-analysis workflow.

## Features

- Import CSV and Excel (`.csv`, `.xlsx`, `.xls`) files
- Display dataset rows, columns, and column headings
- Automatically identify text and numeric columns
- Basic data cleaning and numeric conversion
- Dynamic GroupBy-based report generation
- Supported aggregations: Sum, Mean, Average, Max, Min, Count, Median
- Preview generated reports in the application
- Create Bar, Column, Pie, and Line charts
- Limit large chart datasets to the top 10 records for readability
- Export reports to Excel (`.xlsx`) or CSV (`.csv`)
- Export charts as PNG images
- Save reports and charts to a user-selected location
- User-friendly Tkinter desktop interface

## Workflow

```text
CSV / Excel File
       ↓
   Read Dataset
       ↓
 Inspect Rows, Columns & Headings
       ↓
Identify Text & Numeric Columns
       ↓
 Select Group By Column
       ↓
 Select Aggregation
       ↓
 Select Numeric Value Column
       ↓
 Generate Report
       ↓
 Preview Report
       ↓
 Create Chart
       ↓
 Export Report / Chart
```

## Technology Stack

- **Python** — application development
- **Pandas** — data loading, cleaning, transformation, grouping, aggregation, and analysis
- **Tkinter / ttk** — desktop graphical user interface
- **Matplotlib** — chart creation and visualization

## Project Structure

```text
Corporate-Data-Analyzer-Python/
│
├── Corporate_Data_Analyzer.py
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
│
├── screenshots/
│   ├── main-interface.png
│   ├── report-preview.png
│   └── chart-preview.png
│
└── sample_data/
    └── sample_corporate_data.csv
```

> The `screenshots/` and `sample_data/` folders are optional. Add them only if they are included in the repository.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Corporate-Data-Analyzer-Python.git
```

### 2. Open the project directory

```bash
cd Corporate-Data-Analyzer-Python
```

### 3. Create and activate a virtual environment (recommended)

Windows PowerShell:

```powershell
python -m venv venv
.env\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

## Requirements

The application uses:

```text
pandas
matplotlib
```

Tkinter is used for the desktop interface and is normally included with standard Python installations on Windows.

## How to Use

Run the application:

```bash
python Corporate_Data_Analyzer.py
```

Then:

1. Click **Browse** and select a CSV or Excel file.
2. Click **Read** to load the dataset.
3. Review the file information displayed by the application.
4. Select a **Group By** column.
5. Select an **Aggregation** such as Sum, Mean, Count, Median, Max, or Min.
6. Select a numeric **Value** column.
7. Click **Preview Report**.
8. Select a chart type.
9. Click **Preview Chart**.
10. Export the report as Excel/CSV or the chart as PNG.

## Report Generation

The application dynamically performs grouped analysis using the selected text column and numeric column.

Conceptually:

```python
df.groupby(group_column)[value_column].agg(aggregation)
```

The resulting report is sorted by value in descending order and displayed in the application.

## Data Handling

The application accepts datasets where numeric values may be stored as text. It attempts to identify numeric-looking columns and safely converts values such as:

```text
12,000
25,500
```

into numeric values for analysis.

Basic cleaning is also applied to the selected grouping column by removing leading/trailing spaces and standardizing text capitalization.

## Charting

Charts are generated from the report preview. Available visualizations include:

- Bar charts
- Column charts
- Line charts
- Pie charts

For readability, the application uses the top 10 records when a report contains more than 10 groups.

## Export

### Reports

Reports can be exported as:

- Excel workbook (`.xlsx`)
- CSV (`.csv`)

### Charts

Charts can be exported as:

- PNG (`.png`)

The application uses a Save As dialog so the user can choose the output filename and destination.

## Executable Version

If an `.exe` version of the application is provided separately, users can run the executable without manually launching the Python source file, provided the packaged application was built correctly for their system.

For GitHub distribution, the executable can also be attached to a GitHub Release rather than being treated as the main source of the project.

## Skills Demonstrated

- Python Programming
- Pandas
- Data Analysis
- Data Cleaning
- Data Transformation
- Data Aggregation
- GroupBy Operations
- Data Visualization
- Matplotlib
- Tkinter GUI Development
- File Handling
- CSV Processing
- Excel File Processing
- Reporting Automation
- Desktop Application Development

## Project Purpose

This project was developed as a practical portfolio project to demonstrate how Python can be used to build a reusable data-analysis and reporting application instead of performing every analysis manually.

It combines data processing, analysis, visualization, GUI development, and file export into a single desktop application.

## Limitations

- The application performs general-purpose data analysis and does not provide domain-specific business recommendations.
- Data quality depends on the input file.
- Chart selection and interpretation remain the responsibility of the user.
- The application is intended for analysis and reporting rather than replacing specialized BI platforms.

## Future Improvements

Potential future enhancements include:

- Additional chart types
- More advanced filtering
- Multiple-column grouping
- Additional export formats
- Dashboard-style layouts
- Improved styling and themes
- Automated summary insights
- More advanced data-cleaning options
- Drag-and-drop file loading

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

## Author

**Jatin Singh**

Built as a practical Python data-analysis and reporting project.

# Formula 1 Performance & Race Strategy Analysis

An Excel-based data analysis project exploring historical Formula 1 trends, driver performance, race outcomes, reliability, circuits, and pit-stop strategy.

The project uses **Power Query, Excel Data Model, DAX, PivotTables, and data visualization** to transform and analyze multi-table Formula 1 data spanning 1950–2026.

## Dashboard Preview

![Formula 1 Excel Dashboard](F1_Excel_Dashboard.png)

## Project Objective

The goal of this project is to explore Formula 1 performance and race strategy through historical race data and answer questions such as:

- How has Formula 1 changed in terms of races, drivers, and constructors over time?
- Which established drivers have achieved the highest race win rates?
- How strongly is starting grid position associated with finishing position?
- How have mechanical and technical race outcomes changed across F1 history?
- Which circuits have hosted the most Formula 1 races?
- How has median pit-stop duration changed over time?

## Dataset & Scope

The analysis uses a multi-table Formula 1 dataset containing historical information on races, drivers, constructors, circuits, race results, qualifying, lap times, pit stops, standings, sprint results, and race statuses.

- **Race coverage:** 1950–2026
- **Races:** 1,172 scheduled race records
- **Race result records:** 27,546
- **Drivers:** 865
- **Constructors:** 214
- **Circuits:** 78
- **Lap-time records:** 882,027
- **Pit-stop records:** 22,668

The 2026 season is still in progress, so analyses involving race counts or season-level trends treat 2026 as **year-to-date (YTD)** where applicable. Historical comparisons also account for differences in data availability across tables; for example, lap-time, qualifying, and pit-stop data do not cover the full history of Formula 1.

## Data Preparation & Modeling

The raw data was prepared and modeled in Excel using **Power Query** and the **Excel Data Model**.

Key preparation steps included:

- Imported and transformed multiple CSV tables using Power Query.
- Replaced dataset-specific `\N` placeholders with null values and assigned appropriate data types.
- Preserved missing values rather than treating missing numerical data as zero.
- Built relationships between race results and dimension tables such as races, drivers, constructors, circuits, and race status.
- Used separate fact tables for qualifying, pit stops, lap times, standings, and sprint results where required.
- Created calculated columns and DAX measures for metrics such as race results, race wins, win rate, positions gained, and median pit-stop duration.
- Categorized detailed race statuses into broader analytical groups including **Finished/Classified, Incident, Mechanical/Technical, Did Not Start/Qualify, and Other**.
- Distinguished completed races from future scheduled races so the ongoing 2026 season would not distort historical comparisons.

  ## Key Analysis & Findings

### 1. Formula 1 Calendar Growth
The number of races per season has increased substantially over Formula 1 history. Early championships typically contained far fewer races, while modern seasons regularly exceed 20 events. The lower 2026 count reflects the ongoing season rather than a decline in the calendar.

### 2. Driver Win Rate
Win rate was analyzed for drivers with at least 50 race-result records to reduce the influence of very small samples. Juan Manuel Fangio recorded the highest rate in this group, followed by drivers including Jim Clark, Michael Schumacher, Max Verstappen, Jackie Stewart, Lewis Hamilton, Ayrton Senna, and Alain Prost.

### 3. Starting Position vs Finishing Position
Average finishing position generally worsens as starting grid position moves further back. This demonstrates a strong descriptive association between qualifying/grid position and race outcome, although the analysis does not imply that starting position alone causes the final result.

### 4. Mechanical & Technical Outcomes
Mechanical/technical statuses accounted for a substantially larger share of race-result records in many earlier Formula 1 seasons than in recent decades. The long-term pattern suggests a considerable change in the frequency of recorded technical race outcomes across F1 history.

### 5. Most Frequently Used Circuits
Monza is the most frequently represented circuit among completed races in the dataset, followed by Monaco and Silverstone, highlighting the long-standing presence of several historic venues on the Formula 1 calendar.

### 6. Pit-Stop Duration
Median pit-stop duration declined from roughly 30–31 seconds in much of the 1990s and early 2000s to approximately 22–25 seconds in many recent seasons. Median rather than mean was used because unusually long pit stops substantially distorted annual averages.

## Tools & Skills Demonstrated

- **Microsoft Excel** — PivotTables, PivotCharts, dashboard development, exploratory analysis
- **Power Query** — multi-table import, data cleaning, null handling, data-type transformation
- **Excel Data Model** — relational modeling across multiple fact and dimension tables
- **DAX** — calculated columns and measures for performance and strategy metrics
- **Data Analysis** — trend analysis, descriptive statistics, outlier-aware metric selection, and validation
- **Data Visualization** — historical trends, rankings, performance relationships, and KPI-focused reporting


  ## Repository Contents

- `F1_Performance_Race_Strategy_Analysis.xlsx` — Complete Excel analysis, including Power Query transformations, Data Model, DAX measures, PivotTables, exploratory analysis, and final summary dashboard.
- `F1_Excel_Dashboard.png` — Preview of the final Excel dashboard.
- `README.md` — Project overview, methodology, analytical findings, and documentation.

    ## Data Source

The Formula 1 data used in this project was obtained from the Kaggle dataset **Formula 1 Race Data** by jtrotman.

The dataset contains historical Formula 1 data across multiple related tables, including races, results, drivers, constructors, circuits, qualifying, lap times, pit stops, standings, sprint results, and race statuses.

**Dataset:** [Formula 1 Race Data — Kaggle](https://www.kaggle.com/datasets/jtrotman/formula-1-race-data)

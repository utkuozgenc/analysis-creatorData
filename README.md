# Exams' Impact on My Sleep

## Description
This project aims to investigate the impact of exam dates on my sleep duration. The hypothesis is that exam dates lower my sleep duration. The project involves analyzing sleep data exported from Apple Health, covering the period from October 15, 2024, to November 17, 2024. The goal is to determine if sleep patterns change significantly around exam dates.

## Table of Contents
- [Motivation](#motivation)
- [Tools](#tools)
- [Data Source](#data-source)
- [Data Processing](#data-processing)
- [Data Visualizations](#data-visualizations)
- [Data Analysis](#data-analysis)
- [Findings](#findings)
- [Limitations](#limitations)
- [Future Work](#future-work)

## Motivation
My motivation for this project stems from curiosity about the potential negative effects of academic stress on sleep duration, particularly during exam periods. Understanding the relationship between exams and sleep can help assess the impact of stress on health and performance.

## Tools
- **Python**
- **pandas:** Data cleaning and manipulation
- **matplotlib:** Data visualization
- **seaborn:** Advanced data visualization
- **numpy:** Mathematical operations

## Data Source
The data was exported from Apple Health using the `export.xml` format. Sleep duration data is calculated by subtracting the start time from the end time for each recorded sleep session.

## Data Processing
The data was filtered to include the time period from October 15, 2024, to November 17, 2024. Sleep durations were calculated from the difference between start and end timestamps. Exam dates were included as a separate column for comparative analysis.

### Data Processing Steps
The data processing steps included in the code are as follows:

- **Loading Data:** The sleep data was imported from a preprocessed CSV file (`sleep_data_prepared.csv`).
- **Date Conversion:** The `date` column was converted to a `datetime` object for easier date filtering and visualization.
- **Date Filtering:** The data was filtered to only include sleep records between October 15, 2024, and November 17, 2024.
- **Exam Dates Identification:** A list of specific exam dates was created, and a new column `is_exam` was added to label each day as either an exam or non-exam day.
- **Rolling Averages:** A rolling average column (`rolling_avg`) was calculated with a 5-day window to smooth the sleep data trends.
- **Difference from Mean Calculation:** The difference between each sleep duration and the mean sleep duration was calculated and stored in the `difference_from_mean` column.

## Data Visualizations
The project involves multiple visualization techniques to test the hypothesis:
- Line plots showing daily sleep duration with exam dates highlighted
- Bar plots comparing average sleep duration on exam and non-exam days
- Boxplots comparing the distribution of sleep durations
- Histograms displaying the distribution of sleep durations with KDE overlays
- Rolling average sleep duration trends
- Violin plots comparing the distribution of sleep durations on exam vs non-exam days
- Sleep duration difference from the mean visualized to observe deviations

## Data Analysis
The data analysis involves:
- Examining sleep trends leading up to and following exam dates
- Comparing sleep durations on exam and non-exam days
- Visualizing deviations from average sleep duration

## Findings
Preliminary results suggest a noticeable reduction in sleep durations on exam dates compared to non-exam days. Further statistical testing will be conducted to verify these observations.

## Limitations
- The dataset is limited to a short time period.
- External factors affecting sleep (e.g., health, personal habits) are not accounted for.
- Data is self-reported and may lack accuracy.

## Future Work
- Expanding the dataset to cover a more extended period
- Conducting statistical significance tests to confirm findings
- Exploring additional health metrics such as heart rate and activity levels for a more comprehensive analysis

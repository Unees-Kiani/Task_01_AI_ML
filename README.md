# Task 01: Python Programming, Data Analysis & Visualization

**Devixo Solutions: AI/ML Internship Program**

**Author:** Unees Ur Rehman Kiani
**GitHub:** [Unees-Kiani](https://github.com/Unees-Kiani)

---

## Project Objective

To perform a complete data analysis workflow on a real-world dataset: loading and understanding the data, cleaning and preprocessing it, performing exploratory and statistical analysis, creating visualizations, and extracting meaningful insights.

## Dataset Description

- **Name:** Hotel Booking Demand
- **Source:** Kaggle ("Hotel Booking Demand" dataset, originally published by Antonio, Almeida & Nunes, 2019)
- **Content:** Booking records for a City Hotel and a Resort Hotel, including lead time, arrival date, length of stay, number of guests, market segment, customer type, daily rate, special requests, and cancellation status.
- **Raw size:** 119,390 rows x 32 columns
- **Cleaned size:** 87,303 rows x 33 columns (after removing duplicates and invalid records, and adding `total_guests` and `total_nights`)

## Technologies Used

- Python 3
- Google Colab (Jupyter Notebook environment)

## Libraries Used

- Pandas: data loading, cleaning, analysis
- NumPy: numerical operations
- Matplotlib: visualizations
- Seaborn: statistical visualizations

## Project Workflow

1. Dataset selection
2. Data loading
3. Data understanding (head, tail, sample, info, shape, column types)
4. Data cleaning
   - Dropped the `company` column (about 94% missing)
   - Filled `agent` with 0 (missing means no agent), `children` with the median, `country` with the mode
   - Removed duplicate records
   - Converted `reservation_status_date` to datetime
   - Renamed unclear columns (e.g. `adr` to `average_daily_rate`)
   - Removed bookings with zero guests or negative price
5. Exploratory data analysis
6. Statistical analysis (mean, median, mode, min, max, range, standard deviation, variance, correlation)
7. Data visualization (10 charts)
8. Insights and conclusion

## Visualizations Created

Histogram, bar chart, pie chart, scatter plot, line chart, box plot, correlation heatmap, count plot, pair plot, violin plot. All images are in the `images/` folder.

## Major Findings

1. After cleaning, the dataset has 87,303 bookings with no missing values or duplicates.
2. About 27% of bookings were canceled.
3. Lead time is right-skewed: mean about 80 days, median 49 days.
4. Most bookings are made within two weeks of arrival.
5. August is the busiest month and January the quietest.
6. Average daily rate peaks in August (about 151) and is lowest in winter months.
7. Transient customers make up 82.4% of bookings.
8. Online TA has the highest cancellation rate among large market segments (35.4%), versus about 12% for Corporate bookings.
9. Lead time has the strongest positive correlation with cancellation (+0.18); required parking spaces has the strongest negative (-0.18).
10. Total guests and average daily rate are positively correlated (+0.38).
11. The daily rate has extreme outliers (maximum 5,400).
12. The "Undefined" market segment shows 100% cancellation but has very few records, so it is not reliable.

## Project Structure

    Task_01_AI_ML/
    ├── dataset/
    │   ├── hotel_bookings.csv
    │   └── cleaned_hotel_bookings.csv
    ├── notebook/
    │   └── Task_01_Data_Analysis.ipynb
    ├── images/
    │   └── visualization_01.png ... visualization_10.png
    ├── report/
    │   └── Task_01_Report.pdf
    └── README.md

## How to Run the Project

1. Clone or download this repository.
2. Open `notebook/Task_01_Data_Analysis.ipynb` in Google Colab or Jupyter Notebook.
3. Upload `dataset/hotel_bookings.csv` to the notebook's working directory.
4. Install the libraries if needed: `pip install pandas numpy matplotlib seaborn`
5. Run all cells from top to bottom.

## Author

**Unees Ur Rehman Kiani**
AI/ML Internship, Devixo Solutions

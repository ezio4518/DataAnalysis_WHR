# Data Analysis Project: World Happiness Report

This project analyzes the World Happiness Report data from 2015 to 2019. The analysis focuses on exploring the relationships between various factors such as GDP per capita, social support, life expectancy, and happiness scores for different countries. The project uses Python libraries like `pandas`, `plotly`, `numpy`, and `scikit-learn` for data manipulation, visualization, and modeling.

## Project Workflow

### 1. **Setup and Dependencies**

- The required Python libraries are installed using `pip install` commands:
  ```python
  pip install pandas plotly numpy scikit-learn nbformat statsmodels
  ```

### 2. **Data Import**

- The datasets for the years 2015 to 2019 are loaded from CSV files located in the `data/` directory:
  ```python
  df_2015 = pd.read_csv("data/2015.csv")
  df_2016 = pd.read_csv("data/2016.csv")
  df_2017 = pd.read_csv("data/2017.csv")
  df_2018 = pd.read_csv("data/2018.csv")
  df_2019 = pd.read_csv("data/2019.csv")
  ```

### 3. **Data Preprocessing**

- **Standardizing Country Names**: All country names are converted to lowercase for consistency.
- **Handling Missing Data**: Missing values in the 2018 dataset are dropped.
- **Filtering Countries**: Countries not present in all years are identified and removed from the datasets.
- **Rearranging Columns**: Columns are renamed and reordered for uniformity across all datasets.

### 4. **Exploratory Data Analysis (EDA)**

- **Visualizing Happiness Scores**: Scatter plots are created to visualize happiness scores for each year.
- **Choropleth Map**: A choropleth map is generated to show the happiness scores by country over time.
- **Correlation Analysis**: Correlation matrices are computed and visualized to explore relationships between variables like GDP per capita, social support, and happiness scores.

### 5. **Outlier Detection**

- Z-scores are calculated for GDP per capita to identify outliers. Countries with Z-scores beyond a threshold are visualized in scatter plots.

### 6. **Regression Analysis**

- Linear regression models are built to analyze the relationship between GDP per capita and happiness scores for each year. Metrics like Mean Squared Error (MSE) and R-squared are calculated to evaluate the models.

### 7. **Visualization**

- Various visualizations are created using `plotly`:
  - Scatter plots for happiness scores and GDP per capita.
  - Heatmaps for correlation matrices.
  - Choropleth maps for happiness scores by country.
  - Outlier visualizations using Z-scores.

## Key Functions and Code Highlights

### `getConvoMatrix(df)`

- Computes the correlation matrix for a given dataset.

### `zscore(df)`

- Calculates Z-scores for a given column to identify outliers.

### Regression Analysis

- Uses `scikit-learn` to perform linear regression and evaluate the relationship between GDP per capita and happiness scores.

### Visualization

- `plotly` is used extensively for creating interactive visualizations, including scatter plots, heatmaps, and choropleth maps.

## Outputs

- Interactive visualizations for happiness scores, GDP per capita, and correlations.
- Insights into the relationship between GDP per capita and happiness scores.
- Identification of outliers and their impact on the analysis.

This project provides a comprehensive analysis of the World Happiness Report data, offering insights into the factors influencing happiness across countries over time.

---

## Graphical Analysis

Some of the images of the graphical analysis here to showcase the visualizations generated during the project:

![Happiness Score by Country](https://i.ibb.co/MkR1Cpcx/Screenshot-2025-04-17-210105.png)

![Happiness Score by Country Globe](https://i.ibb.co/xqdHpGvc/Screenshot-2025-04-17-210147.png)

![GDPPC by Country](https://i.ibb.co/ksTBm4kq/Screenshot-2025-04-17-210335.png)

![GDPPC vs Happiness Score](https://i.ibb.co/cKdfMK76/Screenshot-2025-04-17-210310.png)

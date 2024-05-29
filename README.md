# Kaggle World Happiness

Exploration and modeling of World Happiness dataset from Kaggle. 

![](https://storage.googleapis.com/kaggle-datasets-images/894/1634/927f32f2cc2cc40d208ae384562ad743/dataset-cover.jpg)

## Introduction

> The World Happiness Report is a landmark survey of the state of global happiness. The first report was published in 2012, the second in 2013, the third in 2015, and the fourth in the 2016 Update. The World Happiness 2017, which ranks 155 countries by their happiness levels, was released at the United Nations at an event celebrating International Day of Happiness on March 20th. 

> The report continues to gain global recognition as governments, organizations and civil society increasingly use happiness indicators to inform their policy-making decisions. Leading experts across fields – economics, psychology, survey analysis, national statistics, health, public policy and more – describe how measurements of well-being can be used effectively to assess the progress of nations. 

> The reports review the state of happiness in the world today and show how the new science of happiness explains personal and national variations in happiness. 

<a href="https://www.kaggle.com/unsdsn/world-happiness">Read more.</a>

## Installation

To set up the project, follow these steps:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/djeada/Kaggle-World-Happiness.git
    ```
2. **Install `virtualenv`**:
    If `virtualenv` is not already installed, you can install it using:
    ```bash
    pip install virtualenv
    ```
3. **Set Up the Virtual Environment**:
    Open the terminal in the project directory and run the following commands to create and activate a virtual environment:
    ```bash
    cd Kaggle-World-Happiness
    virtualenv env
    source env/bin/activate
    ```
4. **Install Dependencies**:
    Install the required packages using the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```
5. **Launch Jupyter Notebook**:
    Start the Jupyter Notebook server:
    ```bash
    jupyter notebook
    ```
6. **Open Data Exploration Notebook**:
    Navigate to the `src/dataexploration` directory within Jupyter Notebook to begin exploring the data.

## Dataset Description

This dataset contains information about the happiness levels of different countries, measured by various factors. Each row represents a country, and the columns include data on the country's region, happiness rank, happiness score, and several other metrics that contribute to the overall happiness score. Below is a detailed description of each column:

- **Country**: The name of the country.
- **Region**: The region where the country is located.
- **Happiness Rank**: The rank of the country based on its happiness score, with 1 being the happiest.
- **Happiness Score**: A numerical value representing the country's happiness level.
- **Standard Error**: The standard error of the happiness score.
- **Economy (GDP per Capita)**: The contribution of the country's economic status (measured by GDP per capita) to its happiness score.
- **Family**: The contribution of social support and family relationships to the country's happiness score.
- **Health (Life Expectancy)**: The contribution of health and life expectancy to the country's happiness score.
- **Freedom**: The contribution of the freedom to make life choices to the country's happiness score.
- **Trust (Government Corruption)**: The contribution of the perception of government corruption to the country's happiness score.
- **Generosity**: The contribution of generosity and donations to the country's happiness score.
- **Dystopia Residual**: A residual value representing unexplained variations in the happiness score.

### Sample Data

Here are the first three entries in the dataset:

| Country      | Region         | Happiness Rank | Happiness Score | Standard Error | Economy (GDP per Capita) | Family  | Health (Life Expectancy) | Freedom | Trust (Government Corruption) | Generosity | Dystopia Residual |
|--------------|----------------|----------------|-----------------|----------------|--------------------------|---------|--------------------------|---------|------------------------------|------------|-------------------|
| Switzerland  | Western Europe | 1              | 7.587           | 0.03411        | 1.39651                  | 1.34951 | 0.94143                  | 0.66557 | 0.41978                      | 0.29678    | 2.51738           |
| Iceland      | Western Europe | 2              | 7.561           | 0.04884        | 1.30232                  | 1.40223 | 0.94784                  | 0.62877 | 0.14145                      | 0.43630    | 2.70201           |
| Denmark      | Western Europe | 3              | 7.527           | 0.03328        | 1.32548                  | 1.36058 | 0.87464                  | 0.64938 | 0.48357                      | 0.34139    | 2.49204           |

## Potential Analyses

This dataset provides rich information for various types of analysis related to the happiness levels of countries. Below is a table summarizing the types of analyses that can be performed and those that are not suitable for this dataset:

| **Type of Analysis**                    | **Description**                                                                                  | **Suitability** |
|-----------------------------------------|--------------------------------------------------------------------------------------------------|-----------------|
| **Descriptive Analysis**                | Summary statistics, distribution analysis                                                        | Suitable        |
| **Comparative Analysis**                | Regional comparisons, top/bottom analysis                                                        | Suitable        |
| **Correlation Analysis**                | Correlation matrix, scatter plots                                                                | Suitable        |
| **Regression Analysis**                 | Linear regression, multiple regression                                                           | Suitable        |
| **Cluster Analysis**                    | Clustering countries with similar profiles                                                       | Suitable        |
| **Time Series Analysis**                | Trend analysis over different time periods                                                       | Not Suitable    |
| **Temporal Analysis**                   | Analysis requiring data over different time periods (e.g., trend analysis, forecasting)          | Not Suitable    |
| **Causal Analysis**                     | Determining causation rather than correlation                                                    | Not Suitable    |
| **Individual-Level Analysis**           | Micro-level insights (e.g., personal happiness determinants)                                     | Not Suitable    |
| **In-depth Policy Impact Analysis**     | Detailed evaluation of specific policies                                                         | Not Suitable    |

This table provides an overview of the potential analyses that can be performed on the dataset, highlighting the suitability of different types of analysis.

## Results

I. Bar Chart Analysis of Happiness Scores

![Screenshot from 2024-05-29 22-44-02](https://github.com/djeada/Kaggle-World-Happiness/assets/37275728/0880a429-301f-4df6-8ffd-cc3fe2dfe2a5)

The bar chart illustrates the happiness scores for the top 5 and worst 5 countries in 2019. Here's a general analysis:

- Top 5 Happiest Countries:
  - **Finland**
  - **Denmark**
  - **Norway**
  - **Iceland**
  - **Netherlands**

- Worst 5 Unhappiest Countries:
  - **Rwanda**
  - **Tanzania**
  - **Afghanistan**
  - **Central African Republic**
  - **South Sudan**

II. Heatmap Analysis

![Screenshot from 2024-05-29 22-41-16](https://github.com/djeada/Kaggle-World-Happiness/assets/37275728/004556d6-10fa-456e-a6a6-eae819aac93f)

The heatmap illustrates the correlation matrix between various factors influencing happiness scores across different countries. Here's a general analysis of the key findings:

- **Happiness Score**: Strongly positively correlated with:
  - **GDP per Capita**: Indicates that higher economic performance is associated with higher happiness.
  - **Family**: Suggests that strong social support and family relationships contribute significantly to happiness.
  - **Life Expectancy**: Shows that better health and longer life expectancy are linked to higher happiness.
  - **Freedom**: Indicates that the freedom to make life choices is important for happiness.
  - **Lack of Corruption**: Suggests that lower perceived corruption is associated with higher happiness.
  - **Generosity**: Weaker correlation, but still positively related to happiness.

- **GDP per Capita**: Positively correlated with:
  - **Life Expectancy**: Wealthier countries tend to have better healthcare and higher life expectancy.
  - **Family**: Suggests better social support systems in wealthier nations.
  - **Freedom**: Economic freedom might coincide with personal freedom.
  - **Lack of Corruption**: Wealthier countries tend to have lower levels of corruption.

- **Family**: Correlated with:
  - **Life Expectancy**: Better family support might lead to better health outcomes.
  - **Freedom**: Social support enhances perceived freedom.
  - **Lack of Corruption**: Better social structures might coincide with lower corruption.

- **Life Expectancy**: Positively correlated with:
  - **Freedom**: Healthier societies might enjoy greater freedoms.
  - **Lack of Corruption**: Better health systems might exist in less corrupt environments.

- **Freedom**: Moderately correlated with:
  - **Lack of Corruption**: Freer societies tend to have lower levels of corruption.
  - **Generosity**: Freedom might encourage generosity.

- **Lack of Corruption**: Strong correlations with several factors and moderate correlation with:
  - **Generosity**: Less corrupt societies might also be more generous.

- **Generosity**: Shows moderate positive correlations with freedom and lack of corruption, indicating some level of interdependence.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

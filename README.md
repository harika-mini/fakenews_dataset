# Fake News Dataset 📊

Welcome to the Fake News Dataset repository! This dataset includes two separate collections of labeled news articles, categorized as fake and true, to aid in the development of machine learning models for fake news detection. The dataset is intended for educational and research purposes only.

## 📄 Dataset Overview

The dataset contains two files:

- **Fake.csv**: Contains news articles labeled as fake.
- **True.csv**: Contains news articles labeled as true.

Each file includes various attributes for each article, such as title, content, and publication date, to help develop and train accurate models for distinguishing between real and fake news articles.

## 🗂️ Data Format

Each record in both datasets (Fake.csv and True.csv) includes the following fields:

- **Title**: The headline of the news article.
- **Text**: The full content of the news article.
- **Subject**: The subject category of the article.
- **Date**: The publication date of the article.

### Example Structure

| Title                     | Text                          | Subject   | Date       |
|---------------------------|-------------------------------|-----------|------------|
| "Fake News Headline"     | "Content of the fake article."| "Politics"| 2024-10-01 |
| "True News Headline"     | "Content of the true article."| "Health"  | 2024-10-02 |

## 📊 Dataset Details

### File 1: Fake.csv
- **Total Articles**: Approximately 23,503.
- **Subjects**: Politics, World, Economy, etc.

### File 2: True.csv
- **Total Articles**: Approximately 21,418.
- **Subjects**: Politics, Health, Technology, etc.

## 🛠️ Usage

### Step 1: Download
Clone this repository or download the dataset files directly.

### Step 2: Load the Datasets
Use Pandas or another library to load the datasets and prepare them for analysis:

```python
import pandas as pd

# Load the fake and true datasets
fake_df = pd.read_csv('Fake.csv')
true_df = pd.read_csv('True.csv')

# Preview the data
print(fake_df.head())
print(true_df.head())
```
### Step 3: Combine and Label (Optional)
For training, you may want to combine both datasets and add a label column to indicate fake or true news:

```python
# Add label columns
fake_df['label'] = 0  # Fake news
true_df['label'] = 1  # True news

# Combine datasets
combined_df = pd.concat([fake_df, true_df], ignore_index=True)
```

## ⚠️ License and Usage Policy
This dataset is intended for educational and research purposes only. Any commercial use is prohibited.

## 🤝 Contributing
Contributions to improve this dataset are welcome! If you have additional data, improvements, or suggestions, feel free to submit a pull request or reach out to discuss.

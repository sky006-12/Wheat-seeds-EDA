# Wheat Seeds Analysis (Basic EDA Project)

A beginner-friendly exploratory data analysis project for **B.Tech 1st Year** learners.
It explores the physical measurements of wheat kernels using Python, NumPy, Pandas and Matplotlib.

## Problem statement
Wheat comes in different varieties, and kernel size and shape can help tell them apart. This project studies the measurements of three varieties (Kama, Rosa and Canadian) to see how they differ from each other.

## Questions answered
1. How many samples belong to each variety?
2. What are the mean, median, minimum and maximum of kernel area, perimeter and length?
3. Which variety has the highest average area and width?
4. Which are the top 10 kernels by area?
5. Are there any missing values or duplicates?
6. How do the average measurements compare across the three varieties?

## Dataset
`data/seeds.csv` - 199 rows, 8 columns (Area, Perimeter, Compactness, Kernel.Length, Kernel.Width, Asymmetry.Coeff, Kernel.Groove, Type).
The data is real, taken from the Wheat Seeds dataset on Kaggle ([jmcaro/wheat-seedsuci](https://www.kaggle.com/datasets/jmcaro/wheat-seedsuci)), which is based on the UCI Seeds dataset.
The assignment mentioned 210 rows, but the file used here has 199. The `Type` column holds 1, 2 and 3, which are treated as Kama, Rosa and Canadian (the usual order for this dataset).

## Project structure
```
wheat-seeds-eda/
├── data/seeds.csv
├── Source Code/wheat_seeds_eda.ipynb
├── images/                  (2 graphs related to this project)
├── docs/SRS.pdf             
├── requirements.txt
├── .gitignore
└── README.md
```

## How to run
```bash
git clone https://github.com/<your-username>/wheat-seeds-eda.git
cd wheat-seeds-eda
pip install -r requirements.txt
jupyter notebook notebooks/wheat_seeds_eda.ipynb
```
To use Google Colab instead, upload the notebook, click **Runtime > Run all** and choose `data/seeds.csv` when the first cell asks for a file.

## Steps followed
1. Load the data and rename the columns  2. Inspect it with head(), tail(), shape, info() and describe()  3. Answer the six questions with NumPy and Pandas (value_counts, groupby, sort_values, filtering)  4. Make two charts  5. Write observations

## Key findings (from this dataset)
- 199 samples: Rosa 68, Kama 66, Canadian 65, so the varieties are almost balanced.
- Average kernel area is about 14.9 (range 10.59 to 21.18).
- Rosa has the largest kernels (average area 18.37, width 3.68). Canadian has the smallest (average area 11.88).
- All of the top 10 kernels by area are Rosa.
- There are no missing values and no duplicate rows.
- Area and perimeter are almost perfectly correlated (about 0.99), as bigger kernels have a longer boundary.

## Charts
![Variety count](images/variety_count.png)
![Area histogram](images/area_histogram.png)

## Tools
Python 3 · NumPy · Pandas · Matplotlib · Jupyter Notebook / Google Colab · Git and GitHub

## Author
Your Name - B.Tech 1st Year (replace with your details)

# Education Project

> We are interested in whether there is a relationship between the ACT score and socioeconomic variables

---

## Project Overview


- **Objective:** There are many variables that can impact educational inequalities. We are using ACT/ SAT scores as a proxy for achievement in school, since it is a standardized test that many high school students take during the process of applying to college. We are examining different factors that might contribute to lower scores on the ACT (or SAT)
- **Domain:** Education
- **Key Techniques:** Correlation Matrix,  Imputation, Linear Regression

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** 

- https://nces.ed.gov/ccd/elsi/tableGenerator.aspx
- https://www.dropbox.com/s/lkl5nvcdmwyoban/ccd_sch_029_1617_w_1a_11212017.csv?dl=1 

- **Description:** This project utilizes three data sets EdGap_data.xlsx and ccd_sch_029_1617_w_1a_11212017.csv. The primary data set is the EdGap data set from EdGap.org. This data set from 2016 includes information about average ACT or SAT scores for schools and several socioeconomic characteristics of the school district. The secondary data set is basic information about each school from the National Center for Education Statistics. The third data set is from the National Center for Education Statistics and provides information about the student to teacher ratio.

- **License:** 

---

## Analysis

There is only one notebook. Each cell should be run in the order presented. After data cleaning steps the notebook will output a cleaned csv to the data folder which can be used separately for other analysis. However, all of my analysis is in this notebook and continues directly after the data cleaning steps.

---

## Results

Statistically, the most significant contributor to SAT scores is the access to free and reduced lunch. 

Single linear regression models revealed that most of the factors were relatively weak on their own. This was followed up with a multilinear model composed of all the factors. From this we were able to eliminate percent married, median income, and student-teacher ratio. Then we built a reduced model with only unemployment, percent college and percent free lunch which was able to strongly predict SAT scores. However, the factors are all on different scales, so the final step of analysis was to standardize all factors so that one unit change was equivalent. This then revealed that free lunch alone was the strongest predictor.

---

## Authors

- Ahrial Young - [@ayoung42](https://github.com/ayoung42)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- seaborns, sklearn, statsmodels, plotly
-I followed data cleaning and exploration tutorials provided by Dr. Brian Fischer for his DATA 5100 FQ 2025 class. [https://github.com/brian-fischer]

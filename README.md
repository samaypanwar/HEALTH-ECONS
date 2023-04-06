# Health Economics

Under Group Project dir,

each year is our cleaned data filtered with:
1. "Blue"
2. "Individual Premium Age 21"

This data is then combined in main data file

To add:
1. Covid cases by county
2. republican/democrat data for each state and house information in each state

Need to change:
1. Remove covid dummy and add year dummy

Questions to answer:
1. What is effect of the progress of covid on premiums by state
2. What was the effect of the level of covid cases by county on premiums
3. what was the effect of the ruling party on increase in premiums

#### Regressors

1. Medical 
    1. Max OOP
    2. Deductible
    3. Metal Name (Type of Plan) 
   
   [link to dataset](https://www.cms.gov/cciio/resources/data-resources/qhp-choice-premiums)
---
2. Geographical
   1. State?
   2. County indicator variable
   3. Time trend yearly dummy

---
3. Covid
   1. Number of covid cases in _year_ for State/county
   2. Number of covid deaths in _year
   3. Citation: Centers for Disease Control and Prevention, COVID-19 Response. Weekly United States COVID-19 Cases and Deaths by State (version date: [Month] [Date], [Year]).
   
   [link to dataset](https://data.cdc.gov/Case-Surveillance/Weekly-United-States-COVID-19-Cases-and-Deaths-by-/pwn4-m3yp)
   
   [link to cdc covid tracker](https://covid.cdc.gov/covid-data-tracker/#cases_totalcases)
   **Do we want to include both of these --> High multicollinearity**

---
4. Political
   1. Ruling party by state for year * year
   2. Unanimous house for state by year * year

## Things to Do

   1. Merge both the dataframes of covid based on year
   2. Conduct normality test on covid, premiums
   3. Box plots to see yearwise effect on premiums dist
   4. Create dummies for state
   5. Create final regression dataframe
   6. Test for VIF
   7. HCO OLS and plot parameters for state dummies / covid cases
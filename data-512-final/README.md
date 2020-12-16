# DATA512 Final Project 

* __University of Washington__
* __DATA512 Fall 2020__
* __Sihao Miao__
* __November 5, 2020__


## Abstract
The purpose of this project is to analyze H-1B Employer Data providing information on employers petitioning for H-1B workers from fiscal year 2015 to 2019. I'm interested in seeing the approval and denial data extracted from Form I-129 submitted to USCIS, and in particular, I would like to know the approval and denial rates by employer in the last 5 years. I found that in general, the number of all decisions increased in the fiscal years 2015 to 2019 while the approval rate decreased. I also found that the H-1B approval rate is correlated with state, industry and fiscal year. From a human-centered perspective, the goal of this analysis is to understand both the trend of approval and denial rates over years as well as possible factors affecting such decison in the immigration system. I conducted this analysis in a reproducible way such that other temporary foreign workers might find it useful and apply it into their own analysis. 

## Data
For this analysis, I used H-1B Employer Data from U.S. Citizenship and Immigration Services (USCIS) because the dataset including data from fiscal year 2009 through fiscal year 2020 (quarter 2) is publicly available. The main page of H-1B Employer Data Hub can be found [here](https://www.uscis.gov/tools/reports-and-studies/h-1b-employer-data-hub) and we can download all data files through this [link](https://www.uscis.gov/tools/reports-and-studies/h-1b-employer-data-hub/h-1b-employer-data-hub-files). The dataset consists of the counts of initial approval, initial denial, continuing approval, and continuing denial are aggregated by distinct completion fiscal year, two digit NAICS code, tax ID, state, city, and ZIP code. As stated on [this page](https://www.uscis.gov/tools/reports-and-studies/h-1b-employer-data-hub/h-1b-employer-data-hub-files), the dataset provide by USCIS can be used for personal and non-commercial use. We are allowed to download data for individual fiscal years and conduct our own analyses of these data. More information about terms of use for the data can be found [here](https://www.uscis.gov/tools/reports-and-studies/understanding-our-data).

## Conclusion
* In general, the number of all decisions increased in the fiscal years 2015 to 2019 while the approval rate decreased.    
* The H-1B approval rate is correlated with state, industry and fiscal year.   
   
![](https://github.com/mshhh/data-512/blob/main/data-512-final/plots/approval_denial_trend.png).   
![](https://github.com/mshhh/data-512/blob/main/data-512-final/plots/approval_rate_trend.png)

## Directory Structure 
This directory contains 1 Jupyter Notebook named a7-final-project-report.jpynb displaying the whole analysis, 1 Jupyter Notebook named a5-final-project-proposal.jpynb displaying the initial proposal, 1 folder named [data](https://github.com/mshhh/data-512/tree/main/data-512-final/data) including all source data, 1 folder named [plots](https://github.com/mshhh/data-512/tree/main/data-512-final/plots) containing all images of data visualization, 1 README file, and 1 LICENSE file. The directory structure is shown as following. 
    
```
data-512-a2
│   a7-final-project-report.jpynb 
|   a5-final-project-proposal.jpynb
│   README.md
│   LICENSE
└───data
│   │   h1b_datahubexport-2015.csv
│   │   h1b_datahubexport-2016.csv
│   │   h1b_datahubexport-2017.csv
│   │   h1b_datahubexport-2018.csv
│   │   h1b_datahubexport-2019.csv  
└───image
│   │   approval_denial_trend.png
│   │   approval_rate_trend.png
```

## License
This project is available under the [MIT License](https://github.com/mshhh/data-512/blob/main/data-512-final/LICENSE)

## Note
The Jupyter notebook uses Python version 3.7.4.

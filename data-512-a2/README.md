# A2: Bias in Data
Author: Sihao Miao.  
Date Created: Oct 21, 2020

## Goal
The goal of this project is to identify potential sources of bias in two datasets, "Wikipedia Talk Labels: Toxicity” and "Wikipedia Talk Labels: Personal Attacks", from the Wikipedia Talk corpus, and to perform an exploratory data analysis based on those data. The analysis is done in a Jupyter Notebook including a description about some implications of the bias and some suggestions on correcting those bias and reducing negative consequences. 

## License & Data Use
This project is available under the [MIT License](https://github.com/mshhh/data-512/blob/main/data-512-a1/LICENSE).

The two datasets can be accessed through [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731) and the schema and descriptions can be found [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release): 

1. [Toxicity Figshare dataset](https://figshare.com/articles/Wikipedia_Talk_Labels_Toxicity/4563973): over 100k labeled discussion comments from English Wikipedia by multiple annotators via Crowdflower on whether it is a toxic or healthy contribution with some demographic data for each crowd-worker.
2. [Personal Attacks Figshare dataset](https://figshare.com/articles/Wikipedia_Talk_Labels_Personal_Attacks/4054689): over 100k labeled discussion comments from English Wikipedia by multiple annotators via Crowdflower on whether it contains a personal attack with some demographic data for each crowd-worker. 

For your information, you can learn more details about the project on [Detox wiki page](https://meta.wikimedia.org/wiki/Research:Detox) and [perspective API repository on GitHub](https://github.com/conversationai/perspectiveapi/wiki/perspective-hacks).

## Directory Structure 
This directory contains 1 Jupyter notebook named hcds-a2-data-bias.jpynb displaying the whole analysis, 1 file named data including all source data, 1 file named image containing all images of data visualization, 1 README file, and 1 LICENSE file. The directory structure is shown as following. 
    
```
data-512-a2
│   hcds-a2-data-bias.jpynb   
└───data
│   │   toxicity_annotated_comments.tsv
│   │   toxicity_annotations.tsv
│   │   toxicity_worker_demographics.tsv
│   │   attack_annotated_comments.tsv
│   │   attack_annotations.tsv
│   │   attack_worker_demographics.tsv   
└───image
│   │   file.png
│   │   file.png
└───README.md
└───LICENSE
```
      

## Data Visualization
![]()

## Note
The notebook uses Python version 3.7.4.


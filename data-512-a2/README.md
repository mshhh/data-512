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
This directory contains 1 Jupyter Notebook named hcds-a2-data-bias.jpynb displaying the whole analysis, 1 folder named [data](https://github.com/mshhh/data-512/tree/main/data-512-a2/data) including all source data, 1 folder named [image](https://github.com/mshhh/data-512/tree/main/data-512-a2/image) containing all images of data visualization, 1 README file, and 1 LICENSE file. The directory structure is shown as following. 
    
```
data-512-a2
│   hcds-a2-data-bias.jpynb  
│   README.md
│   LICENSE
└───data
│   │   toxicity_annotated_comments.tsv
│   │   toxicity_annotations.tsv
│   │   toxicity_worker_demographics.tsv
│   │   attack_annotated_comments.tsv
│   │   attack_annotations.tsv
│   │   attack_worker_demographics.tsv   
└───image
│   │   analysis1_fig1.png
│   │   analysis1_fig2.png
│   │   analysis1_fig3.png
│   │   analysis1_fig4.png
│   │   analysis2_fig.png
```
      
## Exploratory Analysis Research Questions 

Analysis 1: Analyzing the demographic information about the Crowdflower workers that is available in the dataset. 

For the first analysis, I only focused on one dataset (toxicity) and the the research questions I came up with are: 

1. What are gender, age group, first language, and education level distributions among crowworkers in the toxicity dataset? 
2. Does the demographic profile of the crowworkers match that of the general population?

Analysis 2: Analyzing relationships between worker demographics and labeling behavior.

Beside the demographic profile information of the crowworkers, I was also interested in analyzing if the unequal distribution of crowworkers would lead to bias in labeling behaviors. In particular, I paid more attention to the following research questions:

1. How consistent are labelling behaviors among crowworkers with different ages?
2. Does there exist a difference between age groups when labeling comments as toxicity vs. personal attacks?

The Jupyter Notebook conducting the whole exploratory analysis can be found [here]().

## Results

Analysis 1:
    
1. Based on the graphs above, I found that 1. 66.0% of the crowworkers are male, 2. 52.6% (majority) of the crowworkers are 18-30 years old, 3. 82.6% of the crowworkers do not have English as their first language, and 4. 40.1% of the crowworkers have bachelor’s degrees, 28.3% are in high school. Therefore, we can see that the numbers of crowworkers for gender, age group, first language, and education level are disproportionate.    
2. The distributions of crowworkers by gender, age group, first language, and education level do not represent the general population fairly. Therefore, the unequal distributions of crowworkers are likely to introduce some bias gender, age group, first language, and education level in the labelling process. For example, 82.6% of crowworks who are not English native speakers might understand the comments differently from the native speakers. As a result, when they label the comments, the misunderstanding can cause bias in this process and further would affect the training process for machine learning models.

The figures created in this analysis were named as analysis1_fig1.png, analysis1_fig2.png, analysis1_fig3.png, and analysis1_fig4.png which can be found in the [image](https://github.com/mshhh/data-512/tree/main/data-512-a2/image) folder.

Analysis 2:

1. Based on the graph above, I found that crowworkers with different age groups labeled the comment inconsistently. For example, crowwokers in the age group of over 60 are more likely to label comments as toxicity and attack than croworkerss in other age groups. On the contrary, crowworkers of age under 18 own the lowest average indicator value which represents whether the worker thought the comment contains any form of personal attack (or the comment is toxic in the toxicity dataset). As far as I'm concerned, older age groups might be more sensitive to toxic and attack comments compared to younger crowworker, which can produce bias in this process.
2. Since I joined the two datasets on rev_id and filtered the rows with the same age_group in the two datasets, I noticed that for the same comment, crowworkers under age 45 tend to label it as toxicty than as any forms of personal attack, and vice versa for crowworkers of age above 45. This difference would also introduce bias in the labeling process and this might be caused by different understanding of toxicity and personal attack between age groups. 

The figure created in this analysis was named as analysis2_fig.png which can be found in the [image](https://github.com/mshhh/data-512/tree/main/data-512-a2/image) folder.

## Note
The Jupyter notebook uses Python version 3.7.4.


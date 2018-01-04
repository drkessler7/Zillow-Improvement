## Zillow Zestimate® Improvement

### Overview
Imagine being able to determine the value of your home without outside help, and in only a few clicks. That's what Zestimate® does: it provides users with an independent, unbiased starting point for determining a home’s worth based on data from over 100 million other homes on and off the market. Through Kaggle— the world's largest platform for predictive analytics competitions— Zillow challenged the global data science community to improve the accuracy of the tool. I joined the contest as a solo participant, motivated by using data science/digital engineering to solve a real world problem.

### Problem
The earliest Zestimates from 2006 had error rates of roughly 14%, were calculated monthly, and for only about half of the homes in the country. Today, the error rates are down to about 5%, are calculated continually and for all homes nationwide. Zillow wants to continue to close the gap in the margin of error, thereby enhancing the accuracy of the client-facing Zestimate tool.

### Process
As this contest is still underway, I won't tell exactly which predictive models I used to make my submission. But I will share some of the basic initial steps that I took in tackling this challenge. As with any data science project, it was important to take a look at the data and learn some simple things from it. The rules of the competition state that all participants must use only the data provided by Zillow for the competition.

Zillow provided six different files that contain data, and other information to describe it. I carefully investigated all six files to see what was inside. I discovered that four of the files contained Comma Separated Values (.csv file type), which can be viewed as large Excel spreadsheets. These had data for each of the 3 million Los Angeles homes examined in this contest. Two spreadsheets contained different characteristics of each home. These included the square footage of each home, how many bathrooms and bedrooms each of them had, and 55 other interesting traits.

However, I could see that not all homes had every piece of information. The number of pools was not listed for many homes. Very few homes had values that told their architectural type. So I had to decide how to handle these missing values. I could have used math to make an estimation of what each missing value may have been, or I could have just left those values blank. 

Some values needed be cleaned up a little bit so they could be used properly. For instance, each property’s county land use code (think zoning purposes) contained both numbers and letters. When using data in calculations or to make predictions, there cannot be letters or other characters in the data. What answer could possibly be found if you tried to add 1 + FD3? It doesn’t work. So I had to find a way to convert values like these into new ones that contained only numbers. 

Next I had to decide if it would be better to use all of the data that was given or not. I had to do some research and learn about the real estate industry. What kinds of things have a high impact on the sale price of a home? Which ones have a low impact? For the average person looking to buy or rent a new home, would they care more about the type of fireplace, or how many bedrooms there are? Would they care more about what kind of deck the home has, or the square footage of the basement?

By researching these kinds of questions, I could give more attention to certain parts of the data. Sometimes when making predictive models, it is better not to use all of the data, but instead only that which is the most pertinent. 

After completing these steps, I took what I learned about real estate and the cleaned data, and started to build my predictive models. It is better to build multiple models, as some will be stronger or weaker, depending on characteristics of the data. Sometimes it is hard to tell which models will be best until you test them out. Also, combining results of multiple models in a certain way can produce new results that are more accurate than those of any single model. 

Once I had built my models, tested them, and was happy with the results, I submitted them to the Kaggle system for scoring.

### Timeline/Scoring
The competition includes 2 rounds: Round 1 (a qualifying round) and Round 2 (the final round). Round 1 began in May 2017, with submissions for that round accepted until mid-October. At the Round 1/October 2017 deadline, teams contributed final updates to predictive models, the leaderboard locked, and scoring commenced. Teams that finish in the top 100 will continue on to Round 2 in January 2018. From there, competitors will have the opportunity to enhance pre-existing models accordingly.

There are two leaderboards: 1 public and 1 private. To uphold the integrity of the competition, the public leaderboard is scored on a different set of data than that of the private leaderboard. Kaggle may also temporarily swap the leaderboard display between the public and private versions. This, and a variety of other factors (such as team disqualification), may temporarily alter the accuracy of the publicly displayed rankings.


### Results and Code Availability
Competition scoring is currently ongoing, with 3,700+ teams (initially 3,800+) competing for $1.2 million in prizes. Due to the nature of the project, code and strategy for the predictive models cannot be publicly released at this time. In the meantime, I'm glad to discuss aspects of my process, and share some code that I used when examining the competition data. I'm presently in the top 0.6%.


## About Files/Folders in this Repository
* EDA folder: The images within the Exploratory Data Analysis (EDA) folder were created using the Jupyter Notebook described below. These graphs help viewers understand basic characteristics of the data used in the competition.
* Zillow_EDA.ipynb: This Jupyter Notebook was created to display some of the initial steps that I took before building my predictive models. The notebook contains code cells that can be run individually, as well as markdown cells that only contain text to explain the each of the steps. 

## Installation
The installation documentation for the Jupyter platform can be found [here](https://jupyter.readthedocs.io/en/latest/install.html).

Documentation for advanced usage of Jupyter notebook can be found [here](https://jupyter-notebook.readthedocs.io/en/latest/).
 
 
This project requires **Python 3.6** and the following Python libraries installed:
* [NumPy](http://www.numpy.org/)
* [Pandas](http://pandas.pydata.org)
* [openpyxl](http://openpyxl.readthedocs.io/en/default/index.html)
* [folium](https://folium.readthedocs.io/en/latest/)
* [scikit-learn](http://scikit-learn.org/stable/)
* [matplotlib](http://matplotlib.org/)
* [seaborn](https://seaborn.pydata.org/)


To run locally on your machine, launch with:
 
     $ jupyter notebook
     



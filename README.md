# Linear-Regression

# Metis Project 2: Linear Regression

## ABSTRACT:

**I scraped data from Box Office Mojo and built Linear Regression models that predict domestic gross for top domestic movies.**

I examined the target of domestic gross and feature inputs including Domestic Opening Gross, Running Time, Release Month, Release Year, Distributor, Genre, MPAA Rating, Budget, World Gross, and Foreign Gross.


## DESIGN:

My client is a Movie Producer who wants to ensure that their plan for a new movie is a smashing success and their budget, marketing costs, and overhead is spent wisely. For instance, if a movie flops at the opening, the Producer might want to siphon off any extra expenditures and re-evaluate their marketing plan. 


I explored the Box Office Mojo website and scraped data from the top 1000+ films in terms of domestic gross. 


## DATA:

	Box Office Mojo's top lifetime grossing films: 
	- https://www.boxofficemojo.com/chart/top_lifetime_gross/?area=XWW
	
## ALGORITHMS:

_*Data Cleaning*_

** I started off by scraping data from Box Office Mojo using Beautiful Soup and Python's Pandas package
** Next, I standardized the data by clearing white space, dropping unecessary columns, and cleaning up any extraneous data.
** In doing Exploratory Data Analysis, I narrowed down the key features to do my regression analysis of based on coefficient size.
** I focused on the mass-market viable movies only by restricting the analysis to PG rated movies; G, PG13, and R rated movies were removed since they are marketed and consumed by and targeted for a smaller audience, comparatively.


_*Analysis*_

** Feature Selection & Engineering: I chose to just look at the top performing Genre by looking at the Coefficient of Determiniation as well as the percentage of films a Genre was seen in. In this case, Comedy movies were the best indicator of a profitable movie genre. I also used this same reasoning to narrow down the list of Distributors to just Walt Disney Studios. 
** Model Selection and Evaluation: did proper validation and testing.


** A simple linear regression model with multiple multiplicative interaction terms was selected in addition to Lasso Regulation. Features included in the final model are domestic opening weekend gross, Disney as distribution company, comedy genre, release month, PG rating, running time, budget, number of markets (countries movie is shown in).


** The model was optimized for R2 and mean absolute error. The final model's test data outputted an R2 of 0.71 for Linear Regression in Train/Test/Val, and then the Cross-Validation test was 0.704.


## TOOLS:

** Python
** Beautiful Soup
** HTML
** Matplotlib
** Pandas
** Numpy
** Statsmodels
** Scikit-Learn


## COMMUNICATION

My analysis will be presented in Google Sheets using visualizations created with Matplotlib. See GitHub repository for project files and code.

# Linear-Regression

# Metis Project 2: Linear Regression

## ABSTRACT:

**I scraped data from Box Office Mojo and built Linear Regression models that predict domestic gross for top domestic movies.**

I examined the target of domestic gross and feature inputs including Domestic Opening Gross, Running Time, Release Month, Release Year, Distributor, Genre, MPAA Rating, Budget, World Gross, and Foreign Gross.
----------------
To reduce statistical noise and maximize the chances that resources would get used, I focused on MTA traffic after work hours, between 4pm - 8pm, assuming that people would seek these types of services outside of their typical work day. I analyzed traffic over the course of Spring 2021 (March - June) to inform my client when to anticipate fluxes in traffic for Spring 2022. With these metrics, my client can best anticipate relative clinic traffic due to proximity to heavily used subway stations and allow them to readily stock up on supplies.

I developed graphs using matplotlib to visualize which stations had the most traffic in terms of daily average and overall traffic to best assess which nearby clinics should receive additional resources and funding. 


## DESIGN:

My client is a Movie Producer who wants to ensure that their plan for a new movie is a smashing success and their budget, marketing costs, and overhead is spent wisely. For instance, if a movie flops at the opening, the Producer might want to siphon off any extra expenditures and re-evaluate their marketing plan. 


I explored the Box Office Mojo website and scraped data from the top 1000+ films in terms of domestic gross. 


## DATA:

	Box Office Mojo's top lifetime grossing films: 
	- https://www.boxofficemojo.com/chart/top_lifetime_gross/?area=XWW
	
## ALGORITHMS:

_*Data Cleaning*_

Algorithms:
- build a linear regression in python, using techniques such as:
—> feature engineering
—> add polynomial and interaction features
—> regularization
- rigorous model selection and evaluation (proper validation and testing) required

and movie profiles using BeautifulSoup
acquisition: web scraping put links
	•	storage: flat files
	•	sources: (as listed below or any other publicly available information)
	•	movie: boxofficemojo.com, imdb.com
	•	sports: sports-reference.com
   - primary data must be scraped
- have a continuous, numerical target variables to predict (GROSS), 1000+ data points and 10+ features
- feature engineering & selection challenges
- 

** I started off by scraping data from Box Office Mojo using Beautiful Soup and Python's Pandas package
** Next, I standardized the data by clearing white space, dropping unecessary columns, and cleaning up any extraneous data.
** In doing Exploratory Data Analysis, I narrowed down the key features to do my regression analysis of based on coefficient size.
** I focused on the mass-market viable movies only by restricting the analysis to PG rated movies; G, PG13, and R rated movies were removed since they are marketed and consumed by and targeted for a smaller audience, comparatively.


_*Analysis*_
** Feature Selection

** I aggregated entry and exit data to create analysis on total station traffic using a merge function in Pandas.
** I noticed that station traffic increased from March - June for each station overall, as well as for the top 3 stations.
** Traffic was typically greatest on Mondays.
In a linear regression, the R-squared term is a measure of “goodness of fit”, and in this case the resulting model had an R-squared of 0.502, which means that just over 50% of the variation among the observed data can be explained by the results OLS regression model. The underlying distribution of the data is unlikely to be linear in nature, which limits our ability to improve R-squared substantially, however in order to improve the model, my next step would be to create interaction terms for runtime versus genre (I suspect in general there is a overall optimal runtime for movies, but that perhaps audiences will expect fantasy movies to be longer than action movies of similar budgets) and to scrape more years of worldwide movie releases so that we are expanding our label-space at the same time as we add more features.


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

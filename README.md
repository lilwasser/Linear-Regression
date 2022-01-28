# Linear-Regression

# Metis Project 2: Linear Regression

## ABSTRACT:

**Use scraped data to build LR models that address a useful prediction and /or interpretation problem. Build a regression model to predict foreign lifetime gross for top domestic movies.
**

The goal of this project was to provide insight into the relationship between Metropolitan Transportation Authority (MTA) turnstile activity, specifically its most heavily foot-trafficked stations, and the locations of sexual health clinics in New York. 

To reduce statistical noise and maximize the chances that resources would get used, I focused on MTA traffic after work hours, between 4pm - 8pm, assuming that people would seek these types of services outside of their typical work day. I analyzed traffic over the course of Spring 2021 (March - June) to inform my client when to anticipate fluxes in traffic for Spring 2022. With these metrics, my client can best anticipate relative clinic traffic due to proximity to heavily used subway stations and allow them to readily stock up on supplies.

I developed graphs using matplotlib to visualize which stations had the most traffic in terms of daily average and overall traffic to best assess which nearby clinics should receive additional resources and funding. 


## DESIGN:

### above: The clearly defined client backstory is exceptionally creative and involved, and is addressed in a highly proficient manner.

	•	iterative design process
	•	"MVP"s and building outward

My client, NYC Department of Health and Mental Hygiene (NYC DOHMH), offers free sexual health services and supplies through their NYC Condom Availability Program. Products are distributed at local businesses, community-based organizations, and health care facilities. The Program gives away more than 30 million free safer sex products every year to over 3,500 locations and across all five boroughs. 

The NYC DOMHM has asked me to help them prepare for safe sex supply distributions in Spring 2022, so I explored the MTA turnstile data from March - June to discover which stations had the highest foot traffic after work hours in Spring 2021. I assumed that people would be more likely seek these types of supplies outside of regular working hours and somewhere near their subway station once they get off work, so my time frame is between 4pm - 8pm Monday through Friday. I looked at the top 3 busiest stations based on overall traffic (exits+entries) and then used location data to identify which 3 nearby clinics would subsequently garner the most foot traffic and should receive additional resources and funding 

## DATA:

	Box Office Mojo's top lifetime grossing films and movie profiles using BeautifulSoup
acquisition: web scraping put links
	•	storage: flat files
	•	sources: (as listed below or any other publicly available information)
	•	movie: boxofficemojo.com, imdb.com
	•	sports: sports-reference.com
   - primary data must be scraped
- have a continuous, numerical target variables to predict (GROSS), 1000+ data points and 10+ features
- feature engineering & selection challenges

## ALGORITHMS:

_*Data Cleaning*_


Algorithms:
- build a linear regression in python, using techniques such as:
—> feature engineering
—> add polynomial and interaction features
—> regularization
- rigorous model selection and evaluation (proper validation and testing) required

** I pulled data from 2/27 to 6/26 of 2021 for my complete analysis. I started off by standardizing all the column names by clearing white space and providing a uniform format, and dropped unecessary columns. 
** I removed all turnstile records that were not reported between the hours of 4 pm to 8 pm Monday - Friday.
** In some cases, the turnstiles were being counted in reverse, which led to inaccurate calculations in regards to entry and exit data. I cleaned up these errors early on in data analysis.
** There were some outrageous numbers when it came to entry and exit data for a given turnstile. Even in one of the biggest cities in the world, it would be impossible for a single turnstile in New York to see 1 million entries in a given day. I created thresholds on these counters to account for outliers in the data.
** I used a function to identify reverse counting, resets, and extra large numbers in the cumulative count for a turnstile.

I scraped information on budget, MPAA rating, runtime, genre, and release date for five years (2011-2015) of worldwide releases from BoxOfficeMojo using Beautiful Soup and Python 3.4 Anaconda distribution with pandas. I focused on the mass-market viable movies only by restricting the analysis to PG, PG-13, and R rated movies; G rated movies were removed since they are marketed and consumed in a very different way, such as requiring toy tie-ins.
In a linear regression, the R-squared term is a measure of “goodness of fit”, and in this case the resulting model had an R-squared of 0.502, which means that just over 50% of the variation among the observed data can be explained by the results OLS regression model. The underlying distribution of the data is unlikely to be linear in nature, which limits our ability to improve R-squared substantially, however in order to improve the model, my next step would be to create interaction terms for runtime versus genre (I suspect in general there is a overall optimal runtime for movies, but that perhaps audiences will expect fantasy movies to be longer than action movies of similar budgets) and to scrape more years of worldwide movie releases so that we are expanding our label-space at the same time as we add more features.


_*Analysis*_

** I aggregated entry and exit data to create analysis on total station traffic using a merge function in Pandas.
** I noticed that station traffic increased from March - June for each station overall, as well as for the top 3 stations.
** Traffic was typically greatest on Mondays.

## TOOLS:

** Python
** SQLAlchemy
** Matplotlib
** Pandas
** Numpy
** SQLite
** Geocode
** Geopy

Skills:
	•	basics of the web (requests, HTML, CSS, JavaScript)
	•	web scraping
	•	numpy and pandas
	•	statsmodels, scikit-learn
   - BeautifulSoup 
- HTML 
- LR
- Feature Selection

## COMMUNICATION

My analysis will be presented in Google Sheets using visualizations created with Matplotlib, Seaborn, and Geocode.
	•	organized project repository
	•	slide presentation
	•	visual and oral communication in presentations
	•	write-up of process and results

FILES
	1.	movies.csv contains the data scraped from the web
	2.	web_scraping.ipynb shows the process of scraping movie data from the 3 websites
	3.	model_testing.ipynb shows the process of evaluating linear regression models and plotting feature relationships


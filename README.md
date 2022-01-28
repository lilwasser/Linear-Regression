# Linear-Regression

# Metis Project I: Exploratory Data Analysis

## ABSTRACT:

The goal of this project was to provide insight into the relationship between Metropolitan Transportation Authority (MTA) turnstile activity, specifically its most heavily foot-trafficked stations, and the locations of sexual health clinics in New York. 

To reduce statistical noise and maximize the chances that resources would get used, I focused on MTA traffic after work hours, between 4pm - 8pm, assuming that people would seek these types of services outside of their typical work day. I analyzed traffic over the course of Spring 2021 (March - June) to inform my client when to anticipate fluxes in traffic for Spring 2022. With these metrics, my client can best anticipate relative clinic traffic due to proximity to heavily used subway stations and allow them to readily stock up on supplies.

I developed graphs using matplotlib to visualize which stations had the most traffic in terms of daily average and overall traffic to best assess which nearby clinics should receive additional resources and funding. 


## DESIGN:

### above: The clearly defined client backstory is exceptionally creative and involved, and is addressed in a highly proficient manner.

My client, NYC Department of Health and Mental Hygiene (NYC DOHMH), offers free sexual health services and supplies through their NYC Condom Availability Program. Products are distributed at local businesses, community-based organizations, and health care facilities. The Program gives away more than 30 million free safer sex products every year to over 3,500 locations and across all five boroughs. 

The NYC DOMHM has asked me to help them prepare for safe sex supply distributions in Spring 2022, so I explored the MTA turnstile data from March - June to discover which stations had the highest foot traffic after work hours in Spring 2021. I assumed that people would be more likely seek these types of supplies outside of regular working hours and somewhere near their subway station once they get off work, so my time frame is between 4pm - 8pm Monday through Friday. I looked at the top 3 busiest stations based on overall traffic (exits+entries) and then used location data to identify which 3 nearby clinics would subsequently garner the most foot traffic and should receive additional resources and funding 

## DATA:

* MTA turnstile data  (March - June 2021)

    * http://web.mta.info/developers/turnstile.html 


* NYC Venues providing safe sex products and resources

    * https://data.cityofnewyork.us/Health/NYC-Condom-Availability-Program-HIV-condom-distrib/4kpn-sezh

## ALGORITHMS:

_*Data Cleaning*_

** I pulled data from 2/27 to 6/26 of 2021 for my complete analysis. I started off by standardizing all the column names by clearing white space and providing a uniform format, and dropped unecessary columns. 
** I removed all turnstile records that were not reported between the hours of 4 pm to 8 pm Monday - Friday.
** In some cases, the turnstiles were being counted in reverse, which led to inaccurate calculations in regards to entry and exit data. I cleaned up these errors early on in data analysis.
** There were some outrageous numbers when it came to entry and exit data for a given turnstile. Even in one of the biggest cities in the world, it would be impossible for a single turnstile in New York to see 1 million entries in a given day. I created thresholds on these counters to account for outliers in the data.
** I used a function to identify reverse counting, resets, and extra large numbers in the cumulative count for a turnstile.

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

## COMMUNICATION

My analysis will be presented in Google Sheets using visualizations created with Matplotlib, Seaborn, and Geocode.



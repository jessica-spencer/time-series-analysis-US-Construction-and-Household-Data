# Time Series Analysis: US Construction and Household Data

Granger causality analysis of the relationship between cost of residential construction and number of households in the US.

Created on Kaggle: [https://www.kaggle.com/code/uwu1234/time-series-analysis-usconstruction-households]

## Description

Decided to do a quick analysis of Construction Spending and Total Households in the US. It's a small dataset, because we have only yearly datapoints, but I hypothesize that they will be strongly related.

My analysis includes
  - Datasets Explained
  - Cleaning & Initial Visualization
  - Stationarity Tests - ADFuller and KPSS
  - Transformation to Stationary data - difference method
  - Vector Autoregressive Model
  - Durbin-Watson Statistic to check for Autoregression
  - Granger-Causality Analysis
  - Conclusions

## The Data

### Construction dataset:
https://www.census.gov/construction/c30/definitions.html

Observation Start: 2001

Observation End : 2019

Frequency: Monthly

Construction includes the following:

New buildings and structures.

Additions, alterations, conversions, expansions, reconstruction, renovations, rehabilitations, and major replacements (such as the complete replacement of a roof or heating system).

Mechanical and electrical installations

Site preparation and outside construction of fixed structures or facilities such as sidewalks, highways and streets, parking lots, etc.

Installation of boilers, overhead hoists and cranes, and blast furnaces.

Fixed, largely site-fabricated equipment not housed in a building,like storage tanks, refrigeration systems, etc.

Cost and installation of construction materials

VALUE OF CONSTRUCTION PUT IN PLACE The “value of construction put in place” is a measure of the value of construction installed or erected at the site during a given period. For an individual project, this includes—

Cost of materials installed or erected, Cost of labor, Contractor’s profit, Cost of architectural and engineering work, Miscellaneous overhead and office costs chargeable to the project on the owner’s books and Interest and taxes paid during construction (except for state and locally owned projects).
The total value-in-place for a given period is the sum of the value of work done on all projects underway during this period.

CLASSIFICATION OF CONSTRUCTION The downloaded dataset only looks at the Residential Construction, which inclues:

Residential Buildings New single family New multi-family Includes new apartments and condominiums.

State and local includes remodeling, additions, and major replacements, the addition of swimming pools and garages, and replacement of major equipment items such as water heaters. Maintenance and repair work is excluded.

Includes remodeling, additions, and major replacements, includes construction of additional housing units in existing residential structures, Maintenance and repair work is not included.

### Household Dataset:
Observation Start: 1940-01-01

Observation End : 2019-01-01

Frequency: Yearly

Household is an occupied housing unit. Householder is a person in whose name the housing unit is rented or owned. This person must be at least 15 years old. Family household is a household in which there is at least 1 person present who is related to the householder by birth, marriage or adoption. Family is used to refer to a family household. In general, family consists of those related to each other by birth, marriage or adoption.

This data uses the householder's person weight to describe characteristics of people living in households. As a result, estimates of the number of households do not match estimates of housing units from the Housing Vacancy Survey (HVS). The HVS is weighted to housing units, rather than the population, in order to more accurately estimate the number of occupied and vacant housing units. For more information about the source and accuracy statement of the Annual Social and Economic Supplement (ASEC) of the Current Population Survey (CPS) see the technical documentation accessible at: http://www.census.gov/programs-surveys/cps/technical-documentation/complete.html

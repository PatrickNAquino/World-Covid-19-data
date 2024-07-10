# World-Covid-19-data
Explore the global data on COVID-19 cases, deaths and vaccinations.


## Overview
The dataset provided by [Our World in Data](https://ourworldindata.org/) brings us into the history of the COVID-19 pandemic from Jan/2020 until Apr/2024 with the possibility to analyse cases, deaths and vaccination across the globe.

Link to the dataset: [OWID-COVID-19-Data](https://github.com/owid/covid-19-data/tree/master/public/data)

## Measures (DAX)
The dashboard allow us to track all the data about the COVID-19 scenario in the world. So to understand the data I had to create some measures.

- Population = MAX('owid-covid-data'[population]) 
- Total Cases = SUM('owid-covid-data'[new_cases])
- Total Deaths = SUM('owid-covid-data'[new_deaths])
- Total Tests = SUM('owid-covid-data'[new_tests])
- Total Vaccines = SUM('owid-covid-data'[new_vaccinations])
- People Vaccinated (full) = MAX('owid-covid-data'[people_fully_vaccinated])
- % Population Vaccinated = [People Vaccinated (full)]/[Population]
- % Positive Tests = DIVIDE([Total Cases],[Total Tests])
- % Positive Tests = DIVIDE([Total Cases],[Total Tests])
- % Mortality = DIVIDE([Total Deaths],[Population])
- % Infection Fatality = DIVIDE([Total Deaths],[Total Cases])

## Analysis
[PowerBI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNTIwOGQ4MjktMWRkOC00ZGQwLWI3ZTktOTczNWQ2NzVkNjBiIiwidCI6Ijc5NzgyMzFkLTA4ZjAtNDVhNy05ZDEzLTc3YzNmYTk2OGI4OCJ9)

Until Apr/2024 in the world we had 775M positive cases of COVID-19 with 7M deaths, corresponding to a 0.9% of infected people dying. If we consider all the global population this represents a mortality of 0.5%.
- United States and China are the top counties in COVID-19 cases reported. Cases were higher back in 2022 with 424M people infected, this represents 55% of cases in just 1 year.
- USA leads total deaths also, followed by Brazil with 1.2M and 702K cases respectivelly.
- The peak of death occured in 2021 with 57% of total deaths. In this period the USA registered 40% of the total deaths in the country;
- With 89% of global population vaccinated in 2024, the cases and mortality dropped signifficantly. But the scennario wasn't that back in 2021 where the mortality rate achieved the highest value 0.2%. Brazil, United Kingdom and USA suffered a lot with deaths in this period;
- Even with higher number of cases in 2022, the effect of vaccination can be visualized through the lowest infection fatality rate, just 0.3%, where in 2020 and 2021 we experienced 2.4% and 1.8%. This show us that people are safer even when they are infected with the virus.

Now in 2024 COVID-19 is still between us, but the data shows that the effects of the virus is now attenuated. The world is now safer even with the possibility of contamination our chances to survive are better.

![image](https://github.com/PatrickNAquino/World-Covid-19-data/assets/118391206/f6b438bf-eeaa-489a-81d4-44a39dd4304d)

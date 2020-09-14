![Exploratory Data Analysis - Course Project](./assets/cover.jpg)

The overall goal of this project is to explore the National Emissions Inventory database and see what it say about fine particulate matter pollution in the United states over the 10-year period 1999–2008.

## The Data Set

Fine particulate matter (PM2.5) is an ambient air pollutant for which there is strong evidence that it is harmful to human health. In the United States, the Environmental Protection Agency (EPA) is tasked with setting national ambient air quality standards for fine PM and for tracking the emissions of this pollutant into the atmosphere. Approximatly every 3 years, the EPA releases its database on emissions of PM2.5. This database is known as the National Emissions Inventory (NEI). You can read more information about the NEI at the <a href="http://www.epa.gov/ttn/chief/eiinformation.html">EPA National Emissions Inventory web site</a>.

For each year and for each type of PM source, the NEI records how many tons of PM2.5 were emitted from that source over the course of the entire year. The data that you will use for this assignment are for 1999, 2002, 2005, and 2008.

The data for this project are available from the course web site as a single zip file:

<ul>
  <li><a href="https://d396qusza40orc.cloudfront.net/exdata%2Fdata%2FNEI_data.zip">Data for Peer Project [29Mb]</a></li>
</ul>

PM2.5 Emissions Data (\color{red}{\verb|summarySCC_PM25.rds|}summarySCC_PM25.rds): This file contains a data frame with all of the PM2.5 emissions data for 1999, 2002, 2005, and 2008. For each year, the table contains number of tons of PM2.5 emitted from a specific type of source for the entire year. Here are the first few rows.

<ul>
<li>fibs: A five-digit number (represented as a string) indicating the U.S. county</li>
<li>SCC: The name of the source as indicated by a digit string (see source code classification table)</li>
<li>Pollutant: A string indicating the pollutant</li>
<li>Emissions: Amount of PM2.5 emitted, in tons</li>
<li>type: The type of source (point, non-point, on-road, or non-road)</li>
<li>year: The year of emissions recorded</li>
</ul>

Source Classification Code Table (\color{red}{\verb|Source_Classification_Code.rds|}Source_Classification_Code.rds): This table provides a mapping from the SCC digit strings in the Emissions table to the actual name of the PM2.5 source. The sources are categorized in a few different ways from more general to more specific and you may choose to explore whatever categories you think are most useful. For example, source “10100101” is known as “Ext Comb /Electric Gen /Anthracite Coal /Pulverized Coal”.

## Questions
#### Have total emissions from PM2.5 decreased in the United States from 1999 to 2008? Using the base plotting system, make a plot showing the total PM2.5 emission from all sources for each of the years 1999, 2002, 2005, and 2008.

![Answer 1](./answer1.png)

#### Have total emissions from PM2.5 decreased in the Baltimore City, Maryland (fips == "24510") from 1999 to 2008? Use the base plotting system to make a plot answering this question.

![Answer 2](./answer2.png)

#### Of the four types of sources indicated by the type (point, nonpoint, onroad, nonroad) variable, which of these four sources have seen decreases in emissions from 1999–2008 for Baltimore City? Which have seen increases in emissions from 1999–2008? Use the ggplot2 plotting system to make a plot answer this question.

![Answer 3](./answer3.png)

#### Across the United States, how have emissions from coal combustion-related sources changed from 1999–2008?

![Answer 4](./answer4.png)

#### How have emissions from motor vehicle sources changed from 1999–2008 in Baltimore City?

![Answer 5](./answer5.png)

#### Compare emissions from motor vehicle sources in Baltimore City with emissions from motor vehicle sources in Los Angeles County, California (fips == "06037"). Which city has seen greater changes over time in motor vehicle emissions?

![Answer 6](./answer6.png)

## Quick start

| Step | Example |
| ------------- | ------------- |
| Download the data and unzip the files on the project folder | https://d396qusza40orc.cloudfront.net/exdata%2Fdata%2FNEI_data.zip |
| Run each script  | ```answer1.R``` - ```answer2.R``` - ```answer3.R``` - ```answer4.R``` - ```answer5.R``` - ```answer6.R```  |

## Dependecies

This project use the **dplyr** and **ggplot2** packages, you can download from **CRAN** just like that:
`install.packages('dplyr','ggplot2')`

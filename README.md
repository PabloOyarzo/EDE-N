# EDE-N

### Descripción del proyecto


### Scope of work
1. Business Task.
2. Descripción de todas las fuentes de datos utilizadas.
3. Documentación de cualquier manipulación de data o limpieza de data.
4. Summary del análisis, conjunto con visualización de la data. Todo a dashboard hosted

## Ask Phase: Statement of the Business Task
The primary business task is to design marketing strategies aimed at converting casual riders into annual members. To achieve this, we will explore how annual members and casual riders use Cyclistic bikes differently, why casual riders would be interested in purchasing annual memberships, and how digital media could influence their decision to become members. The insights gained from this analysis will help guide targeted marketing efforts towards casual riders.

Questions to Guide the Analysis:
How do annual members and casual riders use Cyclistic bikes differently?
Why would casual riders buy Cyclistic annual memberships?
How can Cyclistic use digital media to influence casual riders to become members?
Primary Stakeholders:
Lily Moreno - Director of Marketing.
Cyclistic Executive Team.
Secondary Stakeholders:
Marketing Analytics Team (my crew 😛)

## Ask Phase: Statement of the Business Task

The primary business task is to design marketing strategies aimed at converting casual riders into annual members. To achieve this, we will explore how annual members and casual riders use Cyclistic bikes differently, why casual riders would be interested in purchasing annual memberships, and how digital media could influence their decision to become members. The insights gained from this analysis will help guide targeted marketing efforts towards casual riders.

### Questions to Guide the Analysis:

1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

### Primary Stakeholders:

* Lily Moreno - Director of Marketing.
* Cyclistic Executive Team.

### Secondary Stakeholders:

* Marketing Analytics Team (my crew 😛)

## Prepare Phase: Descripción de todas las fuentes de datos utilizadas. Aquí vamos a listar y mostrar cómo preparamos la data para limpieza y procesamiento.

**Dataset:** The data for our analysis is sourced from divvy-tripdata, available in CSV format. The dataset has been provided by Motivate International Inc. and is accessible under their specified license agreement. It is important to note that the data does not include personally identifiable information, ensuring the privacy of the riders.

### Data Integrity and Credibility:

**Dataset:**

divvy-tripdata. [Click here](https://divvy-tripdata.s3.amazonaws.com/index.html) to access the dataset. For this project, we'll be working with data from June 2022 to June 2023. The data it’s in CSV format, and has been made available by Motivate International Inc. under this [license](https://divvy-tripdata.s3.amazonaws.com/index.html). Note that data-privacy issues prohibit the use of riders’ personally identifiable information, making it impossible to link trips to specific riders, in case casual riders purchase multiple single passes.

**Data integrity and credibility:**

The data has been evaluated using the "ROCCC" system to assess its credibility and integrity:

1. **Reliability:** The data is complete and free of duplicate entries, but it lacks information to account for bias.
3. **Originality:** The data is original and directly collected by Motivate LLC, a company that services bicycle sharing systems in North America.
4. **Comprehensiveness:** The data may not be comprehensive enough to cover all variables needed for a fair analysis.
5. **Current:** The data is updated monthly up to 2013, making it current.
6. **Cited:** The data includes all relevant sources and responsible parties.

Overall, the data integrity is acceptable but may have limitations in providing comprehensive insights due to potential biases. Any conclusions drawn from here only can lead to unfairness, and thus have to be further confirmed though a more reliable dataset.

**Data Usefulness:**

The dataset covers bike trip data from June 2022 to June 2023, comprising a substantial 6,548,648 rows summed up. This is a great amount of data points, all meaningful for the analysis.

**Data Organization:**

Each of the CSV files contain 13 columns. The variables include ride_id (character), rideable_type (character), started_at (date and time), ended_at (date and time), start_station_name (character), among others. The data represents information about individual bike trips, including details like ride identifiers, bike type, timestamps for starting and ending trips, station names and IDs, including geological data, and whether the rider is a casual or member customer.

### Generating the data


### Combining the Data

## Process Phase: Documentación de cualquier manipulación de data o limpieza de data.
In this section, we perform data cleaning and manipulation tasks. First, we recode the values in the columns 'member_casual' and 'rideable_type' to have more descriptive names ("Subscriber" instead of "member" and "Classic Bike" instead of "classic_bike," etc.). Next, we create new columns for 'year', 'month', and 'day' extracted from the 'started_at' column using the lubridate package. Additionally, we calculate the trip duration in seconds and add a new column 'trip_duration_secs' to the data frame. Some trips had negative durations, because they were taken out for maintenance. We want to filter those trips, and at last, create a cleaned data frame called clean_yearlytrips.

## Analyze Phase: Summary del análisis, conjunto con visualización de la data. Todo a dashboard hosted

# K-means-Clustering-Covid-data analysis

Coronavirus disease 2019 (COVID-19) is a contagious disease caused by a virus, the severe acute
respiratory syndrome coronavirus 2 (SARS-CoV-2). The first known case was identified in Wuhan, China, in
December 2019. The disease quickly spread worldwide, resulting in the COVID-19 pandemic.

As at the end of February 2023, there have been 758,390,564 cases and 6,859,093 deaths worldwide.
Effective screening or vaccination enables quick and efficient diagnosis of the virus, mitigating the burden on
the healthcare system, there have been 653,592,180 recovered cases worldwide.

This comparative analysis aims to ascertain how the world is managing, coping, and surviving with the virus
through preventive measures such as wearing of mask, isolation, vaccination, and improvement of general
hygiene. I chose the dataset from 1st of October 2020 to 1st of Janaury 2021 (Dataset 1) and 1st of October
2021 to 1st of January 2022(Dataset 2) using Kmeans clustering.

Firstly, the data was consolidated, renamed accordingly, and then cleaned (null/ negative values were
replaced or removed depending on the best approach for each situation).
Data cleaning is the process of detecting and correcting (or removing) corrupt or inaccurate records from a
record set, table, or database and refers to identifying incomplete, incorrect, inaccurate or irrelevant parts of
the data and then replacing, modifying, or deleting the dirty or coarse data. It is important because it
improves the data quality and, in so doing, increases overall productivity. For this case, it helped remove
errors in the clustering and negative clusters.

Geopy was used to confirm the accuracy of longitude and latitude in the dataset. Geopy helped in the
location of the coordinates of addresses, cities, countries, and landmarks across the globe using third-party
geocodes. For the clustering analysis only the Confirmed cases and Death columns were needed. So, all
other columns were dropped, to create a new data frame.

The confirmed cases and death scale (2 features needed for k means clustering) are different because
several confirmed instances will always be more than Death. The data were normalized to reduce the scale
using a standard scalar method. Please note that the k-means algorithm is dependent on Euclidean
distance, so having two features on different scales can be problematic to the k-means algorithm.
To know the best value of K to use in the clustering, create a scree plot (a line plot that helps determine the
number of clusters). The Elbow point defines the optimal value of k. the optimal values for k are k =3 and k
=4. SSE is decreasing linearly after both of these points. For this analysis, 4 is the best value for K. Since
deaths and confirmed cases are in different scales, feeding the k value and the scaled data frame
(X_scaled) to the K-Means algorithm is the best approach, then calculate the mean value of k to get the
value for each cluster. We had 4 clusters; Cluster 2- Moderate risk, Cluster 3- High risk, Cluster 1- very Low
risk, and Cluster 4- Low risk.

Data visualization was the final process assigning a color to each cluster, making it easier to read.
From the map, I agree with the result because the spread of covid dropped significantly except in countries
like England and Turkey, which had an outbreak of the variant Omicron. This can be further justified by the
WHO and Worldometer data. Only two countries remained in Moderate and high-risk countries from 2020 to
2021, and they are England and Turkey, and this was because of the omicron variant of Covid 19. A country
like Argentina moved from moderate risk to very low risk, while France moved from a high risk to a low risk
countries.

There was a decline in the infection and death rate across the world as countries implemented measures to
better manage the pandemic.

## REFERENCES
Department of Transport and Department of Health and Social care (2021): Red list of countries and
Territories. Available at: https://www.gov.uk/guidance/red-list-of-countries-and-territories
(https://www.gov.uk/guidance/red-list-of-countries-and-territories) (Accessed 22 February 2023)

Prime Minister's statement on coronavirus (COVID-19): 31 October 2020. Available at:
https://www.gov.uk/government/speeches/prime-ministers-statement-on-coronavirus-covid-19-31-october2020 (https://www.gov.uk/government/speeches/prime-ministers-statement-on-coronavirus-covid-19-31-
october-2020) (Accessed 24 February 2023).

Nahar, V. (2023) ‘Week 3’. 7CSO33: Data Mining and Informatics. Available at: https:
https://canvas.wlv.ac.uk/courses/36895/modules (https://canvas.wlv.ac.uk/courses/36895/modules)
(Accessed: 19 February 2023).

World Health Organization WHO. Coronavirus (Covid19) Dashboard. Available at: https://covid19.who.int/
(https://covid19.who.int/) (Accessed 24 February 2023)

Worldometer. Covid19 Coronavirus Pandemic. Available at: https://www.worldometers.info/coronavirus
(https://www.worldometers.info/coronavirus). (Accessed 25 February 2023)

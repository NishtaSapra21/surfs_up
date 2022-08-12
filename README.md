# Surfs Up Analysis

## Overview

This analysis reports temperature trends for month of June and December in Oahu, in order to determine if surf and ice-cream shop business is sustainable year-around or not using Python, Pandas functions and methods and SQLAlchemy.

## Results

After comparing two figures below of __June Temps__ and __December Temps__ ; following observations are made.

  ![june_summary](https://user-images.githubusercontent.com/107717882/184427319-b5a3ce03-2ad7-4f59-8dc5-bb19c7d32b61.png)![december_summary](https://user-images.githubusercontent.com/107717882/184427342-de8eeae6-b201-4a70-8d99-73a4d9c5e897.png)

  
* __Standard Deviation__ in both observations of temperatures for June and December are  __3.257417__ , __3.745920__  respectively. These deviations are lower than       mean so data clustered around mean. Let’s consider mean of June temperatures i.e around 75 that means most of the temperatures are around 75 degree as standard         deviation is much lower. You can see same for December, temperatures are clustered around mean value 71. There’s no much more difference but yes, June is better. 

* Considering range __(64(min temp) to 85(max temp))__ and __50th percentile__ which is __75__ for June temperatures, it is obvious that  50% of temperatures are fall     into half quartile, below 75 degree. So half of the temperatures are obviously above the 75 degree. Assuming that half of the days in June are having temperatures     above 75, it’s a good to go sign for surf and ice cream shop.  

  Let’s look at December range which is __from 56 to 83__ and __50th percentile__ is __71__.  It obvious that 50% of temperatures are below 71. December also looks       good for surfing and having ice creams. 
  
* Considering minimum temperatures for __June (64)__ and __December (56)__ with __25th percentile__ data, __73__  and __69__ for June and December respectively;         December might have less business than June 

## Summary

### __High-Level Summary__

Looking at summary statistics of June and December temperatures , we have lower standard deviations, not having big difference between maximum and minimum temperatures, more days of higher temperatures, so all data showing good sign to jump for surf and cream business. 

###  __Temperatures and Precipitation Together__ 

Let’s have a look below image.  

![june_temp_prcp_summary](https://user-images.githubusercontent.com/107717882/184429636-e96f0bce-9c1f-4690-a72b-80f415a7df07.png)![dec_temp_prcp_summary](https://user-images.githubusercontent.com/107717882/184429660-c611d1bf-0a9b-40fe-9b5a-53d3aabc62a4.png)

We can get this result by adding __’Precipitation’__ column to our June DataFrmes and using __june_df.describ()__ . The query is below. Same query we can use for December with specifies months, list and DataFrame. 

![june_query1](https://user-images.githubusercontent.com/107717882/184429702-9901224a-97ed-41cd-8d1a-7fa229b7408f.png)

Now, we can say that precipitation data of both June and December also support surf and ice-cream business. 75th percentile of June precipitation is __0.12__ and that is light rain. December has little more 75th percentile , __0.15__ but it can be considered as light rain. Clearly we have more than half of the days of no rain or very light rain, good for our business. 

###  __Average, Minimum, Maximum Temperatures and Precipitation of June and December Year Wise__

Here is the query that displays average, minimum and maximum temperatures for June year wise. We can use same query for December by changing month. 

![june_query2](https://user-images.githubusercontent.com/107717882/184429885-cbeada9b-7cb5-46bf-84d2-898aa4dc534b.png)

Here is the query that displays average, minimum and maximum precipitation for June. The same query we can use for December DataFrame. This observation can give more insight for business.

![june_query3](https://user-images.githubusercontent.com/107717882/184429919-5de428c5-f9a1-4021-82c0-68ecc6998308.png)

Followings are results for June temperatures and precipitations year wise.

![june_temps_yearwise](https://user-images.githubusercontent.com/107717882/184429974-bd6ccd89-3ef7-4f83-b2bb-f50c8d90ebc6.png)![june_prcps_yearwise](https://user-images.githubusercontent.com/107717882/184430028-545b2baa-aed1-4974-b396-05a574995d95.png)

Following are results for December temperatures and precipitations year wise.

![dec_temps_yearwise](https://user-images.githubusercontent.com/107717882/184430074-16b53636-2c2d-4fee-a9f7-921c2b1980ba.png)![dec_prcps_yearwise](https://user-images.githubusercontent.com/107717882/184430091-088770af-109c-4e76-bee6-cc31f7120783.png)

###  __Minimum, Average, maximum Temperatures and Precipitations Station Wise__

The following query displays minimum, average and maximum temperatures for December , station wise. This result can help us to decide on which stations are better for business. 

![dec_query1](https://user-images.githubusercontent.com/107717882/184430141-8dd3a39d-baf8-47a5-a645-02e672857187.png)

![dec_query2](https://user-images.githubusercontent.com/107717882/184430163-55675d00-182c-4c70-9d61-ebf470f40bdd.png)

![dec_query3](https://user-images.githubusercontent.com/107717882/184430173-b46a2cbb-cccf-4363-b4fc-9da5cc156f7e.png)

The following query displays minimum, average and maximum precipitation for December; station wise.

![station_dec_temps](https://user-images.githubusercontent.com/107717882/184430226-a771a629-3ab3-4a51-a4d8-db1242d99a8f.png)![station_dec_prcps](https://user-images.githubusercontent.com/107717882/184430243-c0c279f7-6d97-4af4-904e-8c15df329c43.png)

The following query displays minimum, average and maximum precipitation for June; station wise.

![station_june_temps](https://user-images.githubusercontent.com/107717882/184430297-e42e0d70-a40d-4830-a785-1041657751ae.png)![station_june_prcps](https://user-images.githubusercontent.com/107717882/184430315-c095b550-8315-4d38-b6f6-80e86223a61b.png)

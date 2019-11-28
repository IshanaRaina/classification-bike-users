##  Data Preprocessing

###  Inconsistent Data

- Some `Zip Code` values are less than 5 digits.  This is incorrect since this system is located in California where zip codes are 5 digits long. 

![](https://i.imgur.com/BtupGFn.jpg)

**Solution**: Eliminate the rows with incorrrect `Zip Code` values. 

- Some `Zip Code` values, even though 5 digits long, fall out of the correct range of zip codes for California.

![](https://i.imgur.com/qR1XACz.png)

**Solution**: Eliminate the rows with out-of-range `Zip Code`  values. 

- Some `Date` values are in the format _dd/mm/yyyy_ which is not the correct notation of writing dates in the US, or simply _yyyy_. 

![](https://i.imgur.com/fMmCA92.png)

**Solution**: Tableau was able to map the _dd/mm/yyyy_ dates to the correct _mm/dd/yyyy_ format. As for the _yyyy_ dates, those rows were eliminated. 

### Outliers

On plotting `Trip Count` v/s `Avg Duration`, it was observed that even though December has the least number of trip counts, the average duration of rides in December are almost double that of the other months. 

![](https://i.imgur.com/AdFx1Lp.png)

To visualize the data differently, the box-whisker plot is created. December is, in fact, an outlier with the `Avg(Duration)` value much higher than any other month.

![](https://i.imgur.com/ve4mniz.png)

Digging deeper into the matter, it is observed that there is a ride recorded with a `Duration` of 17,270,400 seconds ~ 200 days which seems unrealistic. Sounds more like 'Around the US in 200 days!' :stuck_out_tongue: 

![](https://i.imgur.com/0YEm3ga.png)

**Solution** Eliminate the row where the poor rider was apparently riding his bike for 200 days!

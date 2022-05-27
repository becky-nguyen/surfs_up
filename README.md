# surfs_up
## Overview
The purpose of this analysis is to review the weather in June and December in Hawaii to see if it would be ideal for year-round success for a surf shop. 


## Results

![june](https://user-images.githubusercontent.com/100896787/170632144-aead35fc-fc0d-4819-bb1e-44fb4c0cc7b2.PNG)

* Average temperature of June is 77.2 degrees F, with a standard deviation of 2.6 degrees. Temperatures would go down to 71 at the lowest and 83 at the maximum. 

![december](https://user-images.githubusercontent.com/100896787/170632166-5c4cf6ba-0f56-4c44-a41d-cbe943f3f994.PNG)

* Average temperature of December is 71.1 degrees F, with a standard deviation of 3.4 degrees. Temperatures would go down to 60 at the lowest and 78 at the maximum. 
* Surprisingly, there isn't that much of a difference between the average temperatures in June and July (only 6.1 degrees). December's max temperature is close to June's average. However, December's lowest temperature is far below the range for June. 

## Summary
Although December may drop in temperature, it can still be surf appropriate if it remains around the average or above. This suggests that the surf shop would still have good business in the months of December. 

Something to consider (and may help) is humidity. We can run an analysis on the humidity levels of these two months; because even though temperature may drop down to 60 degrees, if humidity is still high, the weather would be perfect for surfing! To get the humidity levels for June and December, we can use the following queries next time in our analysis:
* june = session.query(Measurement.date, Measurement.<insert_humidity>).filter((Measurement.date >= june_temp) & (Measurement.date < july_temp)).all()
* december = session.query(Measurement.date, Measurement.<insert_humidity>).filter((Measurement.date >= december_temp) & (Measurement.date < jan_temp)).all()


Additionally, precipitation should be considered as surfers may not want to surf if it's raining (unless it's really hot anyways!) To check the rainfall, we can use the following queries next time in our analysis: 
* june = session.query(Measurement.date, Measurement.<prcp>).filter((Measurement.date >= june_temp) & (Measurement.date < july_temp)).all()
* december = session.query(Measurement.date, Measurement.<prcp>).filter((Measurement.date >= december_temp) & (Measurement.date < jan_temp)).all()

# Hawaii Weather analysis

## Overview

This analysis is made to explore the business viabiility of Surf n' Shake shak in Oahu.

## Results

  - On average, there is no real difference between the average temperature between Jun and December. This makes our business and attractive year long possibility.
    
    ![image](https://user-images.githubusercontent.com/101848882/172084360-3b1bb500-f542-48ff-b136-224defd02aa5.png)    ![image](https://user-images.githubusercontent.com/101848882/172084385-ea22b0be-6727-48cd-bf7d-97f5d604ba79.png)

  - December does show a more extreme temperature with a minimum registered of 56 deegrees vs the 64 deegrees on June.


  - The maximum temperature is very similar though, so this makes us believe that the weather seems constant throughout the year.

## Summary

We observe a real investment opportunity in a suf n shake shak in Oahu. This is supported by a constant weather throughout the year and it being already a popular tourist spot. Should more information be required, queries for consulting temperatures during february, which is usually the coldest month, is added. Should the need arise, a query for the anual temperature data from the second more active station has been added. As to eloborate a secondary spot analysis for the bes surfing spot.

February temperatures query:
print(session.query(Measurement.tobs).filter(extract('month', Measurement.date) == 2).all())

Second most active station query:
session.query(Measurement.tobs).\
filter(Measurement.station == 'USC00519397').\
filter(Measurement.date >= prev_year).all()
print(results)

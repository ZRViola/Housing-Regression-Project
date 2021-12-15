
# Housing Price Linear Regression Project

The housing price prediction dataset by Shree from Kaggle
provides data for several features in regards to the housing market. 
It provides features related to the different sizes, rooms, and locations 
of numerous homes. I chose this dataset because I was interested in seeing 
what factors and variables actually affect the price of a home. As a young 
adult, eventually I will have to buy a house, and I thought this would be helpful 
to see what is taken into account during the process. 




## The Problem
I want to find and plot any relationship or correlation between 
some of the variables of this dataset and the price of homes to 
see how they affect, or do not affect, the price. This data was in tidy format, and featured 
4600 observations of 18 variables. I also added a new feature called 
"age" to represent how old the homes were. I will be specifically focusing on how the variables 
of living space, lot size, bathrooms, bedrooms, and age affect the price of a house.

## Analysis
After deciding which variables I was going to focus on
in this analysis, I got straight to plotting. I plotted the
variables of square feet, lot size, bathrooms, bedrooms,
and age each against the prices of the houses on a boxplot.
I then proceeded to calculate each of their correlation 
with the price variable. I found that none of them had any 
strong or signifcant correlations. They were are all pretty weak
and close to 0. The graphs showed no strong positively or negatively
signifcant trends either which surprised me. I then proceeded to 
to find the linear regression between each variable and price.
Just as I found with correlation, there were no strong multiple R-squared
values among any of the variables. 
## Challenges
I faced a handful of challenges while dealing with this
dataset. For one, when I first attempted to plot each variable
against price on a box plot, the data was all gathered into one area 
and very hard to see or make anything of it. I also faced many outliers
in this dataset which were very prevalent in my graphs. In an attempt 
to combat this, I modified my boxplots by using the features of "scale_x_continuous"
and "scale_y_continuous." In short, this helped to make my data easier to see
and read on my graphs. It raised and spread the data out a lot. 
Here's what one of the codes looked like:

lot_price<-ggplot(data=house_df,aes(x=sqft_lot, y=price, color="red"))+
  geom_point()+
  xlab("Square Feet")+
  ylab("Price")+
  ggtitle("Square Feet vs. Price")+
  scale_x_continuous(trans="log10")+
  scale_y_continuous(trans="log10")

## Conclusion
In conclusion, the data and analysis proved that 
none of the variables were really significant in 
affecting the price of a house. This lead me to the conclusion
that factors like location play a much bigger role in affecting
the price of a house. Things like state, city, and geographical location
would definitely have a much stronger correlation with price than these
variables I originally thought would. Converting several different locations 
into numerical values in a dataset would be challenging, 
but those are the true variables that will predict the price 
of a house.

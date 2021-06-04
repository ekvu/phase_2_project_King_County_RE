![Opening Image](https://github.com/ekvu/phase_2_project_vac_pandas/blob/main/images/istockphoto-619736868-612x612.jpg?raw=true)

Image from istockphoto.com
# King County Housing's Reigning Features
Authors: Brian Matsiko, Erin Vu

# Table of Contents
1. Overview
2. Business Problem
3. Data
4. Recommendations
5. Conclusion
6. For More Information

# 1. Overview

In this notebook, we will be exploring the Kings County real estate sales data to identify key features that drive prices up in housing sales in order to maximize the market value of a home to sell for the highest profit margin. In identifying these key features, we can recommend to remodel houses or multifamily units, and focus on these features in new developments to increase their value to rent and sell at higher prices, maximizing profits. We used Python to clean and preprocess the data, execute exploratory data analysis, and build simple and multiple linear regression models.

# 2. Business Problem

Our stakeholders at Seattle Rental Group/Pointe3 offers services for not only property owners but also to renters and buyers. Their property owner service side will help you lease or sell your home or multifamily property. We want to know what sells high value homes. Properties will have many different facets that will be more or less attractive to buyers and renters which impacts the market value. We want to investigate how we can advise Seattle Rental Group/Pointe3 to apply features to their properties and new developments and advise property owners who use their services to remodel and upgrade their properties to maximize the market value of the property to sell or lease. The initial features we believe have an impact on prices are square feet of the property, the room count of the property, and whether or not the property is waterfront and will explore these feaures and others.

# 3. Data

- The source for this data is from the official government website of [King County for housing sales](https://info.kingcounty.gov/assessor/esales/Residential.aspx) in 2014-2015.
- The data is relevant for our analysis because we are focusing in the King's County area and this set has information about housing sales in King's County.
- The data set includes 21,597 records 21 features
- Our target variable is sale price
- Features included:
-     -house id, 
      -sale date, 
      -sale price, 
      -bedrooms, 
      -bathrooms, 
      -square footage of home, 
      -square footage of the lot, 
      -how many floors, 
      -waterfront or not, 
      -view rating, grade of house, 
      -square footage above the basement, 
      -square footage of the basement, 
      -the year the house was built,
      -the year the house was renovated, 
      -the zip code of the house, 
      -the latitude and longitude, 
      -square footage of the living space for the nearest 15 neighbors
      -square footage of lot for the nearest 15 neighbors

# 4. Methods 

- We started off by importing the data and looking at the data
- We then identified our numerical/continuous variables and our categorical variables and started framing our questions
- We cleaned our data in Python and then visualized our data through histograms and correlation plots with Seaborne and Matplotlib
- We then used Stats Models and ScikitLearn to build our first simple linear regression model
- First simple model: Target was price and our variable was sq ft of living area as it had the highest correlation to price
- We observed our R^2 to be 0.49 and our coefficient to be 280.87, meaning an increase in sqft increases the sale price by $280.87.

![FSM](https://github.com/ekvu/phase_2_project_vac_pandas/blob/main/images/fsm_dark.png?raw=true)


- After our first model, we added, transformed, and engineered new features to observe how they impacted price
- We then examined our results and formulated our conclusions.

We believe that this approach is appropriate as our goal of our analysis is to see what features drive sale price up so we can focus on remodelling or upgrading to those features.

# 5. Results

From the results of our modelling, we were able to add and identify features with a positive impact on the sale price. We explored the zip codes and saw that these zip codes, 98039, 98004, 98112, 98102, 98109 had the largest coefficients meaning they had a greater influence on the price if they were located in these zipccodes vs other zip codes. We were able to also observe the average price of the homes in those zip codes and compare against the total mean.

![Bar Chart](https://github.com/ekvu/phase_2_project_vac_pandas/blob/main/images/Mean_Sales_Zip_Price.png?raw=true)

We also observed other key features such as waterfront, view count, sqft, and renovations as having a positive impact on the price as shown by the coefficient. We thought bedrooms would have a positive impact on price but as the bedrooms increased, the coefficients increased negatively.

![Final Model Coefficients](https://user-images.githubusercontent.com/80011920/120841022-d4d02180-c51f-11eb-8f83-9b9c4de4d15f.png)


# 6. Conclusions

In our final model, we found that the zip code, waterfront, view count, sqft, and renovation features had the greatest impact on sale price of houses in King County of Washington with an R^2 of 0.87. We recommend that our stakeholder remodel, upgrade, and develop properties in Medina, Bellevue, Madison Park, East Lake, East Queen Anne with waterfronts and amazing views to increase the value of the home and sale price. Our stakeholder can also communicate these findings to property owners who use their services to lease or sell their own properties. Our model might not fully solve the business problem as our data only includes home sales and not multifamily buildings. We also lack a full understanding of the neighborhoods and how they are perceived. Other ways our model might be incomplete are the other amenities a house might have not included in the data, such as ac/heater systems, appliances, type of flooring, or attics and garages. In the future, we can add to our model by adding data on mutlifamily building sales as well as trying to find out more information on specific housing amenities and neighborhood perception that might impact the sale price. Another topic we could explore is types of renovations. Would conversions from multiple bedrooms to less bedrooms increase the price? 

# 7. For More Information

Please review our full analysis in our [Jupyter Notebook](https://github.com/ekvu/phase_2_project_vac_pandas/blob/main/Final_Technical_notebook.ipynb) and our [presentation](https://github.com/ekvu/phase_2_project_vac_pandas/blob/main/Phase2_BrianMatsiko_ErinVu_KingCounty.pdf). The data can be found in [/data](https://github.com/ekvu/phase_2_project_vac_pandas/tree/main/data), images in [/images](https://github.com/ekvu/phase_2_project_vac_pandas/tree/main/images), and our working notebooks in [/dev_notebooks](https://github.com/ekvu/phase_2_project_vac_pandas/tree/main/dev_notebooks).

For additional questions, please contact:

Brian Matsiko at makryan77@gmail.com

Erin Vu at erin.vu94@gmail.com

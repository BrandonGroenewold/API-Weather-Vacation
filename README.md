# Ideal Weather and Vacation API

### Before You Begin

1. Create a new repository and be sure to select a `.gitignore` template for Python.

2. Clone the new repository to your computer.

3. Use Visual Studio Code to open this new repo and then edit the `.gitignore` file to add the following the top of the file. 

```python
# Adding file to hold API keys. 
api_keys.py
```

Note: the code above can appear anywhere in your `.gitignore` file

4. Create new files called `WeatherPy.ipynb` and `VacationPy.ipynb`. These will be the main scripts to run for each analysis.

5. Use Git to `add`, `commit`, and `push` the above changes to GitHub.

## Part 1: WeatherPy

In this section, I created a Python script to visualize the weather of 500+ cities of varying distance from the equator. To do so, I used a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and my problem-solving skills to create a representative model of weather across cities.

The first task I did was creating a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, I added a sentence or two explaining what the code is analyzing.

The second task I accomplished was computing the linear regression for each relationship. This time, I separates the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

## Part 2: VacationPy

* **Note:** Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure you can't be charged. Check out [Google Maps Platform Billing](https://developers.google.com/maps/billing/gmp-billing#monitor-and-restrict-consumption) and [Manage your cost of use](https://developers.google.com/maps/documentation/javascript/usage-and-billing#set-caps) for more information.

* To start off part 2 I created a heat map that displays the humidity for every city from Part 1, as in the following image:

  ![heatmap](../Weather-Vacation/Images/heatmap.png)

* Narrowed down the DataFrame to find my ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't satisfy all three conditions. I want to be sure the weather is ideal.

  * **Note:** If you recreate this feel free to adjust your specifications, but make sure to limit the number of rows returned by your API requests to a reasonable number.

* Used Google Places API to find the first hotel for each city located within 5,000 meters of your coordinates.

* Plotted the hotels on top of the humidity heatmap, with each pin containing the **Hotel Name**, **City**, and **Country**, as in the following image:

  ![hotel map](Weather-Vacation/Images/hotel_map.png)

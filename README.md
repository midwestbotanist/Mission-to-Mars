# Mission-to-Mars

## Background
The goal for this project is to scrape the recent articles (titles and preview text) from the Mars news site, along with weather data found on another site. This climate data has been collected by the Curiosity rover that NASA sent to Mars. Both of the deliverables are meant to collect some general information available about Mars, with the focus on Mar's climate.

## Deliverable 1: Scrape Titles and Preview Text from Mars News
In a Jupyter notebook, both Splinter and BeautifulSoup were used to scrape title and preview text from the html code (https://redplanetscience.com/).

### The following code was used to assign the titles and previews for parsing
![Screenshot 2022-11-06 233410](https://user-images.githubusercontent.com/101941048/200233740-35e5019a-fe0c-45db-9baf-898efc32c5e9.png)

### The code was parsed by using a for loop to iterate through each article to collect and create title and preview pairs
![Screenshot 2022-11-06 233320](https://user-images.githubusercontent.com/101941048/200233625-9f463e66-6ac9-4a00-bc91-df62bc70ddfc.png)

### Finally, the article_data dictionary was stored into a json file using json.dumps
![Screenshot 2022-11-06 233502](https://user-images.githubusercontent.com/101941048/200233810-cc8ed5f9-d785-4be4-9b6c-05255976faad.png)

## Deliverable 2: Scrape and Analyze Mars Weather Data
In a Jupyter notebook, Mars temperature data is scraped from a table in the html code (https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html).
This data can be easily scraped using Pandas, though Splinter and BeautifulSoup provide an alternate means. The first attempt in the challenge code shows this method, but due to becoming stuck, Pandas was ultimately used to scrape the table.

### The purpose of scraping the table was to answer the following questions
#### How many months exist on Mars?
* Answer: **12 Months**

    ![Screenshot 2022-11-06 234247](https://user-images.githubusercontent.com/101941048/200234730-2fb545d3-a4fd-4d0c-9a07-384cbc18db74.png)

#### How many Martian (and not Earth) days worth of data exist in the scraped dataset?
* Answer: **1867 Martian Days**

     ![Screenshot 2022-11-06 234527](https://user-images.githubusercontent.com/101941048/200235119-bbd7fb55-e2f6-43ca-9f2f-513352f233aa.png)

### What are the coldest and the warmest months on Mars (at the location of Curiosity)? Get the answer by averaging the minimum daily temperature of all the months. Plot the results as a bar chart.
* Answer: **Month 8 is the warmest month on Mars, at -68.38 degrees F. Month 3 is the coldest month on Mars, at -83.31 degrees F.**

![Screenshot 2022-11-06 234835](https://user-images.githubusercontent.com/101941048/200235364-afac176f-b90f-4417-9180-c9b5aae490af.png)

### Which months have the lowest and the highest atmospheric pressure on Mars? Get the answer by averaging the daily atmospheric pressure of all the months. Plot the results as a bar chart.
* Answer: **Month 9 has the highest atmospheric pressure at 913.31. Month 6 has the lowest atmospheric pressure at 745.10**

    ![Screenshot 2022-11-06 235000](https://user-images.githubusercontent.com/101941048/200235523-6cdb5fde-1790-4e26-9e71-5a1cc1a5f4b8.png)

### About how many terrestrial (Earth) days exist in a Martian year? That is, in the time that Mars circles the Sun once, how many days elapse on Earth? Visually estimate the result by plotting the daily minimum temperature.
* Answer: Using the chart below, we can visually estimate 2.75 Earth years in the data. From this, we can divide the total number of Earth dats in the data and divide by the 2.75 to come up with an estimate of about **~680 days in one Martian year.**
    
    ![Screenshot 2022-11-06 235139](https://user-images.githubusercontent.com/101941048/200235731-9fed47d3-1cee-449f-ba48-d957c731b9d3.png)


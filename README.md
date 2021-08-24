Source: Lede Program 2021 Final Presentation
Mang Lu

## Data Analysis and Visualization of Crime Trends in the District of Columbia


I'm a crime reporter at American Witness, a nonprofit that reports on criminal justice issues in DC and Baltimore. Included in this repository are various projects I've pursued with guidance and feedback from Lede.

### Violence Interrupters

Due to the fact that I began working on this project earlier on in the program, the coding was done using R. Indexed dataframe joining was used to assign a dictionary of locations to homicide incidents in DC. Google Sheets' AwesomeTable plugin was used to automate latitude and longitude; associated errors were corrected and misreadings such as freeway intersections were manually entered.

Geospatial visualization was done in QGIS using a delimited text layer of homicide incident details, including location. Map and graphic design and violence interrupter site labels were created in Photoshop.

### Multiple DC Shootings in One Day

There were two attempts at this mapping project: one in QGIS and one in Google Maps' map builder. QGIS's QuickMapServices plugin was discarded for not being aesthetically pleasing, and Google Maps generates higher resolution images. 

From DC Witness's data collected through court reporting, I constructed a dataframe of days between June 1, 2021 to August 12, 2021 on which multiple homicides involving a shooting or a stabbing occurred. Each homicide is marked by a pin, which is generated in Google Maps. Full graphic created in Photoshop.

### Scraping Cold Cases in DC

I wrote a program to scrape a number of DC's cold cases from an online database for a colleague. Each "row" (each case) included three tables, one for the victim, one for the suspect, and one for case details. I wrote a for loop that read each table from each "row" and appended them, going to the next page (search parameters were included in the URL) automatically. The end result was imperfect, but nothing some Excel cell functions can't fix.

### Scraping MPD Crime Alerts on Twitter and MapBox Visualization

I employed the snscrape package to download all MPD tweets in a given period containing "alert", as MPD crime alerts on Twitter always begin with "ALERT". I used Google Sheets cell functions to draw addresses out of the tweets, and then used Google's AwesomeTable to generate latitudes and longitudes. 

The associated .csv file was imported into geojson.io and imported into an HTML file against a map layer from MapBox's API. I used JS to add pop-up windows indicating the tweet's text and time of publication. I used CSS to make the icons Twitter blue.

### Scraping MPD Homicide Flyer PDFs

Pretty straightforward. I was assigned to collect a large quantity victims' pictures and input them into DC Witness's database. Homicide flyers frequently include a picture of the victim. I scraped each page using BeautifulSoup and downloaded all "href" tags to a specified file path.

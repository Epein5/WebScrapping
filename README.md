
This is a webscrapping that scrapes the website "kissanime.ru" a popular anime site and crawls the trending page of the website through beautifulsoup.

Beautiful soup is used for scrapping 
pandas,sklearn for data manipulation and cleaning
mathplotlib for visualation

# WebScrapping

Firstly the the first trending page is scrapped.Then the code crawls through the trending animes pages one by one reaching upto total of 10 trending pages and 950 anime

Then the Name , ALternatename , condition(completed or ongoing) , no of views , latest-episode and a breif discreption of the anime is scraped from eacha and every pages of the anime.

Name , ALternatename , condition(completed or ongoing) , no of views , latest-episode and a breif discreption of the anime is stored in .txt file.
Name , condition(completed or ongoing) , no of views , latest-episode  is stored in .csv file.


# DataCleaning

Step 1 : removed the new line character"\n" after the end of every row 

Step 2 : Some of the elements in the Latest Episode didnt not contain digits but rather characters(a-z). This woulld hinder while model training and data visualation so  removed the (LatestEpisode)rows containing such non-digits.

step 3 : The datas i.e.(no of views , latest-episode) were stored as string. Converted all the columns of Views and Latest Episode to float. This step makes it ready for model training. 

Step 4 : The 'Condition' column which contains whether the anime is completed or is still ongoing was converted to boolean values 0 and 1


# DataVisualation
fig 1 : shows a ie chart that gives the ratio between Ongoing and Completed Animes.

fig 2 : Shows s bar graph showing the relatiobship between The Top trending animies(left-to right) and their Views 

fig 3 : shows a scatter plot showing the relationship between the total number of views of anime and its Condition(whether it is ongoing or completed)

fig 4 : shows the animies with highest views

fig 5 : shows the anime with highest episodes

# Analysis
Since we scrapped all the trending pages of the website,

1>From the first fig(pie-chart) we found out that the majority of the trending pages is filled with the animes that have already been completed.

2>second figure compares the views of the top 20 trending animies with eachother.It is seen that the top trending anime is far from the maximun views of the anime.

3>we foundd the most viewed anime of all time(One piece) and 19 below it in descending order

4>we foundd the anime with the most episodes of all time(Mrs. Sazae) and 19 others in decsending order

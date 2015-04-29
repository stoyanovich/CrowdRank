# CrowdRank
CrowdRank

This data set consists of 5006 rankings from 351 users on 471 movies. The data was collected through Amazon Mechanical Turk (Mturk) during one-month period from June 11, 2013 through July 16, 2013. We published 50 HITs in total, each of which contains 20 movies for users to rank, and collected 100 assignments for each HIT.

We created these 50 HITs according to the following steps. At first, we randomly chose 945 movies from IMDb, and created 144 blocks of movies. Each block consisting of up to 10 movies is described by a set of attributes, which is a subset of: genre, year, director and popularity.  All movies in the block have the same value for all specified attributes.  Blocks have overlaps in terms of movies. Then we randomly picked blocks of movies that has the right attributes to create 50 HITs, which are of size 20 and have pre-defined attributes, including popularity, director, genre, year and randomization. There are 10 HITs in each category.  The same block can repeat in multiple HITs.  Finally, we randomly reordered movies in each HIT before showing HITs to the user.

We then set a qualification test to collect workers’ demographic information, and published the 50 HITs in MTurk to collect 100 assignments for each HIT. The qualification test consists of four questions:

1. What is your gender?
2. What is your age?
3. What is the highest level of education you have completed?
4. How often do you watch movies?

Once the worker takes the qualification test, they will obtain a qualification value of 100. Workers are required to finish the qualification test to acquire the ranking qualification before doing our HITs. 

For the test run, we published six HITs, including HIT 11, HIT 12, HIT 21, HIT 22, HIT 41 and HIT 42. We collected 100 assignments for each HIT with requiring workers to have an MTurk Master qualification, a ranking qualification value of 90 or higher and an approval rate of 95% or higher with at least 1,000 HITs completed already. We then published the other 44 HITs in three runs with requiring workers to have a ranking qualification value of 90 or higher and an approval rate of 80% or higher with at least 1,000 HITs completed already.

First run: HIT 31-40, HIT 23-27
Second run: HIT 1-10, HIT 13-17
Third run: HIT 18-20, HIT 28-30, HIT 43-50


Here are brief descriptions of the data.

movies  -- Information about the movies; this is a list of movieid|Title|Year|Rated|Released|Runtime|Director|Writer|Actors|Poster|imdbRating|imdbVotes|imdbID|Action|Adventure|Animation|Biography|Comedy|Crime|Documentary|Drama|Family|Fantasy|History|Horror|Mistery|Romance|Sci-Fi|Thriller|War|Western.

The last 18 fields are the genres, a 1 indicates the movie is of that genre, a 0 indicates it is not; movies can be in several genres at once.

hits  -- Information about the HITs; this is a list of hitid|movieid.

workers  -- Information about the workers; this is a list of workerid|MTurkWorkerID|LinkToPage|NumberOfHITs|gender|age|education|frequency.

Education: 1 -- Some high school
           2 -- High school graduate
           3 -- Some college, no degree
           4 -- Associates degree
           5 -- Bachelors degree
           6 -- Graduate degree (Masters, Doctorate, etc.)
           7 -- Other

Frequency: 1 -- 10+ a week
           2 -- 5-9 a week
           3 -- 3-4 a week
           4 -- 1-2 a week
           5 -- 1-3 a month

rankings  -- Information about the ranking results; this is a list of workerid|hitid|movieid|rank.

blocks -- Information about the movies in each block.

attributesofblocks -- information about the attributes of each block.

blocksinhits -- Information about the blocks in each HIT.

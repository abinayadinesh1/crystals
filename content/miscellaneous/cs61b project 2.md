
<s>Final</s>
Project 2 (Ngordnet)
	2a - 800 points
	https://www.gradescope.com/courses/484660/assignments/2695548/submissions/168822229
		just need to do **history handlers**
		time series, ngram map count, and ngram map weight are already done


Intro video!
ngrams dataset (for 2a)
single word, for every year in a range of years, write how many times that word was mentioned vs all the others 
static/ngordnet_2a.html is where we can look at how this works


take queries and return strings in history text handler



wordnet dataset

by 8:10, i want to be caught up on what the heck is going on
	<mark style="background: #ABF7F7A6;">timeseries</mark>
		year: number
		for every word, have an associated timeseries
		extends a treemap, with an integer (year) and double (frequency)

two constructors: 
1. empty treemap TimeSeries()
2. timeseries between specific years TimeSeries(TimeSeries ts, int startYear, int endYear)

commands:
1. List Integer  years() - returns all the years in a list (just the keys)
2. List Double data() - returns all the frequencies (just the values)
3. TimeSeries plus(TimeSeries ts) - basically just take all the years within the min to max range, if its in both, add the sum to a new timeseries, and if its only in one just add that one
4. TimeSeries dividedBy(TimeSeries ts) - does the same just divides if its both



<mark style="background: #ABF7F7A6;">ngram map</mark>
		give it two data files - words and counts of words
		countHistory
		totalCountHistory
		weightHistory
		summedWeightHistories


read the data:
 words - has the word and its frequency in the year
 total counts - total number of words in that year

ngrammap.wordInfo2 = String, TimeSeries (Year, Frequency)

<mark style="background: #ABF7F7A6;">history text handler</mark>

started at 8pm
1.  Create a new file called `HistoryTextHandler.java` that takes the given `NgordnetQuery` and returns a String in the same format as above.
3. Modify `Main.java` so that your `HistoryTextHandler` is used when someone clicks `History (Text)`. In other words, instead of registering `DummyHistoryTextHandler`, you should register your `HistoryTextHandler` class instead.


what sort of request are we getting?
what data structures can we use to get the info we need?
	timeseries
what do we need?



for every word in the request, return search and return that word in the ngrammap

finished at 10pm


2b - 2400 points
	https://www.gradescope.com/courses/484660/assignments/2722448/submissions/172268702




Project 3 (BYOW)
	total - 3200 points
	just have to email them asking why i wasnt graded for this when 

asking for **relative popularity** of the words cat and dog in the given years
take each of the words
get the time series of the frequency per year of that word
divide one by the other


divide the time series of that word with the one of all the words





how does historytexthandler have access to ngm?
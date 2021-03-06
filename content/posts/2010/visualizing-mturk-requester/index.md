Visualizing MTurk requesters
============================
categories: [web, social]
posted: 2010-02-06
snip: A quick stab at scraping Mechanical Turk for statistics into a Google Spreadsheet,
  and then using Google's Visualization APIs to present that data in a meaningful
  way.




I signed up to do one month of paid research at CMU|Portugal before
spring classes start. My task boils down to creating interesting
visualizations. The bad news is that I have no experience visualizing
data and the dataset I'm to visualize hasn't yet been collected.
Fortunately, I've always been *theoretically* interested in data
visualization, so I was happy to have a solid excuse to explore the
subject. All I needed was a sufficiently rich data set, mad skills and a
bit of inspiration.

Lately, I've been pretty excited about squeezing some new potential out
of Mechanical Turk. Part of my research involves finding patterns in
Mechanical Turk requester strategies. A few weeks ago, I began gathering
data with a [python program][] that extracts all scrape-able information
about every HIT group and stores it in a sqlite3 database. This is quite
an interesting data set, so I pounced on the opportunity to visualize
it, killing two birds with one stone.

Due to lack of time, I decided to skip most of the 
[visualization literature][]. Instead, I found a great 
[visualization project database][] and started writing simple examples
using some popular
visualization languages and frameworks. I began with [Processing][] and
[Processing.js][] but quickly tired of the raster-based drawing model. I
turned to SVG with [Raphaël][] and jQuery and ended up building a simple
bubble chart. I had no specific visualization in mind, so my vague goal
was to be able to visualize data in [Hans Rosling][]'s favorite
five-dimensional (x, y, size, color, time) graph. Making this graph
animate, however, proved to be quite difficult.

![image][] 

I turned to
the internet for help, and Itai Raz [explained to me][] in his thick
Israeli accent that the Google Visualization API is pretty sweet.
Moreover, it comes with the exact visualization I wanted to implement,
apparently called the [Motion Chart][]. Happily, Google Spreadsheets
export data in the format that the visualization framework consumes.
Thus my problem was greatly reduced to one of analyzing and uploading
data to a Google Spreadsheet. Turns out that this too is quite easy
using the python [GData framework][].

I decided to visualize differences between requester strategies on
Mechanical Turk. Every time I scrape, I generate a Average Reward (x),
Average Allotted Time (y), Total Number of Hits (size) graph for the top
50 requesters, and then upload it to a google spreadsheet. Here is the
[python program][] I wrote for this purpose. [The results][] are
interesting and fun to play with. Google's Motion Chart visualization is
incredibly powerful and flexible. I won't go in detail into findings
from the data since it's irrelevant to this largely technical discussion
about visualization technologies. I'll soon get my hands on the data I'm
expecting and create a custom visualization for it with the Google
Visualization API. Stay chooned!

  []: turk-visualizer/
  [python program]: turk-visualizer/turk_scraper.py
  [visualization literature]: http://www.amazon.com/Visual-Display-Quantitative-Information/dp/096139210X
  [visualization project database]: http://www.visualcomplexity.com/vc/
  [Processing]: http://processing.org/
  [Processing.js]: http://processingjs.org/
  [Raphaël]: http://raphaeljs.com/
  [Hans Rosling]: http://www.gapminder.org/
  [image]: raphael.jpg
  [explained to me]: http://www.youtube.com/watch?v=guhdYoPY3kM
  [Motion Chart]: http://code.google.com/apis/visualization/documentation/gallery/motionchart.html
  [GData framework]: http://code.google.com/p/gdata-python-client/
  [python program]: turk-visualizer/turkviz_scraper.py
  [The results]: http://www.borismus.com/wp-content/uploads/2010/02/turk_requester_visualizer.html


# 2\_web_scrape

Now that we've familiarized ourselves with the ways Python works, we have a little bit of a foundation to build from. Nearly everything else we do today is going to be using the fundamentals from [1_start](https://github.com/richardsalex/coding_for_journos/tree/master/1_start) to varying degrees and in different combinations to create longer scripts.

So let's scrape a web page. We want to collect all the data from the main table on the U.S. Nuclear Regulatory Commission's [list of domestic power reactor units](http://www.nrc.gov/reactors/operating/list-power-reactor-units.html).

Python comes with a library installed that's designed specifically for reading and writing CSV files ([```csv```](https://docs.python.org/2/library/csv.html)), but we're also going to need to extend Python's functionality a bit by bringing in two other libraries.

One is [```requests```](http://docs.python-requests.org/en/latest/) -- it handles the job of playing a web browser that can fetch a web page and send back the underlying HTML. The other is [```BeautifulSoup```](http://www.crummy.com/software/BeautifulSoup/), which parses the HTML into what amounts to a series of lists that we can then search, navigate and extract data from.

When we get to part two, we'll use the built-in regular expressions library [```re```](https://docs.python.org/2/library/re.html) to isolate some text from the detail pages and [```time```](https://docs.python.org/2/library/time.html) to keep us from swamping a government site with too many requests at once.

A big thank you to [Anthony DeBarros](https://twitter.com/anthonydb) for allowing us to present a modified version of his web scraping example from [python-get-started](https://github.com/anthonydb/python-get-started).

This exercise contains six files:

- **scrape.py**: The file we'll use to write our scraping script, following the comments.

- **scrape_pt2.py**: The file we'll use to push our scraping script further; it contains finished code for **scrape.py** and open spots to add code that loops through to detail pages and collects additional information.

- **nrc_backup.html**: A backup version of the main table we want to scrape in case there's a connection problem.

- **table_example.html**: A bare bones HTML table that shows the basic tags and how they're nested, with the flourishes of a modern web page stripped away -- it's ugly.
- **scrape_done.py**: A completed and working version of **scrape.py**.
 
- **scrape\_pt2\_done.py**: A completed and working version of **scrape_pt2.py**. 
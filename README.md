# tidyr

[![Build Status](https://travis-ci.org/hadley/tidyr.png?branch=master)](https://travis-ci.org/hadley/tidyr)

tidyr is a reframing of reshape2 designed to accompany the [tidy data framework](http://vita.had.co.nz/papers/tidy-data.html), and to work hand-in-hand with magrittr and dplyr to build a solid pipeline for data analysis. 

Just as reshape2 did less than reshape, tidy2 does less than reshape2. It's designed specifically for tidying data, not the general reshaping that reshape2 does, or the general aggregation that reshape did. In particular, built-in methods only work for data frames, and tidyr provides no margins or aggregation. 

There are two fundamental verbs of data tidying: 

* `gather()` takes multiple columns, and gathers them into key-value pairs: it 
  makes "wide" data longer.

* `spread()`. takes two columns (key & value) and spreads in to multiple 
  columns, it makes "long" data wider. 

These verbs have a number of synonyms:

| tidyr        | gather | spread  |
|--------------|--------|---------|
| reshape(2)   | melt   | cast    |
| spreadsheets | pivot  | unpivot | 
| databases    | fold   | unfold  |

tidyr also provides `separate()` function which makes it easier to turn a single character column into multiple columns either according to regular expression, or by fixed positions. The component to `separate()` is `unite()`.

## Installation

tidyr is not available from CRAN (yet!) but you can get it with:

```s
# install.packages("devtools")
devtools::install_github("hadley/tidyr")
```

## Getting started

To get started, check out the `demos/`.  Note that tidyr is designed for use in conjunction with dplyr, so you should always load both:

```s
library(tidyr)
library(dplyr)
```
## References

If you'd like to learn more about these data reshaping operators, I'd recommend the following papers:

* [Wrangler: Interactive visual specification of data transformation scripts](http://vis.stanford.edu/papers/wrangler)
* [An interactive framework for data cleaning](http://www.eecs.berkeley.edu/Pubs/TechRpts/2000/CSD-00-1110.pdf) (Potter's wheel)
* [On efficiently implementing SchemaSQL on a SQL database system](http://www.vldb.org/conf/1999/P45.pdf)


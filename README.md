# p8105_hw2_ys3298
Problem 1
This problem uses the Mr. Trash Wheel dataset, available as an Excel file on the course website.

Read and clean the Mr. Trash Wheel sheet:

specify the sheet in the Excel file and to omit non-data entries (rows with notes / figures; columns containing notes) using arguments in read_excel
use reasonable variable names
omit rows that do not include dumpster-specific data
round the number of sports balls to the nearest integer and converts the result to an integer variable (using as.integer)
Read and clean precipitation data for 2017 and 2018. For each, omit rows without precipitation data and add a variable year. Next, combine precipitation datasets and convert month to a character variable (the variable month.name is built into R and should be useful).

Write a paragraph about these data; you are encouraged to use inline R. Be sure to note the number of observations in both resulting datasets, and give examples of key variables. For available data, what was the total precipitation in 2018? What was the median number of sports balls in a dumpster in 2017?

Problem 2
This problem uses the FiveThirtyEight data; these data were gathered to create the interactive graphic on this page. In particular, we’ll use the data in pols-month.csv, unemployment.csv, and snp.csv. Our goal is to merge these into a single data frame using year and month as keys across datasets.

First, clean the data in pols-month.csv. Use separate() to break up the variable mon into integer variables year, month, and day; replace month number with month name; create a president variable taking values gop and dem, and remove prez_dem and prez_gop; and remove the day variable.

Second, clean the data in snp.csv using a similar process to the above. For consistency across datasets, arrange according to year and month, and organize so that year and month are the leading columns.

Third, tidy the unemployment data so that it can be merged with the previous datasets. This process will involve switching from “wide” to “long” format; ensuring that key variables have the same name; and ensuring that key variables take the same values.

Join the datasets by merging snp into pols, and merging unemployment into the result.

Write a short paragraph about these datasets. Explain briefly what each dataset contained, and describe the resulting dataset (e.g. give the dimension, range of years, and names of key variables).

Note: we could have used a date variable as a key instead of creating year and month keys; doing so would help with some kinds of plotting, and be a more accurate representation of the data. Date formats are tricky, though. For more information check out the lubridate package in the tidyverse.

Problem 3
This problem uses data from NYC Open data on the popularity of baby names, and can be downloaded here.

Load and tidy the data. Note that, although these data may seem fairly well formatted initially, the names of a categorical predictor and the case structure of string variables changed over time; you’ll need to address this in your data cleaning. Also, some rows seem duplicated, and these will need to be removed (hint: google something like “dplyr remove duplicate rows” to get started).

Produce a well-structured, reader-friendly table showing the rank in popularity of the name “Olivia” as a female baby name over time; this should have rows for ethnicities and columns for year. Produce a similar table showing the most popular name among male children over time.

Finally, for male, white non-hispanic children born in 2016, produce a scatter plot showing the number of children with a name (y axis) against the rank in popularity of that name (x axis).
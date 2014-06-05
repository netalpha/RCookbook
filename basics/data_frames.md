# Data Frames

Data frames are the data structure most indicated for storing the data tables. They are similar to matrices in structure as they are also dimensional. However, contrary to matrices, data frames may include data of a different type in each column. So data frames are a special class of lists. Each row of a data frame is an _observation(or case)_, being described by a set of _variable_.

	> my.dataset <- data.frame(site=c('A', 'B', 'A', 'A', 'B'), season=c('Winter', 'Summer', 'Summer', 'Spring', 'Fall'), pH=c(7.4, 6.3, 8.6, 7.2 8.9))
	> my.dataset
	   site  season   pH
	1   A    Winter    7.4
	2   B    Summer    6.3
	3   A    Summer    8.6
	4   A    Spring    7.2
	5   B    Fall      8.9

### Subset

	> my.dataset(3, 2)
	[1] Summer
	Levels: Fall Spring Summer Winter
	# 'season' column has been coerced into a factor, which is the default behavior of the data.frame() function.
	> my.dataset$pH
	[1] 7.4 6.3 8.6 7.2 8.9
	> my.dataset[my.dataset$pH > 7, ]
	   site  season   pH
	1   A    Winter    7.4
	3   A    Summer    8.6
	4   A    Spring    7.2
	5   B    Fall      8.9
	> my.dataset[my.dataset$site == 'A', 'pH']
	[1] 7.4 8.6 7.2

### Attach and detach

The function of _attach()_ simplifies the typing of these queries.

	> attach(my.dataset)
	> my.dataset[site=='B',]
	  site season  pH
	2  B   Summer 6.3
	5  B   Fall   8.9
	> season
	[1] Winter Summer Summer Spring Fall
	Levels: Fall Spring Summer Winter
	> detach(my.dataset)
	> season
	Error: Object "season" not found

### Using the function of subset()

	> subset(my.dataset, pH>8)
	  site season pH
	3  A   Summer 8.6
	5  B   Fall   8.9
	> subset(my.dataset, season == "Summer", season:pH)
	   season  pH
	2   Summer  6.3
	3   Summer  8.6

### The number of rows and columns

	> nrow(my.dataset)
	[1] 5
	> ncol(my.dataset)
	[1] 3

### Spreadsheet-like interface

	> my.dataset <- edit(my.dataset)
	> new.dataset <- edit(data.frame())

### Names of the columns

The name attribute is a vector.
	> names(my.dataset)
	[1] "site" "season" "pH"
	> names(my.dataset)[3] <- "PH"

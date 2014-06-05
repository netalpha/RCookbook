# Some Useful Command

### Package Management

	> installed.packages() # know the packages installed
	> library() # know the packages installed in a more user-friendly, but less complete way
	> old.packages() # know the outdated packages
	> update.packages() # update the outdated packages

### Build-in Dataset

	> data()
	> data(USArrests)
	# to use the dataset of 'USArrests'

### Execution of a source file

	> source('mysourcecode.R')

### Changint the workspace

	> getwd()
	> setwd("some_dir")

### Save the objects

	> save(f, my.dataset, file='mysession.RData')
	# save the objects named f and my.dataset
	> load("mysession.RData")
	> save.image()
	# save all the objects in the workspace
